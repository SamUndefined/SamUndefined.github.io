<template>
  <section id="app">
    <div class="columns is-marginless">
      <app-menu class="column is-one-fifth is-one-quarter-tablet"/>
      <router-view class="section column"/>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import AppMenu from './components/Menu.vue'

@Component({
  components: {
    AppMenu,
  },
})
export default class App extends Vue {
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
@media screen and (min-width: 1024px) {
    .margin-5-is-desktop {
        margin-left: 5rem;
    }
}
</style>
