<template>
  <div class="headerContainer">
    <header>
      <img src="src/assets/icon.png" alt="My Logo" />
      <div id="myNav" class="overlay">
        <a href="javascript:void(0)" class="closebtn" onclick="closeNav()"
          >&times;</a
        >
        <div class="overlay-content">
          <h2 class="menu_text">Nothing here</h2>
        </div>
      </div>
      <span class="burger" @click="toggleNav">&#9776;</span>
      <Overlay :isOpen="isNavOpen" @closeNav="closeNav"></Overlay>
    </header>
  </div>
</template>

<script>
import { ref } from "vue";
import Overlay from "./Overlay.vue";

export default {
  components: {
    Overlay,
  },
  data() {
    return {
      isNavOpen: false,
    };
  },
  methods: {
    toggleNav() {
      this.isNavOpen = !this.isNavOpen;
    },
    closeNav() {
      this.isNavOpen = false;
    },
  },
};
</script>
<style scoped>
.headerContainer {
  margin-bottom: 1rem;
  background: rgb(2, 0, 36);
  background: linear-gradient(
    90deg,
    rgba(2, 0, 36, 0.89) 0%,
    rgba(9, 9, 121, 0.96) 35%,
    rgba(6, 81, 168, 0.96) 62%,
    rgba(15, 161, 190, 0.89) 100%
  );
}

header {
  max-width: 1000px;
  color: #fff;
  padding: 15px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

header img {
  height: 50px;
}

/*  Menu Responsive Start */

.burger {
  font-size: 30px;
  cursor: pointer;
  color: #ecf0f2;
}
.overlay {
  height: 0%;
  width: 100%;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background: rgb(2, 0, 36);
  background: linear-gradient(
    90deg,
    rgba(2, 0, 36, 0.89) 0%,
    rgba(9, 9, 121, 0.96) 35%,
    rgba(6, 81, 168, 0.96) 62%,
    rgba(15, 161, 190, 0.89) 100%
  );
  overflow-y: hidden;
  transition: 0.5s;
}

.menu_text {
  color: #dccfcf;
  font-size: 3rem;
}

.overlay-content {
  position: relative;
  top: 25%;
  width: 100%;
  text-align: center;
  margin-top: 30px;
}

.overlay a {
  padding: 8px;
  text-decoration: none;
  font-size: 36px;
  color: #dccfcf;
  display: block;
  transition: 0.3s;
}

.overlay a:hover,
.overlay a:focus {
  color: rgb(123, 123, 182);
}

.overlay .closebtn {
  position: absolute;
  top: 20px;
  right: 45px;
  font-size: 60px;
}

@media screen and (max-height: 450px) {
  .overlay {
    overflow-y: auto;
  }
  .overlay a {
    font-size: 20px;
  }
  .overlay .closebtn {
    font-size: 40px;
    top: 15px;
    right: 35px;
  }
}

/*  Menu Responsive End */
</style>
