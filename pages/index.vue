<template>
  <div class="index">
    <topnav />

    <p class="text">Drop some <span>&#128077;</span></p>
    <button v-on:click="likeThis">Like</button>

    <p>The page has {{ like }}<span>&#128077;</span></p>
    <div class="middel-div">This div is in the middle</div>
    <div class="middel-flex">This flex is in the middle</div>
    <div class="middel-grid">This grid is in the middle</div>
  </div>
</template>

<script>
import topnav from '@/components/levi/topnav.vue'

export default {
  name: 'homepage',
  components: { topnav },

  data() {
    return {
      like: 0,
    }
  },

  methods: {
    likeThis() {
      this.like++
    },
  },
}
</script>
