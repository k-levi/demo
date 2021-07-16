<template>
  <div class="index">
    <topnav />

    <p class="text">Drop some <span>&#128077;</span></p>
    <button v-on:click="likeThis">Like</button>

    <p>The page has {{ like }}<span>&#128077;</span></p>
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
