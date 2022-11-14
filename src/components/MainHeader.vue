<template>
  <header id="mainHeader">
    <h1 class="site-name">SUZUKI Yuta's Profile</h1>
  </header>
</template>

<style scoped lang="scss">
@import "@/assets/styles/variables.scss";

#mainHeader {
  position: sticky;
  display: flex;
  flex-flow: row;
  align-items: center;
  justify-content: center;
  background-color: #000;
  color: #eee;
  top: 0;
  left: 0;
  height: $headerHeight;
  z-index: 9;
  box-shadow: 0 4px 16px #000;
}
.site-name {
  font-size: 2rem;
  color: #eee;
  text-shadow: 0 4px 16px #333;
}
</style>
