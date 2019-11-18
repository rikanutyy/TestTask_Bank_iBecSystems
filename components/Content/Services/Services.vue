<template>
<div class="row">
    <!-- Карточка "Шаблоны операций" -->
    <div class="col-12 col-md-12">
      
        <div class="row">
          <div class="col-12">
            <adRate />
          </div>
          <div class="col-6 col-lg-12">
            <adAutoCredit />
          </div>
          <div class="col-6 col-lg-12">
            <adDeposits />
          </div>

        </div>

    </div>
</div>
</template>

<script>
import adRate from '@/components/Content/Services/_ad_rate';
import adAutoCredit from '@/components/Content/Services/_ad_autoCredit';
import adDeposits from '@/components/Content/Services/_ad_deposits';

export default {
  components: {
    adRate,
    adAutoCredit,
    adDeposits
  }
}
</script>

<style lang="scss">
.ad {
  background: $card-bc;
  min-height: $height-ad;
  border: $card-border;
  border-radius: 5px;
  margin-bottom: $default-indent;
}

.ad__head {
  .ad__icon {
    display: block;
    z-index: 1;
  }
  .ad__title {
    font-size: $ad-title-fc;
    color: $text-color;
    width: 100%;
    padding: 15px 0;
    text-align: center;
  }
}
.ad__body {
  text-align: center;

  img {
    display: block;
    margin: 0 auto;
    width: 100%;
  }
  .ad__btn {
    border: 0;
    outline: 0;
    color: $ad-btn-fc;
    background: $ad-btn-bc;
    width: 100%;
    padding: 6px 12px;

      border-bottom-left-radius: 5px;
      border-bottom-right-radius: 5px;
  }
}
</style>
