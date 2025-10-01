<script setup lang="ts">
import MainHeader from "./components/MainHeader.vue";
import ViewSeparator from "./components/ViewSeparator.vue";
import MainFooter from "./components/MainFooter.vue";
import TopView from "./views/TopView.vue";
import ProfileView from "./views/AboutmeView.vue";
import SkillsView from "./views/SkillsView.vue";
import ContactView from "./views/ContactView.vue";
</script>

<template>
  <MainHeader />
  <div class="views">
    <TopView />
    <ViewSeparator />
    <ProfileView />
    <ViewSeparator />
    <SkillsView />
    <ViewSeparator />
    <ContactView />
    <MainFooter />
  </div>
</template>
