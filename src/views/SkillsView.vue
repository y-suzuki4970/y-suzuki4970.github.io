<script setup lang="ts">
import TopPageViewSection from '@/components/TopPageViewSection.vue';
import CommonArticle from '@/components/CommonArticle.vue';
import SkillMeter from '@/components/SkillMeter.vue';
import RatingStars from '@/components/RatingStars.vue';

interface Skill {
  name: string;
  like: number;
  confidence: number;
}
interface SkillKind {
  name: string;
  singleName: string;
  skills: Skill[];
}

const skillKinds : SkillKind[] = [
  {
    name: "言語",
    singleName: "言語名",
    skills: [
      { name: "Java", like: 4, confidence: 5 },
      { name: "C#", like: 5, confidence: 4 },
      { name: "VB.NET", like: 4, confidence: 4 },
      { name: "Visual Basic", like: 1, confidence: 3 },
      { name: "JavaScript", like: 5, confidence: 3 },
      { name: "SQL", like: 5, confidence: 3 },
    ]
  },
  {
    name: "フレームワーク",
    singleName: "FW名",
    skills: [
      { name: "Spring Framework", like: 5, confidence: 4 },
      { name: "MyBatis", like: 5, confidence: 4 },
      { name: "ASP.NET", like: 4, confidence: 4 },
      { name: "jQuery", like: 4, confidence: 3 },
    ]
  },
  {
    name: "データベース",
    singleName: "DBMS名",
    skills: [
      { name: "Oracle", like: 4, confidence: 3 },
      { name: "SQL Server", like: 5, confidence: 3 },
      { name: "PostgreSQL", like: 5, confidence: 3 },
    ]
  },
  {
    name: "その他",
    singleName: "名称",
    skills: [
      { name: "HTML LS", like: 4, confidence: 4 },
      { name: "CSS 3", like: 4, confidence: 4 },
      { name: "Access VBA", like: 1, confidence: 4 },
      { name: "Subversion", like: 4, confidence: 3 },
    ]
  },
];

</script>

<template>
  <TopPageViewSection
    en-title="Skills"
    ja-title="スキル一覧"
    background-image-url="/images/skills.jpg"
    background-image-author="Lukas"
    background-image-source-link="https://www.pexels.com/ja-jp/photo/574071/"
  >
    <div
      class="
        container
        mx-auto my-0
        w-4/5 pt-16 pb-4
      "
    >
      <CommonArticle header-text="各スキルについて">
        <section class="w-fit mx-auto">
          <p class="indent-4">ここでは業務で利用した主な言語等について記述します。<br>その他の業務で使ったもの・趣味で使っているものについてはこちらも御覧ください。</p>
          <ul>
            <li>
              <a
                href="https://stackshare.io/y-suzuki4970/works"
                target="_blank"
              >stackshare - 業務で使ったスキル</a>
            </li>
            <li>
              <a
                href="https://stackshare.io/y-suzuki4970/hobby"
                target="_blank"
              >stackshare - 趣味で使っているスキル</a>
            </li>
          </ul>
        </section>
      </CommonArticle>
      <template v-for="(skillKind, i) in skillKinds" :key="i">
        <CommonArticle :header-text="skillKind.name">
          <table class="skills-table">
            <thead>
              <tr>
                <th>{{ skillKind.singleName }}</th>
                <th class="min-w-fit">Like</th>
                <th>自信</th>
              </tr>
            </thead>
            <tbody>
              <template v-for="(skill, j) in skillKind.skills" :key="j">
                <tr>
                  <th>{{ skill.name }}</th>
                  <td><RatingStars :rate="skill.like" /></td>
                  <td><SkillMeter :value="skill.confidence" /></td>
                </tr>
              </template>
            </tbody>
          </table>
        </CommonArticle>
      </template>
      <aside
        class="
          w-fit mx-auto
        "
      >
        <p class="indent-4">ちなみに、このページは個人的に勉強しているVue.js 3で作成しています。いちおう、利用している技術について記述しておきます。</p>
        <ul class="list-disc ml-6">
          <li>Vue.js 3</li>
          <li>TailwindCSS</li>
          <li>SCSS</li>
        </ul>
      </aside>
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
.skills-table {
  border-collapse: separate;
  border-spacing: 1px;
  margin-inline-start: 2rem;
  margin: 0 auto;
  th, td {
    padding: 2px;
    background: #00000044;
  }
  tbody {
    th {
      text-align: left;
    }
    td {
      text-align: center;
    }
  }
}
</style>
