<template>
  <div class="coffee-wrapper">
    <img class="img" :src="`assets/${img}`" alt="Image of the coffee" />
    <h2 class="name">{{ name }}</h2>
    <p class="description">{{ desc }}</p>

    <div class="wrapper-price">
      <p class="price"><span>$ </span>{{ price }}</p>

      <button class="add">+</button>
    </div>
  </div>
</template>

<style>
.coffee-wrapper {
  width: 100%;
  height: 270px;
  padding: 14px;
  border-radius: 35px;
  background: rgb(20, 25, 33);
  background: linear-gradient(
    130deg,
    rgba(20, 25, 33, 1) 0%,
    rgb(41, 41, 41) 30%,
    rgba(12, 16, 21, 1) 100%
  );
  box-sizing: border-box;
  transition: all ease 1s;
  margin-bottom: 10px;
}

.coffee-wrapper .img {
  width: 100%;
  margin-bottom: 8px;
  border-radius: 25px;
  height: 140px;
  object-fit: cover;

  /* -webkit-box-shadow: 0px 10px 13px -7px #d17844,
    5px 5px 15px 5px rgba(209, 120, 68, 0);
  box-shadow: 0px 10px 13px -7px #d17844, 5px 5px 15px 5px rgba(209, 120, 68, 0); */
}

.coffee-wrapper:hover {
  opacity: 1;
  filter: blur(0);
}
.coffee-wrapper .name {
  color: white;
  font-family: "Nunito";
  font-size: 18px;
  font-weight: 700;
  padding-bottom: 4px;
}

.coffee-wrapper .description {
  font-family: "Nunito";
  font-weight: 300;
  color: white;
  font-size: 14px;
}

.coffee-wrapper .wrapper-price {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
}

.coffee-wrapper .wrapper-price .add {
  width: 30px;
  height: 30px;
  background: #d17844;
  border: none;
  border-radius: 11px;
  color: white;
  font-weight: 900;
  font-family: "Nunito";
  font-size: 20px;
  text-align: center;
  padding-bottom: 2px;
  cursor: pointer;
}

.coffee-wrapper .wrapper-price .price {
  margin-top: 16px;
  color: white;
  font-family: "Nunito";
  font-weight: 700;
  font-size: 18px;
}

.coffee-wrapper .wrapper-price .price span {
  color: #d17844;
}
</style>

<script>
export default {
  name: "Coffee",
  props: {
    name: String,
    desc: String,
    price: String,
    img: String,
    category: String,
  },
};
</script>