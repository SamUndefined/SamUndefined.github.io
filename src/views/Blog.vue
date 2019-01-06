<template>
    <div class="blog content columns">
        <div class="column is-three-quarters margin-5-is-desktop">
            <h1>Hello blog</h1>
            <p class="date-posted has-text-grey">January 6th, 2019</p>
            <br>
            <vue-markdown>
    This is my first (sort of) blog post and the start of the blog itself!

    This is not the first blog I've built - many framework/stack tutorials are centered around writing basic blogs. I decided to build it manually rather than using another service, though, for a few reasons:

    1) It's fun
    2) It showcases some of my skills
    3) I can customize it however I want
    4) Hosting it myself allows me to learn, which is one of my favorite things. 

    In the future, I plan to add more capabilities to this blog - including comments, some form of clap system, and possibly replies to comments as well. 

    Anyway, this is just a little intro post. Later I'll write some actual blogs of varying lengths and this page will be dedicated to previewing posts. 
            </vue-markdown>
        </div>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import VueMarkdown from 'vue-markdown'

@Component({
    components: {
        VueMarkdown
    }
})
export default class Blog extends Vue {
}
</script>

<style>
.blog * {
    font-family: Arial, Helvetica, sans-serif;
}
.date-posted {
    font-size: 0.75rem;
    margin-top: -1rem;
}
</style>

