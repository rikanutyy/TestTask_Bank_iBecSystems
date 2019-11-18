<template>
    <!-- Карточка "Шаблоны операций" -->
    <div class="col-12 col-md-6">
      <div class="card">

        <div class="card__head d-flex">
          <img :src="iconDocuments">
          <h5 class="card__title">{{ cardTitle }}</h5>
        </div>

        <div class="card__body">
          <!-- Здесь должны были быть шаблоны операций -->
          <!-- <p class="card__text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat, tempora!</p> -->
        </div>
      </div>
    </div>
</template>

<script>

// icons (IMG)
import iconDocuments from '@/assets/icons/Documents.png';

export default {
  data() {
    return {
      iconDocuments,
      cardTitle: "Шаблоны операций"
    };
  }
};
</script>