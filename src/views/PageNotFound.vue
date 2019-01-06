<template>
    <div class="content columns">
        <img class="jedi column" src="../assets/ben_kenobi.png" title="Ben Kenobi" alt="Ben Kenobi">
        <div class="column">
            <div class="huge">404</div>
            <p class="title not-as-huge">This is not the page you are looking for.</p>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
.huge {
    font-size: 8rem;
}
.not-as-huge {
    font-weight: 100;
}
.jedi {
    width: 50%;
    height: 50%;
    max-width: 350px;
    max-height: 350px;
}
@media screen and (max-width: 1024px) {
    .jedi {
        display: block;
        margin: 0 auto;
    }
    .huge {
        font-size: 5rem;
    }
    .huge, .title {
        text-align: center;
    }
}
</style>
