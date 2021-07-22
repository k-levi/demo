<template>
  <div class="index">
    <header>
      <topnav />
    </header>

    <div
      class="middel-div"
      style="
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
      "
    >
      <p class="text">Drop some <span>&#128077;</span></p>
      <button v-on:click="likeThis">Like</button>
    </div>
    <div
      class="middel-div"
      style="
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        margin-top: 50px;
        font-size: 18px;
      "
    >
      <p>The page has {{ like }}<span>&#128077;</span></p>
    </div>
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
