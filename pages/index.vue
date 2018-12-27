<template>
  <section class="container">
    <Caption />
    <div>      
      <h1><nuxt-link to="/blog">Blogs</nuxt-link></h1>
      <input type="text" v-model="bid">
      <button @click="onClick">Load Blog Post</button>
    </div>
  </section>
</template>

<script>
import Caption from '~/components/Caption.vue';

export default {
  name: 'home',
  data() {
    return {
      bid: ''
    }
  },
  methods: {
    onClick() {
      this.$router.push('/blog/' + this.bid);
    }
  },
  components: {
    Caption
  }
}
</script>

<style>

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
