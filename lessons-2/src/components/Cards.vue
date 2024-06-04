<template>
  <div class="cards">
    <ul v-for="card in arrayCards" :key="card.name">
      <li>
        <img :src="card.src" :alt="card.alt" width="300" />
        <h2>{{ card.name }}</h2>
        ,
        <h3>{{ card.age }}</h3>
      </li>
    </ul>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "Cards",
  components: {},
  setup() {
    const arrayCards = [
      {
        name: "user1",
        age: "12",
        src: "https://scontent-iev1-1.xx.fbcdn.net/v/t39.30808-6/447776835_7819465388119314_6220546355758555735_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5f2048&_nc_ohc=clXKuGX_jJoQ7kNvgEn9JfR&_nc_ht=scontent-iev1-1.xx&oh=00_AYC6iZKz8JXzs0f9NdueiIpP2IX3GmlO8e2WXl2JFurpWQ&oe=66652A11",
        alt: "kat-1",
      },
      {
        name: "user2",
        age: "16",
        src: "https://scontent-iev1-1.xx.fbcdn.net/v/t39.30808-6/447779706_7819466411452545_7688509755729886839_n.jpg?_nc_cat=104&ccb=1-7&_nc_sid=5f2048&_nc_ohc=EO9VV2MZU7cQ7kNvgEltopJ&_nc_ht=scontent-iev1-1.xx&oh=00_AYD32MFImXKqmcAQtjCy_8ausUS-ct_ZhgjMUdDIIdt69w&oe=66652251",
        alt: "kat-2",
      },
      {
        name: "user3",
        age: "2",
        src: "https://scontent-iev1-1.xx.fbcdn.net/v/t39.30808-6/447306755_7819466338119219_1016513726257455931_n.jpg?_nc_cat=102&ccb=1-7&_nc_sid=5f2048&_nc_ohc=VekWtH97mjsQ7kNvgEhlAyL&_nc_ht=scontent-iev1-1.xx&oh=00_AYDQsAV3NfaNkYDfCqVb9H7eJloRnuQnCIia0qFqveFbbQ&oe=6664FAED",
        alt: "kat-3",
      },
      {
        name: "user4",
        age: "1",
        src: "https://scontent-iev1-1.xx.fbcdn.net/v/t39.30808-6/447777565_7819466431452543_1252825776529953015_n.jpg?_nc_cat=111&ccb=1-7&_nc_sid=5f2048&_nc_ohc=wnNpV4bwdQsQ7kNvgFcruH2&_nc_ht=scontent-iev1-1.xx&oh=00_AYAUju-jtOJqWKKlTHH5z0zHE_T0t_Y2OD2yWMdRHSUEtA&oe=66650D9E",
        alt: "kat-4",
      },
    ];

    return {
      arrayCards,
    };
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style></style>
