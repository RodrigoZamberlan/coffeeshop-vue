<template>
  <div>
    <div v-if="categoryTab == 'Capuccino'">
      <div class="list-coffee" v-if="allCapuccinos && allCapuccinos.length > 0">
        <Coffee
          v-for="coffee in allCapuccinos"
          :key="coffee.id"
          :img="coffee.img"
          :name="coffee.name"
          :desc="coffee.desc"
          :price="coffee.price"
        />
      </div>
    </div>

    <div v-else-if="categoryTab == 'Espresso'">
      <div class="list-coffee" v-if="allEspressos && allEspressos.length > 0">
        <Coffee
          v-for="coffee in allEspressos"
          :key="coffee.id"
          :img="coffee.img"
          :name="coffee.name"
          :desc="coffee.desc"
          :price="coffee.price"
        />
      </div>
    </div>

    <Special
      img="capuccino-1.jpg"
      name="5 Coffee beans you must try!"
      desc="The world's finest arabica coffee beans are listed by country in no particular order since the biggest factor is personal preference."
    />
  </div>
</template>

<style scoped>
.list-coffee {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  margin-top: 30px;
  gap: 16px;
}

@media only screen and (max-width: 1100px) {
  .list-coffee {
    grid-template-columns: 1fr 1fr;
  }
}

.warning {
  color: white;
  font-size: 20px;
  width: 300px;
  margin: 20px 0 150px;
}
</style>

<script>
import Coffee from "./Coffee";
import Special from "./Special";

export default {
  name: "ListCoffee",
  data() {
    return {
      allLates: [{}],
      allCapuccinos: [
        {
          id: 1,
          name: "Capuccino",
          desc: "With Oak Milk",
          price: "4.20",
          img: "capuccino-1.jpg",
          category: "Capuccino",
        },
        {
          id: 2,
          name: "Capuccino",
          desc: "With Chocolate",
          price: "3.50",
          img: "capuccino-2.jpg",
          category: "Capuccino",
        },
        {
          id: 3,
          name: "Capuccino",
          desc: "With Vanilla",
          price: "3.80",
          img: "capuccino-3.jpg",
          category: "Capuccino",
        },
        {
          id: 4,
          name: "Capuccino",
          desc: "No Sugar",
          price: "3.00",
          img: "capuccino-4.jpg",
          category: "Capuccino",
        },
      ],
      allEspressos: [
        {
          id: 1,
          name: "Espresso",
          desc: "Light Roast",
          price: "2.50",
          img: "espresso-1.png",
          category: "Espresso",
        },
        {
          id: 2,
          name: "Espresso",
          desc: "Medium Roast",
          price: "2.30",
          img: "espresso-3.webp",
          category: "Espresso",
        },
        {
          id: 3,
          name: "Espresso",
          desc: "Dark Roast",
          price: "2.00",
          img: "espresso-2.jpg",
          category: "Espresso",
        },
      ],
    };
  },
  props: {
    categoryTab: String,
  },
  components: {
    Coffee,
    Special,
  },
};
</script>