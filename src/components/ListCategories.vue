<template>
  <div class="wrapper">
    <div class="list-wrapper">
      <div class="mask"></div>
      <ol class="list">
        <li class="item-list active" @click="handleClick">Capuccino</li>
        <li class="item-list" @click="handleClick">Espresso</li>
        <li class="item-list" @click="handleClick">Latte</li>
        <li class="item-list" @click="handleClick">Flat White</li>
        <li class="item-list" @click="handleClick">Iced Coffee</li>
        <li class="item-list" @click="handleClick">Cold Brew</li>
        <li class="item-list" @click="handleClick">Alcoholic</li>
      </ol>
    </div>

    <ListCoffee :categoryTab="categoryTab" />
  </div>
</template>

<style lang="css" scoped>
.list-wrapper {
  position: relative;
  height: 110px;
  overflow: overlay;
}

.list-wrapper::-webkit-scrollbar {
  display: none;
}

.wrapper {
  position: relative;
  width: 100%;
}

.wrapper .mask {
  position: absolute;
  z-index: 2;
  right: 0;
  bottom: 0;
  width: 20%;
  height: 60px;
  background: linear-gradient(
    to left,
    rgba(12, 16, 21, 1) 7%,
    rgba(0, 0, 0, 0)
  );
}

.list {
  display: flex;
  gap: 30px;
  margin-top: 60px;
  min-width: max-content;
}

.list li {
  color: #52555b;
  font-family: "Nunito";
  font-weight: 700;
  position: relative;
  cursor: pointer;
  transition: all ease 0.5s;
}

.list li.active {
  color: #d17844;
}

.list li.active::after {
  background: #d17844;
  content: "";
  width: 6px;
  height: 6px;
  position: absolute;
  bottom: -10px;
  left: 0;
  right: 0;
  margin: auto;
  border-radius: 50%;
}
</style>

<script>
import ListCoffee from "./ListCoffee";

export default {
  name: "ListCategories",
  components: {
    ListCoffee,
  },
  data() {
    return {
      categoryTab: "Capuccino",
    };
  },
  methods: {
    handleClick: function (event) {
      var listMenus = document.getElementsByClassName("item-list");
      for (let item of listMenus) {
        item.classList.remove("active");
      }
      event.target.classList.add("active");
      this.categoryTab = event.target.textContent;
    },
  },
};
</script>