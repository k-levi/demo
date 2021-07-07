<template>
  <div>
    <topnav/>

    <cat />
  </div>
</template>

<script>
import cat from '@/components/levi/cat.vue'
import topnav from '@/components/levi/topnav.vue'

export default {
  name: 'TestPage', 
  components: { cat, topnav },
}
</script>
