<template>
  <div>
    <div class="team-pres">
      <h1 style="font-weight: bold;">Présentation du Projet</h1>
      <div class="pres-container">
        <img src="/src/assets/imgYFest.png" class="pres-image">
        <p class="presProjet">Notre projet vise à créer une expérience en ligne immersive pour les amateurs de festivals, offrant un aperçu complet des événements musicaux à venir au cours des prochains jours, semaines et mois. Sur notre plateforme, les passionnés de musique pourront explorer en détail chaque festival, découvrir tous les artistes qui s'y produiront, et même réserver leurs billets en ligne en toute simplicité. Notre objectif est de faciliter la planification de vos sorties musicales, de mettre en avant les talents artistiques, et de vous offrir un accès rapide et pratique à l'univers vibrant et passionnant des festivals.</p>
      </div>
      <h2 style="font-weight: bold;">Présentation de l'Équipe</h2>
    </div>
    <div class="team-cards">
      <div class="team-row">
        <div v-for="(membre, index) in equipe.slice(0, 3)" :key="membre.id" class="team-card">
          <img :src="membre.image" alt="Photo de {{ membre.nom }}" class="member-image" />
          <h3>{{ membre.nom }}</h3>
          <p>{{ membre.role }}</p>
        </div>
      </div>
      <div class="team-row">
        <div v-for="(membre, index) in equipe.slice(3, 6)" :key="membre.id" class="team-card">
          <img :src="membre.image" alt="Photo de {{ membre.nom }}" class="member-image" />
          <h3>{{ membre.nom }}</h3>
          <p>{{ membre.role }}</p>
        </div>
      </div>
    </div>
    <div class="section-container">
      <section class="team-section">
        <h3 style="font-size: 1.5em;">Fonctionnalité MVP</h3>
        <h4>Affichage carte France avec les lieux</h4>
        <h4>Descriptif festival, Liste des artistes présent</h4>
        <h4>Transport (temps, prix, distance, etc....)</h4> 
        <h4>Logement (sur le festival ou autour)</h4> 
        <h4>Organisation du festival (Ou sont les toilettes, les bars, la bouffe, etc…)</h4> 
        <h4>Création d’un compte, connexion+ Billetterie </h4>
      </section>
      <section class="team-section">
        <h3 style="font-size: 1.5em; ">Fonctionnalité site web V2</h3>
        <h4>Avec les artistes, leurs tournée actuelles et/ou prévu, tous leurs albums et sons</h4> 
        <h4>Comparatif des prix pour les différents types de transport et compagnies</h4> 
        <h4>Comparatif des prix pour les différents ébergements présents dans la ville en question</h4>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      equipe: [
        { id: 1, nom: 'FOLTZER Thomas', role: 'B2 Informatique', image: '/src/assets/amaury.jpg' },
        { id: 2, nom: 'CHEVALIER Tim', role: 'B3 Cybersécurité', image: '/src/assets/tim.png' },
        { id: 3, nom: 'RODRIGUEZ Thomas', role: 'B3 Developpement', image: '/src/assets/amaury.jpg' },
        { id: 4, nom: 'PIERRE Quentin', role: 'B3 Infrastructure & SI', image: '/src/assets/amaury.jpg' },
        { id: 5, nom: 'LE BARAZER Manon', role: 'B2 Infomatique', image: '/src/assets/manon.png' },
        { id: 6, nom: 'LYONNET Amaury', role: 'B3 Infrastructure & SI', image: '/src/assets/amaury.jpg' },
      ],
    };
  },
};
</script>

<style scoped>
/* Ajoutez vos styles CSS ici */
.pres-container{
  display: flex;
  align-items: center;
}
.pres-image{
  width: 40%;
  height: 40%;
}
.presProjet{
  margin-left: 10%;
  width: 50%;
  font-size: 1.25em;
}
.team-cards {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.team-row {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin-bottom: 20px;
}

.team-card {
  flex: 1; /* Les cartes occupent un espace équitable */
  max-width: calc(33.33% - 20px);
  padding: 10px;
  text-align: center;
  border: 1px solid #EE2677;
  margin-right: 20px;
  box-sizing: border-box;
}

.team-card:last-child {
  margin-right: 0; /* Pas de marge à droite pour la dernière carte de chaque ligne */
}

.member-image {
  max-width: 70%;
  max-height: 70%;
}

.section-container{
  display: flex;
  flex-direction: row;
  justify-content:start;
  align-items: start;
}

.team-section{
  /* justify-content: center; */
  /* align-items: center; */
  width: 100%;
}
  @media screen and (max-width : 900px) {
  .press-container {
    flex-direction: column;
  } 
}
</style>
