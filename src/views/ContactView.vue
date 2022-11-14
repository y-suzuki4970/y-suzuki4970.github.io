<script setup lang="ts">
import TopPageViewSection from '@/components/TopPageViewSection.vue';
</script>

<template>
  <TopPageViewSection
    en-title="Contacts and Links"
    ja-title="連絡先とリンク"
    background-image-url="/images/contact.jpg"
  >
    <div class="container">
      <article>
        <header>
          <h3>Email</h3>
        </header>
        <section>
          <p>y.suzuki4970 (gmail.com)</p>
        </section>
      </article>
      <article>
        <header>
          <h3>GitHub</h3>
        </header>
        <section>
          <p><a href="https://github.com/y-suzuki4970">https://github.com/y-suzuki4970</a></p>
        </section>
      </article>
    </div>
  </TopPageViewSection>
</template>

<style scoped lang="scss">
@import "@/assets/styles/variables.scss";

.container {
  margin: 0 auto;
  padding-block-start: 4rem;
  padding-block-end: 1rem;
  width: $mainWidth;
  min-width: $minWidth;
}
header {
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
