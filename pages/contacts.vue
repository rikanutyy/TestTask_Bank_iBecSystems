<template>
  <div id="app" class="container">
    <div id="map" class="map_style"></div>
  </div>
</template>

<script>
import PinIcon from '@/assets/icons/pin.png';

export default {
  name: 'app',

  created() {
    var myMap,
        myPlacemark;

    ymaps.ready(function () {
        // Создание карты.
        var myMap = new ymaps.Map("map", {
            // Координаты центра карты.
            // Порядок по умолчанию: «широта, долгота».
            // Чтобы не определять координаты центра карты вручную,
            // воспользуйтесь инструментом Определение координат.
            center: [43.24782388563741,76.92575895545819],
            // Уровень масштабирования. Допустимые значения:
            // от 0 (весь мир) до 19.
            zoom: 13
        });
    myMap.controls
         .remove('geolocationControl')
         .remove('trafficControl')
         .remove('searchControl')
         .remove('rulerControl');

    myMap.behaviors.disable([
            'drag',
            'scrollZoom'
    ]),
// Мега парк
        myMap.balloon.open([43.26412725590698,76.92990486508174], "Мега парк", {closeButton: false});

// Нурлы-тау
        var myPlacemark = new ymaps.Placemark([43.23059880179226,76.94600918650815], null, {
            iconLayout: 'default#image',
            iconImageHref: PinIcon,
            iconImageSize: [32, 32],
            iconImageOffset: [-7, -21]
        });

        myMap.geoObjects.add(myPlacemark);
    });
  }
}
</script>

<style lang="scss">
.map_style {
    margin: 50px auto 25px;
    height: 470px;
    text-align: center;
}
</style>