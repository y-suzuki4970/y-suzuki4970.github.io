<script setup lang="ts">
import TopPageViewSection from '@/components/TopPageViewSection.vue';
import SkillMeter from '@/components/SkillMeter.vue';
import RatignStars from '@/components/RatignStars.vue';

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
  >
    <div class="container">
      <article>
        <header>
          <h4>各スキルについて</h4>
        </header>
        <section>
          <p>業務で使ったもの・趣味で使っているものについてはこちらも御覧ください。</p>
          <ul class="ul">
            <li><a href="https://stackshare.io/y-suzuki4970/works">stackshare - 業務で使ったスキル</a></li>
            <li><a href="https://stackshare.io/y-suzuki4970/hobby">stackshare - 趣味で使っているスキル</a></li>
          </ul>
        </section>
      </article>
      <template v-for="(skillKind, i) in skillKinds" :key="i">
        <section>
          <header>
            <h4>{{ skillKind.name }}</h4>
          </header>
          <table class="skills-table">
            <thead>
              <tr>
                <th>{{ skillKind.singleName }}</th>
                <th style="min-width: calc(1.375rem * 5)">好き</th>
                <th>自信</th>
              </tr>
            </thead>
            <tbody>
              <template v-for="(skill, j) in skillKind.skills" :key="j">
                <tr>
                  <th>{{ skill.name }}</th>
                  <td><RatignStars :rate="skill.like" :size-in-px="24" /></td>
                  <td><SkillMeter :value="skill.confidence" /></td>
                </tr>
              </template>
            </tbody>
          </table>
        </section>
      </template>
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
section {
  margin: 0 auto;
  width: 80%;
  min-width: 400px;
}

header {
  margin: 0 auto;
  margin-block-start: 1rem;
  margin-block-end: 1rem;
  text-align: center;
}

.ul {
  margin-inline-start: 2rem;
  list-style: none;
}
.skills-table {
  margin-inline-start: 2rem;
  margin: 0 auto;
  th, td {
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
