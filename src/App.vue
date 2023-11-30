<template>
  <div>
    <HeaderSection @openNav="openNav" />
    <main>
      <HeroSection />
      <SkillsSection />
    </main>
    <footer>
      <p>Made using Vue.js &copy; {{ currentYear }}</p>
    </footer>
  </div>
</template>

<script>
import HeaderSection from "./components/HeaderSection.vue";
import HeroSection from "./components/HeroSection.vue";
import SkillsSection from "./components/SkillsSection.vue";
export default {
  components: {
    HeaderSection,
    HeroSection,
    SkillsSection,
  },
  data() {
    return {
      currentYear: new Date().getFullYear(),
    };
  },
  methods: {
    openNav() {
      // Implement your logic here
    },
  },
};
</script>

<style scoped>
footer {
  background: rgb(2, 0, 36);
  background: linear-gradient(
    90deg,
    rgba(2, 0, 36, 0.89) 0%,
    rgba(9, 9, 121, 0.96) 35%,
    rgba(6, 81, 168, 0.96) 62%,
    rgba(15, 161, 190, 0.89) 100%
  );
  margin-top: 1rem;
  padding: 20px;
  text-align: center;
}

footer a,
footer h3,
footer p {
  color: #ecf0f2;
  text-decoration: none;
}
</style>
