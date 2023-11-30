<template>
  <div class="hero-section">
    <div class="hero-text">
      <h1>I'm {{ name }}</h1>
      <h3>{{ occupation }}</h3>
      <div class="social-icons">
        <a
          v-for="(link, icon) in socialLinks"
          :key="icon"
          :href="link"
          target="_blank"
        >
          <img
            :src="'src/assets/' + icon + '.png'"
            :alt="icon"
            class="social_icons"
          />
        </a>
      </div>
    </div>
    <img :src="photoSrc" :alt="photoAlt" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Vahid",
      occupation: "Web Developer",
      socialLinks: {
        github: "https://github.com/vidito",
        linkedin: "https://www.linkedin.com/in/vahid-niamadpour",
        youtube: "https://www.youtube.com/pythonology",
        website: "https://www.pythonology.eu",
      },
      photoSrc: "src/assets/vahid.png",
      photoAlt: "Vahid's Photo",
    };
  },
};
</script>

<style scoped>
.hero-section {
  max-width: 1000px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  place-items: center;
  gap: 2rem;
  margin: 0 auto;
}

.hero-text h1 {
  font-weight: 900;
}

.social_icons:hover {
  transition: 0.5s all ease-in-out;
  transform: rotate(1turn);
}

.hero-section img {
  border-radius: 10px; /* Creates a circular shape for the image */
  max-width: 200px; /* Adjust the size as needed */
}
</style>
