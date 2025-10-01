<script setup lang="ts">
import TopPageViewSection from '@/components/TopPageViewSection.vue';
import CommonArticle from '@/components/CommonArticle.vue';
</script>

<template>
  <TopPageViewSection
    en-title="Contacts and Links"
    ja-title="連絡先とリンク"
    background-image-url="/images/contact.jpg"
    background-image-author="Terje Sollie"
    background-image-source-link="https://www.pexels.com/ja-jp/photo/i-phone-336948/"
  >
    <div
      class="
        container
        mx-auto my-0 mt-16 mb-4
      "
    >
      <CommonArticle header-text="Email">
        <p class="text-center">y.suzuki4970 (gmail.com)</p>
      </CommonArticle>
      <CommonArticle header-text="GitHub">
        <p class="text-center">
          <a
            href="https://github.com/y-suzuki4970"
            target="_blank"
          >https://github.com/y-suzuki4970</a>
        </p>
      </CommonArticle>
    </div>
  </TopPageViewSection>
</template>

<style scoped lang="scss">
@import "@/assets/styles/variables.scss";

.container {
  width: $mainWidth;
  min-width: $minWidth;
}
.contact-header {
  margin: 0 auto;
  margin-block-start: 1rem;
  margin-block-end: 1rem;
  text-align: center;
}
article {
  margin: 0 auto;
  width: 75%;
  min-width: 320px;
  section {
    margin-inline-start: 2rem;
  }
}
</style>
