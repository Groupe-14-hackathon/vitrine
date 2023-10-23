<script setup>
import logo from "../assets/imgYFest.png";

const equipe = [
  {
    id: 1,
    nom: "FOLTZER Thomas",
    role: "B2 Informatique",
  },
  {
    id: 2,
    nom: "CHEVALIER Tim",
    role: "B3 Cybersécurité",
  },
  {
    id: 3,
    nom: "RODRIGUEZ Thomas",
    role: "B3 Developpement",
  },
  {
    id: 4,
    nom: "PIERRE Quentin",
    role: "B3 Infrastructure & SI",
  },
  {
    id: 5,
    nom: "LE BARAZER Manon",
    role: "B2 Infomatique",
  },
  {
    id: 6,
    nom: "LYONNET Amaury",
    role: "B3 Infrastructure & SI",
  },
];
</script>

<template>
  <div>
    <div class="team-pres">
      <h1 class="title" style="font-weight: bold">PRESENTATION DU PROJET</h1>
      <div class="pres-container">
        <img src="/src/assets/imgYFest.png" class="pres-image" />
        <p class="presProjet">
          Notre projet vise à créer une expérience en ligne immersive pour les
          amateurs de festivals, offrant un aperçu complet des événements
          musicaux à venir au cours des prochains jours, semaines et mois. Sur
          notre plateforme, les passionnés de musique pourront explorer en
          détail chaque festival, découvrir tous les artistes qui s'y
          produiront, et même réserver leurs billets en ligne en toute
          simplicité. Notre objectif est de faciliter la planification de vos
          sorties musicales, de mettre en avant les talents artistiques, et de
          vous offrir un accès rapide et pratique à l'univers vibrant et
          passionnant des festivals.
        </p>
      </div>
      <div id="line">
        <div class="line"></div>
      </div>
      <h2 style="font-weight: bold">PRESENTATION DE L'EQUIPE</h2>
    </div>
    <div class="team-cards">
      <div class="team-row">
        <div
          v-for="(membre, index) in equipe.slice(0, 3)"
          :key="membre.id"
          class="team-card"
        >
          <h3>{{ membre.nom }}</h3>
          <p>{{ membre.role }}</p>
        </div>
      </div>
      <div class="team-row">
        <div
          v-for="(membre, index) in equipe.slice(3, 6)"
          :key="membre.id"
          class="team-card"
        >
          <img :src="membre.image" class="member-image" />
          <h3>{{ membre.nom }}</h3>
          <p>{{ membre.role }}</p>
        </div>
      </div>
    </div>
    <div id="line">
      <div class="line"></div>
    </div>
    <div class="section-container">
      <section class="team-section">
        <h3 style="font-size: 1.5em">Fonctionnalité MVP</h3>
        <p class="fonct">Affichage carte France avec les lieux</p>
        <p class="fonct">Descriptif festival, Liste des artistes présent</p>
        <p class="fonct">
          Organisation du festival (Où sont les toilettes, les bars, la
          nourriture, etc…)
        </p>
        <p class="fonct">Création d’un compte, connexion+ Billetterie</p>
      </section>
      <section class="team-section">
        <h3 style="font-size: 1.5em">Fonctionnalité site web V2</h3>
        <p class="fonct">
          Avec les artistes, leurs tournée actuelles et/ou prévu, tous leurs
          albums et sons
        </p>
        <p class="fonct">
          Comparatif des prix pour les différents types de transport et
          compagnies
        </p>
        <p class="fonct">
          Comparatif des prix pour les différents ébergements présents dans la
          ville en question
        </p>
        <p class="fonct">Transport (temps, prix, distance, etc....)</p>
        <p class="fonct">Logement (sur le festival ou autour)</p>
      </section>
    </div>
    <div id="line">
      <div class="line"></div>
    </div>

    <h3 style="font-size: 1.5em">LIENS IMPORTANTS</h3>
   <div class="link">
      <a target="_blank" href="https://github.com/orgs/Groupe-14-hackathon/repositories"
      >Github</a
       >
      <a target="_blank" href="https://yfestival.netlify.app">App Yfestival</a>
   </div>
  </div>
</template>

<style scoped>

.link {
  display: flex;
  flex-direction: column;
  justify-content: space-between;

}

.pres-container {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.pres-image {
  width: 40%;
  height: 40%;
}

.presProjet {
  margin-left: 10%;
  width: 50%;
  font-size: 1.25em;
}

.team-cards {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: black;
}

.team-row {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin-bottom: 20px;
}

.team-card {
  flex: 1;
  /* Les cartes occupent un espace équitable */
  max-width: calc(33.33% - 20px);
  cursor: pointer;
  padding: 10px;
  text-align: center;
  width: 20%;
  background-color: #ebb3a9;
  box-shadow: 5px 5px 5px rgb(132, 131, 131);
  border-radius: 0.8rem;
  padding: 25px;
  box-sizing: border-box;
}
.team-card:hover {
  background-color: #eca99d;
}
@media screen and (max-width: 900px) {
  .team-card {
    width: 70%;
    margin-bottom: 20px;
  }
}

.team-card:last-child {
  margin-right: 0;
  /* Pas de marge à droite pour la dernière carte de chaque ligne */
}

.member-image {
  max-width: 70%;
  max-height: 70%;
}

.section-container {
  display: flex;
  flex-direction: row;
  justify-content: start;
  align-items: start;
}

.team-section {
  width: 100%;
}

@media screen and (max-width: 900px) {
  .pres-container {
    margin-top: 10%;
    flex-direction: column;
  }

  .title {
    font-size: 1.75em;
  }

  .presProjet {
    font-size: 1em;
    width: 80%;
    margin-left: 0;
  }

  .team-row {
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .team-card {
    max-width: calc(90% + 20px);
  }

  .member-image {
    max-width: 80%;
    max-height: 80%;
  }

  .section-container {
    flex-direction: column;
  }

  .fonct {
    font-size: 1em;
  }
}
</style>
