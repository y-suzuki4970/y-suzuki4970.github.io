<script setup lang="ts">
import TopPageViewSection from '@/components/TopPageViewSection.vue';

const javaSe8Url = "https://www.credly.com/badges/b670e76a-788f-4dc6-8a7a-67a5b7fc8476/public_url";
</script>

<template>
  <TopPageViewSection
    en-title="About me"
    ja-title="私について"
    background-image-url="/images/aboutme.jpg"
  >
    <div class="container">
      <section>
        <header>
          <h3>プロフィール</h3>
        </header>
        <div>
          <dl>
            <dt>氏名</dt>
            <dd>鈴木 勇太</dd>
            <dd>すずき ゆうた</dd>
            <dd>SUZUKI Yuta</dd>
            <dt>出身地</dt>
            <dd>北海道札幌市</dd>
            <dd>Sapporo-shi, Hokkaido</dd>
          </dl>
        </div>
        <p>札幌市出身のプログラマーです。大学でITについて学び、主に自治体・公的機関等のシステム開発に携わってきました。</p>
      </section>
      <section>
        <header>
          <h3>Certifications</h3>
        </header>
        <div>
          <dl>
            <dt>Oracle Certified Java Programmer</dt>
            <dd><a :href="javaSe8Url" target="_blank">Silver SE 8 (JPN)</a></dd>
          </dl>
        </div>
      </section>
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
section, p {
  margin: 0 auto;
  width: $mainWidth;
  min-width: $minWidth;
}
dl {
  display: grid;
  dt {
    grid-column: 1;
    font-weight: bold;
    text-align: right;
    margin-inline-end: 1rem;
  }
  dd {
    grid-column: 2;
    white-space: nowrap;
  }
}
</style>
