<template>
  <div id="special-coffee">
    <h2 class="title-special">Special for today</h2>
    <div class="coffee-wrapper">
      <img class="img" :src="`assets/${img}`" alt="Capuccino" />
      <div class="wrapper-text">
        <h2 class="name">{{ name }}</h2>
        <p class="description">{{ resumeDesc }}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
#special-coffee .coffee-wrapper {
  width: 100%;
  display: flex;
  justify-content: space-between;
  padding-right: 28px;
  height: auto;
}

#special-coffee .coffee-wrapper img {
  max-width: 43%;
  margin-bottom: 0;
}

#special-coffee .coffee-wrapper .wrapper-text {
  max-width: calc(100% - 43% - 20px);
}

#special-coffee .title-special {
  color: white;
  padding: 48px 0 16px;
}

#special-coffee .description {
  margin-top: 8px;
  height: 80px;
  overflow: hidden;
}
</style>

<script>
export default {
  name: "Special",
  data() {
    return {
      resumeDesc: this.desc,
    };
  },
  props: {
    img: String,
    name: String,
    desc: String,
  },
  created: function () {
    this.resumeDesc = this.desc.substr(0, 84) + "...";
  },
};
</script>