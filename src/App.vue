<template>
  <header-uber-eats />
  <main class="main-container">
    <input-restaurant class="mt-5" />
    <h1 class="name-list-restaurant">Рестораны в Москве</h1>
    <div class="d-flex flex-wrap row">
      <restaurant-item
        v-for="restaurant in restaurants"
        :key="restaurant"
        :restaurant="restaurant"
        class="col-lg-4 col-md-6 col-12 mt-4"
      />
    </div>
  </main>
  <footer-uber-eats class="footer-uber-eats"/>
</template>

<script>
import headerUberEats from "./components/index-components/header-uber-eats";
import inputRestaurant from "./components/index-components/input-restaurant.vue";
import restaurantItem from "./components/index-components/restaurant-item.vue";
import footerUberEats from "./components/index-components/footer-uber-eats.vue";
export default {
  components: {
    headerUberEats,
    inputRestaurant,
    restaurantItem,
    footerUberEats,
  },
  data() {
    return {
      restaurants: [],
    };
  },
  created() {
    var jsonData = {
      //здесь будет запрос на сервер (получить json)
      restaurants: [
        {
          name: "Макдоналдс — Газетный",
          costBaseProducts: "₽₽ • Бургеры",
          cookingTime: "25 - 35 мин",
          urlImg:
            "https://s3-alpha-sig.figma.com/img/5e16/8518/66f1d3abd4940a817c788c541e9fbeb3?Expires=1691366400&Signature=eC8oi8saMcqASsSwCJNBi2VzUnuUQf4zlLZzPdA7jm2ZxOWBaZFtMZiQohms-Y6~FuAWbFy9-K5eqQncZig8~33Cq6ibw94xbSvXfjgx5bhouuXqEjIZToKwSd9xUt2E4iCg-qrTiNhhETwmWfVbM-yzx5ZEddvPraUZrh9MflEIxdd03dYBbLbhJrwN86KZZA4Q70Id7BUNf7RS2CwEdJoiWF5kPcIFS33IBhyFKuOXN4FYLS9VvUlvRurFSaxt67Uol1DbS2V2JNg6w9kxpOP07E6UUBm6Gwu-FWnDqMhjS5RDumzH7n7eOU3HsQHyy8m~7x-zVjPJXXIJ9csGOQ__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
        },
        {
          name: "DimSum & Co — ЦДМ",
          costBaseProducts: "₽ • Японская • Китайская • Азиатская",
          cookingTime: "40 - 50 мин",
          urlImg:
            "https://s3-alpha-sig.figma.com/img/f68f/d639/d6cbe90533884dd7cfe6649222111bfa?Expires=1691366400&Signature=qDTFdsFt2kwb7dUftYj0q0XkE73Y7D6vs50KqRYk8pV-pWOOjdtsEcroSuZz1eeMhioogdjUxue43zFw1kdsieqgCeDh-BfaHd-A1jflHDcGCfEocZc8c7Bi8Nu8QpjP~3tArNoiN3m8tTmXQohwYEWwVqsO9EDjK-Dt-FDbtQ2RtRwono-y4X-etVmJtzzWgKLF8N3D4E31xaElnbfFy0iPhgiZ4ZcR-YC77VCPeLaieWb-JISemry8C0wTYEEdpwLLZ0yqyDVhEJ7BpCvRSAd9-kpCO398GDgqFeB2GjlP2U3kCx1uANU4U~CxOQWrCycHY8AksltWAqmmlKXrWA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
        },
        {
          name: "ДвижОК — Манежная",
          costBaseProducts: "₽ • Американская • Европейская",
          cookingTime: "35 - 45 мин",
          urlImg:
            "https://s3-alpha-sig.figma.com/img/85df/27c2/a074eb38c8ee48f65c4d05cff31d07ae?Expires=1691366400&Signature=R9ti4~-brplKs2hudwlHk1EIMTSgvz77L90BGGg2PVBkwC0~9tdIs-6J-~SDs6lCF8IxuUqNwf22w1rD1-zLzaxVczuGSe89hG5UKU9XgGWjvGzHbF-z-CuW273gPs93k1A7VBGRCAAOoIy6fCLPjyiD-VzyLxMBY8jqbysmOV6IwSnrlKE6L-iDfRvZdOo~lnshHK-vkgacCjry6mDQ1ok~nzRmmY1L4xb5EbGjKQH5hDAnpv3BJKIFcmKLKfzl6hb9B2XDm75VcB7uWfIw-26pz~n95Ny~ZujUxfX9Lar3jBeQdLa116PCjT0ezP4L0af~IBvgczGLQFBOIN21kg__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
        },
        {
          name: "НЯ — NHA",
          costBaseProducts: "₽₽ • Вьетнамская",
          cookingTime: "30 - 40 мин",
          urlImg:
            "https://s3-alpha-sig.figma.com/img/f728/ad2b/b170f9a27e7164c221721bfc87422d65?Expires=1691366400&Signature=Qw9RWYHQOuwhxmpHfwGU-xloKjB8NwmMjoZoVh2nrRD6BP3Fx0Bzui62kzM1ocwqxP1b00ubRtxldwoV2v6pFXMK95XYqL~saX0oLYOkeis9Jm5~Ui84MTJ6r6JYxdYE7kthlPJN8d0fzTa8dBmLlpd8xl-0l8ESBSQeqSCIWhe86O3LMT0eav9xgMtgghXAc6lMVklclMeXnnTmg~h8Ni7YfTqrhTOvG5k80wy9EjvTAB1bmk67k4KWcjKJbNHeL2H3lB4M~mLUYMGVwujM7QwU0ja7htxeBKGYvZ8fKbMXGJLpvpZV1n1j9OXjYuy7GcUcU62DCdnAtXa-qXEHQA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
        },
        {
          name: "Точка Дзы — Цветной",
          costBaseProducts: "₽₽ • Вьетнамская",
          cookingTime: "40 - 50 мин",
          urlImg:
            "https://s3-alpha-sig.figma.com/img/e74c/b08d/e7ec2190e9f85dd38530ebb6f2d7d0d0?Expires=1691366400&Signature=ht5eyBz5ZHSSpdrrric9JVl6Xx48h77nm52O8h-yHqCdU7Zj9sOt2TW3Rx1exniPr1eKiKQ~g-czU9qAYwguK4BcSxIuzdEigsvIU1hZKHbQ7Y--F2MO8tavDXtkipV3XXjfb~03ve7ufFpMRM~paGC~YqzgDVA2Zy3tiGK-~ktuhVChHjItnYwRS8fR5jXkiO1AIaDXI258sv1FqFO5Tz77u8cqxGMEuw14izrl51FtzHwKTmtsv5ZI04MGXlCV1gEfBYcSm8Q1~mEVigbvggY-M-rmc4wYn79mUc8B81CWI2Zv0gK09h6B41F88ThWMPncbLiBiB6DiB25Xycmww__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
        },
        {
          name: "Cinnabon",
          costBaseProducts: "₽ • Выпечка • Десерты • Капкейки",
          cookingTime: "25 - 35 мин",
          urlImg:
            "https://s3-alpha-sig.figma.com/img/5c6b/8fb4/4c21b22e642a13f62c4b2e98649ec2c9?Expires=1691366400&Signature=Lb766O4Dn25hbO96Sf2VB-Q0NNaELWIPgMJi-8eVRLIvp09-Cm9Toa4H3d4dEzapuOUQ6JY9aoUM-N5IRNj9mDuhqxMyJy3hnUsw3K~s~DLNYyGG4d-gLtqefwxtkoiyVoRLCa8oowIEiLtgrafrX1CdDKHfNnFSxKzLOOfhBwY2njPepXiCkNRgC75tc3flUgXIkdo17A8K-vP0rlYi81d4DkPPzROPQhZQEqrQNbCYbI-KjGLHIngxxIdYE75h5UUI61QNrCY1ryawVL8JsJ2jQU2tsiHkWOakMDz7JknHIgda2HlQNsGqm0dBLMB4dvC96ANUC5ceUtkqF2E42g__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
        },
        {
          name: "PIZZELOVE",
          costBaseProducts: "₽₽ • Пицца",
          cookingTime: "15 - 25 мин",
          urlImg:
            "https://s3-alpha-sig.figma.com/img/1c92/c4f6/10ed1555ec1226afbb7ebc94743721e9?Expires=1691366400&Signature=DIBW2dDp605aQVDsTxVlVjiv3hM6tahqY3Qhf1eKQohCCN~LNkoi5aO~Tydrn5TXKI9-BDMY3aSXiHctAKnV3cmzjgnLd4IQ4aW~bRwocWxHNE0EnO2xnMe3Wrh4AJMBJFsCXArxkkAivG0l8BGmibvCzU9DIDrBHVW7fAnJBJcwhAkAdEFWD0mJIaeLOOR-vX7E3Loq-lehMH~kNv8lTKKi20S0Y-P8ZAtJnDe1YbYmKrqWgoJS5G-XaPWy3esM7B3l12ecHAW9kmTEv7mC63VZ3KsLOTScSDhSLx~Le3OcDe7crqNYvucWZZ~XaAitgzW~6RRGwCzW20kp5aUtXg__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
        },
        {
          name: "Zю кафе — Тверская",
          costBaseProducts: "₽₽ • Японская",
          cookingTime: "25 - 35 мин",
          urlImg:
            "https://s3-alpha-sig.figma.com/img/5f57/fa5f/ee56bc8525b3a87273ebcaaef0d7793e?Expires=1691366400&Signature=Fkf9AV1NJuODd5o0Hot3aapdaG0YW0btaffZUQl~YL7z~YbUdxq4stK8uvCJLrBCYXFVQgbyuiwKUvyJ9dn8JitB6Nn-BLysZTXyOZ9aPftLvM2pX3FyX~0Qtw06IaydhiAHDlo8kyYMMzrl4N2DF4c64lb~~Y9BrXULMtZlp-RmqkIrqiBbQTDGHvJzoKiwmSbfyoI5Dwz1JTYWlD9gcjQ3XhBp6lutfcrD0NBkpDKLkU8pdbrR2Khpytq7XBh-P3TxLpDRfo48J7aukGMISZEdhWTgT674g99hYqDeJkQzD3kKYQmyDFraKb9hVOPvHD0iwB0ZhwkCQJ4~Dz~RJw__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
        },
        {
          name: "Bar BQ Cafe — Манежная",
          costBaseProducts: "₽₽₽ • Европейская",
          cookingTime: "30 - 40 мин",
          urlImg:
            "https://s3-alpha-sig.figma.com/img/0b8c/5c46/ca4a31f783e1a79e2b56b3218a4dc177?Expires=1691366400&Signature=oMCxkSHoXtbrlyD7NKtOC2R2mRc1fx-kAq7aQAaiL2iijQN~yCpENTf6ahU99Q-QSGnxB2PYlu4lNukUcXmEYiSiO9yVq4soIXrtdjJwRlMs4Iqzn~BWPkzRBMBarby~s4eUyCe0cblLPpHTiZGfePJtc~iyPe70X6ekU1Mm1jhNfKao6Wp1PV0PkvQM6pwLYie-U35su4PkMC08px~ztFv4ra1XM9yuSHIPB9QDkrVtLLJ3xUzbDifeNYNmlN0h3qgd-DDJA9xl8txlgXdW2q5H4ocx-N5GZqsUR~eci9LbhyX5CtC~hWD00ZFosvHnJXRYSvB8wUO8~mACSe8ezA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4",
        },
      ],
    };
    this.restaurants = jsonData.restaurants;
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=League+Spartan:wght@400;600&family=Roboto&display=swap");

.name-list-restaurant {
  margin-top: 55px;
  color: #1d1d1d;
  font-family: Roboto;
  font-size: 22px;
  font-style: normal;
  font-weight: 400;
  line-height: 34px;
}

@media (min-width: 1199px) {
  .main-container {
    margin-left: 80px;
    margin-right: 80px;
  }
}

@media (max-width: 1199px) {
  .main-container {
    margin-left: 8px;
    margin-right: 8px;
  }
}

.card-restaurant-container {
  margin-top: 20px;
}

.card-restaurant-container {
  margin-top: 20px;
}

.card-restaurant-description {
  margin-top: 15px;
  font-family: Roboto;
}

.name-restaurant {
  color: #1d1d1d;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
}

.cost-BaseProducts-restaurant {
  margin-top: 4px;
  color: #626262;
  font-size: 14px;
  font-weight: 400;
  line-height: 21px;
}

.cooking-time-restaurant {
  margin-top: 4px;
  color: #1d1d1d;
  font-size: 13px;
  font-weight: 400;
  line-height: 21px;
}

.footer-uber-eats {
  margin-top: 80px;
}
</style>
