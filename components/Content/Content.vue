<template>
<div class="Content">
 <div class="container">

  <div class="row">
      <div class="left-section col-lg-10">
        <div class="row">
          <cardMyBills />
          <cardOpPatterns />

          <cardMyBills />
          <cardOpPatterns />

          <cardMyBills />
          <cardOpPatterns />

          <cardMyBills/>
          <cardOpPatterns />
        </div>
      </div>

      <div class="right-section col-lg-2">
         <Services />
      </div>

  </div><!-- row END -->

 </div><!-- container END -->
</div><!-- Content END -->
</template>

<script>

// icons (IMG)
import cardMyBills from '@/components/Content/_card_myBills';
import cardOpPatterns from '@/components/Content/_card_opPatterns';
import Services from '@/components/Content/Services/Services';

export default {
  components: {
    cardMyBills,
    cardOpPatterns,
    Services
  }
}
</script>

<style lang="scss">
.Content {
  margin-top: ($default-indent*2);
}
.card {
  background: $card-bc;
  padding: 0 10px;
  min-height: $height-card;
  border: $card-border;
  border-radius: 5px;
  margin-bottom: ($default-indent+5);
}

.card__head {
  .card__icon {
    display: block;
    z-index: 1;
  }
  .card__title {
    font-size: $card-title-fc;
    color: $heading-text-color;
    width: 100%;
    border-bottom: $card-title-border;
    padding: 15px 0;
    margin-left: 10px;
  }
}
</style>
