<template>
<!-- Депозиты -->
      <div class="ad">
        <div class="ad__body">
          <img :src="imgDeposits">
          <button class="ad__btn">Депозиты</button>
        </div>
      </div><!-- ad END -->
</template>

<script>

// icons (IMG)
import imgDeposits from '@/assets/images/imgWoman.png';

export default {
  data() {
    return {
      imgDeposits
    };
  }
};
</script>