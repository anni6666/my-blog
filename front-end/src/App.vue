<!--
 * @Date: 2025-02-13 23:00:28
 * @LastEditors: Aregene
 * @LastEditTime: 2025-02-14 12:52:11
-->

<!--  App.vue  -->

<template>
  <a-layout style="min-height: 100vh">
    <NavHeader />
    <IntroComponent />
    <IntroSection />
    <SquarespaceSection />
    <ProjectShowcase />
    <BlogShowcase />
    <InstagramFeed />
    <FooterComponent />
    <MyFooter/>
  </a-layout>
</template>

<script>
import NavHeader from "./components/home/Header.vue";
import IntroComponent from "./components/home/SelfIntroduction1.vue";
import IntroSection from "./components/home/SelfIntroduction2.vue";
import SquarespaceSection from "./components/home/RecipeCollection.vue";
import ProjectShowcase from "./components/home/SportDisplay.vue";
import BlogShowcase from "./components/home/TravelDisplay.vue";
import InstagramFeed from './components/home/EnvironmentalDisplay.vue';
import FooterComponent from './components/home/MyContact.vue';
import MyFooter from './components/home/MyFooter.vue'

export default {
  name: "App",
  components: {
    NavHeader,
    IntroComponent,
    IntroSection,
    SquarespaceSection,
    ProjectShowcase,
    BlogShowcase,
    InstagramFeed,
    FooterComponent,
    MyFooter
  },
};
</script>

<style>
/* 你可以在这里添加全局样式来保持整体风格的一致性 */
body {
  font-family: "Arial", sans-serif;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

/* 为Sidebar添加一些右外边距 */
.ant-layout-sider {
  margin-right: 16px;
}

/* 如果你希望在内容区域周围添加更多的内边距，可以在这里调整 */
.ant-layout-content {
  padding: 24px;
}
</style>
