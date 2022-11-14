<template>
  <section class="view-separator">
    <p>&nbsp;</p>
  </section>
</template>

<style scoped lang="scss">
@import "@/assets/styles/variables.scss";

.view-separator {
  position: static;
  display: flex;
  top: 0;
  left: 0;
  height: 2px;
  width: 100%;
  background-color: transparent;
  p {
    height: 2px;
    width: 100%;
    background-color: #fff;
    box-shadow: 0 0 24px #fff;
  }
}
</style>
