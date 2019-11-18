<template>
<!-- Авто в кредит -->
      <div class="ad">
        <div class="ad__body">
          <img :src="imgAutoCredit">
          <button class="ad__btn">Кредит Auto</button>
        </div>
      </div><!-- ad END -->
</template>

<script>

// icons (IMG)
import imgAutoCredit from '@/assets/images/imgCar.png';

export default {
  data() {
    return {
      imgAutoCredit
    };
  }
};
</script>