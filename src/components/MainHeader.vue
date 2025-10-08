<template>
  <header
    id="mainHeader"
    class="
      sticky
      flex flrx-row items-center justify-center
      top-0 left-0 z-10
      bg-gray-900
      text-gray-50
    "
  >
    <h1 class="text-3xl text-gray-50">SUZUKI Yuta's Profile</h1>
  </header>
</template>

<style scoped lang="scss">
@use "@/assets/styles/variables";

#mainHeader {
  height: variables.$headerHeight;
  box-shadow: 0 4px 16px #111;
}
.site-name {
  text-shadow: 0 4px 16px #333;
}
</style>
