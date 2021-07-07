<template>
  <div>
    <img :src="imageUrl" alt="cat" />

    <h1>
      {{ name }}
    </h1>

    <div class="catname">
      <label class="mylabel" for="cat-input">Cat name</label>
      <input type="text" id="cat-input" v-model="name" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'cat',
  data() {
    return {
      imageUrl:
        'https://upload.wikimedia.org/wikipedia/commons/thumb/c/c7/Tabby_cat_with_blue_eyes-3336579.jpg/499px-Tabby_cat_with_blue_eyes-3336579.jpg',
      name: '',
    }
  },
}
</script>
