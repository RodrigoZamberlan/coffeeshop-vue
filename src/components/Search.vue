<template>
  <form id="frmSearch">
    <input type="text" placeholder="Find your coffee..." />
    <button type="submit">
      <div class="line"></div>
      <div class="circle"></div>
    </button>
  </form>
</template>

<style scoped>
#frmSearch {
  position: relative;
  height: 27px;
  margin: auto;
  box-sizing: content-box;
}

#frmSearch input {
  display: block;
  border: 0;
  background: #141921;
  border-radius: 10px;
  height: 48px;
  width: 100%;
  box-sizing: border-box;
  padding-left: 16px;
  color: white;
  font-family: "Nunito";
  font-weight: 700;
  outline: none;
  text-decoration: none;
}

#frmSearch input::placeholder {
  color: #52555b;
  font-family: "Nunito";
  font-weight: 700;
}

#frmSearch button {
  position: absolute;
  top: 8px;
  right: 20px;
  height: 100%;
  background: none;
  width: 27px;
  height: 27px;
  border: none;
}

#frmSearch button .circle {
  content: "";
  position: absolute;
  top: 6px;
  left: 0;
  width: 14px;
  height: 14px;
  background: #52555b;
  border-radius: 50%;
}

#frmSearch button .line {
  transform: rotate(-45deg);
  width: 7px;
  height: 4px;
  background: #52555b;
  margin: 0 0 0 0;
  border-radius: 4px;
  bottom: 4px;
  left: -5px;
  position: absolute;
}
</style>

<script>
export default {
  name: "Search",
};
</script>