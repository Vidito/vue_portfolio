<template>
  <div class="skills-section">
    <SkillBox
      logo="html.png"
      alt="html logo"
      name="HTML"
      description="Vanilla HTML"
    />
    <SkillBox
      logo="css.png"
      alt="css logo"
      name="CSS"
      description="Bootstrap, MaterializeCSS"
    />
    <SkillBox
      logo="js.png"
      alt="javascript logo"
      name="JavaScript"
      description="A little React and Vue"
    />
    <SkillBox
      logo="python.png"
      alt="python logo"
      name="Python"
      description="Django and Pandas and NLP"
    />
  </div>
</template>

<script>
import SkillBox from "./SkillBox.vue"; // Create a separate component for SkillBox

export default {
  components: {
    SkillBox,
  },
};
</script>

<style scoped>
.skills-section {
  max-width: 1000px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
  margin: 3rem auto;
  margin-bottom: 0;
}
</style>
