<template>
  <div class="sidebar is-hidden-mobile">
    <div class="menu">
      <br>
      <article class="media">
        <figure class="media-content">
          <p class="image profile">
            <img class="is-round" src="../assets/profile.jpg" :title="name" :alt="name">
          </p>
        </figure>
      </article>
      <p class="title is-5 name has-text-centered">{{ name }}</p>
      <p class="subtitle overview has-text-centered">
        Software engineer | Making information accessible to all.
      </p>
      <ul class="menu-list">
        <li><a>Home</a></li>
        <li><a>Blog</a></li>
        <li>
          <a @click="toggleShowProjects" class="is-info">
            <b-icon
                :icon="projectsIndicator"
                size="is-small">
            </b-icon>
            Projects
          </a>
          <ul :hidden="projectsHidden">
            <li><a>Web</a></li>
            <li><a>Mobile</a></li>
            <li><a>Games</a></li>
          </ul>
        </li>
        <li><a>Contact</a></li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class Menu extends Vue {
  @Prop() private msg!: string
  projectsHidden = true

  get name () {
    return 'Sam Wolstencroft'
  }

  get projectsIndicator () {
    return this.projectsHidden ? 'chevron-right' : 'chevron-down'
  }

  toggleShowProjects () {
    this.projectsHidden = !this.projectsHidden 
  }
}
</script>

<style lang="scss" scoped>
.sidebar {
  background-color: #24373a;
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  height: 100vh;
}
.sidebar * {
  color: lightgrey;
}
.profile {
  width: 70%;
  height: 70%;
  margin: auto;
}
.is-round {
  border-radius: 100%;
}
.name {
  margin: 1rem 0;
}
.overview {
  font-family: Arial, sans-serif;
  font-size: 0.9rem;
  color: gray;
  padding-top: 0.5rem;
}
.menu-item {
  padding-left: 0.75rem;
}
</style>
