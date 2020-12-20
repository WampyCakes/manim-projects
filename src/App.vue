<template>
  <header class="border-bottom border-dark mb-4">
      <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <a class="navbar-brand" draggable="False" href="https://www.manim.community/">
          <img
            draggable="False"
            src="./assets/manim-logo.svg"
            width="60"
            height="60"
            alt="Manim Community Logo"
            loading="lazy"
          />
          Manim Community
        </a>
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#social"
          aria-controls="social"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="social">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a
                href="https://docs.manim.community"
                class="nav-link"
                target="_blank"
                rel="noopener noreferrer"
                ><button type="button" class="btn btn-outline-light">
                  <i class="fas fa-book"></i> Documentation
                </button></a
              >
            </li>
            <li class="nav-item">
              <a
                href="https://github.com/ManimCommunity/manim"
                class="nav-link"
                target="_blank"
                rel="noopener noreferrer"
                ><button type="button" class="btn btn-outline-light">
                  <i class="fab fa-github"></i> GitHub
                </button></a
              >
            </li>
            <li class="nav-item">
              <a
                href="https://twitter.com/manim_community/"
                class="nav-link"
                target="_blank"
                rel="noopener noreferrer"
                ><button type="button" class="btn btn-outline-light">
                  <i class="fab fa-twitter"></i> Twitter
                </button></a
              >
            </li>
            <li class="nav-item">
              <a
                href="https://discord.gg/mMRrZQW"
                class="nav-link"
                target="_blank"
                rel="noopener noreferrer"
                ><button type="button" class="btn btn-outline-light">
                  <i class="fab fa-discord"></i> Discord
                </button></a
              >
            </li>
            <li class="nav-item">
              <a
                href="https://www.reddit.com/r/manim/"
                class="nav-link"
                target="_blank"
                rel="noopener noreferrer"
                ><button type="button" class="btn btn-outline-light">
                  <i class="fab fa-reddit"></i> Reddit
                </button></a
              >
            </li>
          </ul>
        </div>
      </nav>
    </header>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <projects msg="Welcome to Your Vue.js App"/>
</template>

<script>
import Projects from './components/Projects.vue'

export default {
  name: 'App',
  components: {
    Projects
  }
}
</script>
<style>
/* @import '../node_modules/bootstrap/dist/css/bootstrap.min.css';
@import './main.css'; */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
