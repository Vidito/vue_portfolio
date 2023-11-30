<template>
  <div class="skill-box" @mouseover="showOuter" @mouseleave="hideOuter">
    <img :src="'src/assets/' + logo" :alt="alt" class="icon" />
    <span class="inner">{{ name }}</span>
    <Transition>
      <p class="outer" v-show="isOuterVisible">{{ description }}</p>
    </Transition>
  </div>
</template>

<script>
export default {
  props: {
    logo: String,
    alt: String,
    name: String,
    description: String,
  },
  data() {
    return {
      isOuterVisible: false,
    };
  },
  methods: {
    showOuter() {
      this.isOuterVisible = true;
    },
    hideOuter() {
      this.isOuterVisible = false;
    },
  },
};
</script>

<style scoped>
/* Add your existing styles for .skill-box, .inner, and .outer here */
/* Add styles for the hover effect */
.skill-box {
  text-align: center;
  padding: 20px;
  border: 1px solid #68bbe3;
  border-radius: 8px;
  height: 6rem;
}
.icon {
  vertical-align: middle;
}
.v-leave-from {
  opacity: 1;
}
.v-leave-to {
  opacity: 0.1;
}
.skill-box .outer {
  transition: opacity 0.5s;
}
</style>
