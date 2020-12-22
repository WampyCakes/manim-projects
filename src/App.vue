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
          <ul class="navbar-nav" style="display: flex; align-items: center">
            <li class="nav-item">
              <a
                href="https://docs.manim.community"
                class="nav-link"
                target="_blank"
                rel="noopener noreferrer"
                ><button type="button" class="btn btn-outline-light">
                  <strong>Documentation</strong>
                </button></a
              >
            </li>
            <a
            href="https://github.com/WampyCakes/manim-projects"
            class="nav-link"
            rel="noopener noreferrer"
            style="float: right"
            >
            <button type="button" class="btn btn-outline-light">
              <strong>Submit Your Manim Project</strong>
            </button>
            </a>
          </ul>
        </div>
        <li class="nav-item">
              <a
                href="https://github.com/ManimCommunity/manim"
                class="nav-link"
                target="_blank"
                ><img class="hover-social" height="48" width="48" style="margin-top:-2px" draggable="false" src="./assets/github-logo.svg">
                <!-- <button type="button" class="btn btn-outline-light">
                </button> -->
                </a
              >
            </li>
            <li class="nav-item">
              <a
                href="https://twitter.com/manim_community/"
                class="nav-link"
                target="_blank"
                rel="noopener noreferrer"
                ><img class="hover-social" height="48" width="48" draggable="false" src="./assets/twitter-logo.svg">
                <!-- <button type="button" class="btn btn-outline-light">
                </button> -->
                </a
              >
            </li>
            <li class="nav-item">
              <a
                href="https://www.reddit.com/r/manim/"
                class="nav-link"
                target="_blank"
                rel="noopener noreferrer"
                >
                <img class="hover-social" height="48" width="48" draggable="false" src="./assets/reddit-logo.png">
                <!-- <button type="button" class="btn btn-outline-light">
                </button> -->
                </a
              >
            </li>
            <li class="nav-item">
              <a
                href="https://discord.gg/mMRrZQW"
                class="nav-link"
                target="_blank"
                rel="noopener noreferrer"
                ><img class="hover-social" height="60" width="60" style="margin-top:2px; margin-left: -4px;" draggable="false" src="./assets/discord-logo.svg">
                <!-- <button type="button" class="btn btn-outline-light">
                </button> -->
                </a
              >
            </li>
      </nav>
    </header>
  <projects/>
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
