<template>
		<!-- Карточка "Мои счета" -->
    <div class="col-12 col-md-6">
      <div class="card">

        <div class="card__head d-flex">
          <img :src="iconSuitcase">
          <h5 class="card__title">{{ cardTitle }}</h5>
        </div>

        <div class="card__body">
          <!-- Здесь должны были быть логи счетов -->
          <!-- <p class="card__text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, tempora!</p> -->
        </div>
      </div>
    </div>
</template>

<script>

// icons (IMG)
import iconSuitcase from '@/assets/icons/Suitcase.png';

export default {
  data() {
    return {
      iconSuitcase,
      cardTitle: "Мои счета"
    };
  }
};
</script>