<template>
  <div class="hello">
    <div class="container-fluid">
      <div v-for="item in grid" class="row flex-md-row mb-4 h-md-250 position-relative" v-bind:key="item">
        <div v-for="project in item" class="col border rounded shadow-lg p-4 d-flex flex-column position-static m-2" v-bind:key="project">
          <div class="container-fluid pl-0">
            <strong v-for="tag in project.tags" v-bind:key="tag" style="border: 3px solid; color: #fff; border-radius: .9rem; padding: 3px; margin: 3px; float: left" 
            v-bind:style="{background: colors[project.tags.indexOf(tag)], borderColor: colors[project.tags.indexOf(tag)]}">
            {{ tag }}
            </strong>
          </div>
          <strong class="m-3 text-wrap" style="font-size: 20px; color: #000; font-style: italic">{{ project.title }}</strong>
          <strong class="mb-3 text-left">By <p class="d-inline" v-if="project.author == ''">Anonymous</p> {{ project.author }}</strong>
          <div class="embed-responsive embed-responsive-16by9">
            <iframe class="embed-responsive-item" v-bind:src="project.video_url" allowfullscreen></iframe>
          </div>
          <p class="mb-auto py-3 ml-5 text-left">{{ project.description }}</p>
          <div>
            <p tabindex="0" class="btn btn-outline-light hover-card mt-3 d-flex" style="align-items: center; height: 58px; background: white; color: black; float: left"
            data-trigger="focus" data-toggle="popover" data-placement="right" v-bind:data-content="[project.subfields.length === 0 ? 'No subfields listed' : project.
            subfields.join(', ')]">{{ project.fields.join(', ') }} ❯ </p>
            <a class="" v-if="project.repository !== ''" v-bind:href="project.repository">
              <button type="button" class="btn btn-outline-light hover-card mt-3" style="background: white; color: black; float: right">
                Video source code available on GitHub <img height="45" width="45" draggable="false" src="../assets/github-logo.svg">
              </button>
            </a>
          </div>
        </div>
        <div v-if="item.length == 1" class="col m-2"></div>
      </div>
    </div>
  </div>
</template>

<script>
import json from '.././assets/data.json'
const _ = require("lodash")
export default {
  name: 'Projects',
  props: {
    msg: String
  },
  data() {
    return{
      data: json
    }
  },
  computed: {
    grid() {
      return _.chunk(this.data, 2)
    },
    colors() {
      return ["#81b29a", "#454866", "#e07a5f"]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
