<script setup>
    
</script>

<template>
    <div id="hobies">
      <h2 class="text-highlight-1 section-title">LOISIRES</h2>
      <div id="icons-list">
        <div class="hobie-container">
          <img class="hobie-icon" src="@/assets/football.png" alt="Football" />
          <span>Football</span>
        </div>
        <div class="hobie-container">
          <img class="hobie-icon" src="@/assets/natation.png" alt="Natation" />
          <span>Natation</span>
        </div>
        <div class="hobie-container">
          <img class="hobie-icon" src="@/assets/voyageur-avec-bagages.png" alt="Voyage" />
          <span>Voyage</span>
        </div>
      </div>
    </div>
  </template>

<style scoped>
    #hobies {
  margin-top: 60px!important;
}

#icons-list {
  display: flex;
  justify-content: left;
  flex-wrap: wrap;
  gap: 50px;
  margin-top: 35px;
}

.hobie-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  color: var(--vt-c-custom-text-1);
  transition: transform 0.5s;
}

.hobie-container span {
  font-weight: bold;
  margin-top: 10px;
}

.hobie-container:hover {
  transform: rotate(15deg);
  color: var(--vt-c-custom-text-2);
}

.hobie-icon {
  width: 100px; /* Taille fixe pour toutes les images */
  height: 100px;
  object-fit: contain;
  display: block;
}

@media screen and (max-width: 905px) {
  #icons-list {
    gap: 30px;
  }
}

@media screen and (max-width: 450px) {
  #icons-list {
    gap: 20px;
  }
}
</style>