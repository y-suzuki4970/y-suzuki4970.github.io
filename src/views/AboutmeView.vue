<script setup lang="ts">
import TopPageViewSection from '@/components/TopPageViewSection.vue';
import CommonArticle from '@/components/CommonArticle.vue';

const javaSe8Url = "https://www.credly.com/badges/b670e76a-788f-4dc6-8a7a-67a5b7fc8476/public_url";
</script>

<template>
  <TopPageViewSection
    en-title="About me"
    ja-title="私について"
    background-image-url="/images/aboutme.jpg"
    background-image-author="Min An"
    background-image-source-link="https://www.pexels.com/ja-jp/photo/1004021/"
  >
    <div
      class="
        container
        mx-auto my-0
        w-4/5 pt-16 pb-4
      "
    >
      <CommonArticle header-text="プロフィール">
        <div>
          <dl class="grid">
            <dt>氏名</dt>
            <dd>鈴木 勇太</dd>
            <dd>すずき ゆうた</dd>
            <dd>SUZUKI Yuta</dd>
            <dt>出身地</dt>
            <dd>北海道札幌市</dd>
            <dd>Sapporo-shi, Hokkaido</dd>
          </dl>
        </div>
        <p
          class="
            profile-p
            mx-auto my-8
            indent-4
          "
        >
          札幌市出身のプログラマーです。大学でITについて学び、主に自治体・公的機関等のシステム開発に携わってきました。
        </p>
      </CommonArticle>
      <CommonArticle header-text="資格">
        <div>
          <dl class="grid">
            <dt>Oracle Certified Java Programmer</dt>
            <dd><a :href="javaSe8Url" target="_blank">Silver SE 8 (JPN)</a></dd>
          </dl>
        </div>
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
.profile-section, .profile-p {
  width: $mainWidth;
  min-width: $minWidth;
}
dl.grid {
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
