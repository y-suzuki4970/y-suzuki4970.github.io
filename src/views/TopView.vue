<script setup lang="ts">
import TopPageViewSection from '@/components/TopPageViewSection.vue';
</script>

<template>
  <TopPageViewSection
    background-image-url="/images/top-view.jpg"
    background-image-name="神田明神 (2017年)"
    background-image-author="SUZUKI Yuta"
  >
    <div
      class="
        container
        relative
        w-full h-screen
        mx-auto my-0
        pt-4 pb-4
      "
    >
      <div
        class="
          m-auto
          text-5xl text-center
        "
      >
        <p class="my-16">Welcome!</p>
        <p class="text-xl">ここはうまれたてのページです。</p>
        <p class="text-xl">まだ見にくい部分もあるかもしれませんが、ご容赦ください。</p>
      </div>
      <div
        class="
          absolute bottom-24 left-1/2 -translate-x-1/2
          text-lg text-center
        "
      >
        <p class="mb-4 text-lg">スクロールして続きを表示してください！</p>
        <p class="flex justify-center">
          <svg
            class="
              icon
              w-12
            "
            viewBox="0 0 24 24"
          >
            <path fill="currentColor" d="M9.9,21V11L6.7,12.69L6.5,12.72C6.19,12.72 5.93,12.6 5.74,12.4L5,11.63L9.9,7.43C10.16,7.16 10.5,7 10.9,7H17.4C18.17,7 18.9,7.7 18.9,8.5V12.86C18.9,13.47 18.55,14 18.05,14.2L13.11,16.4L11.9,16.53V21A1,1 0 0,1 10.9,22A1,1 0 0,1 9.9,21M18.9,5H10.9V2H18.9V5Z" />
          </svg>
        </p>
      </div>
    </div>
  </TopPageViewSection>
</template>

<style scoped lang="scss">
@import "@/assets/styles/variables.scss";

.container {
  min-width: $minWidth;
}
.contents {
  transform: translateY(-50%) translateX(-50%);
}

@keyframes pointer-anime {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(25%);
  }
  100% {
    transform: translateY(0);
  }
}

.icon {
  filter: drop-shadow(2px 2px 2px #eee) drop-shadow(-1px -1px 2px #eee);
  animation-name: pointer-anime;
  animation-duration: 1s;
  animation-iteration-count: infinite;
}
</style>
