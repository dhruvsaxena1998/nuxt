<template>
  <div>
    <h1>{{ post.title }}</h1>
    <h2>{{ post.description }}</h2>
    <h3>{{ post.continent }}</h3>

    <span class="my-2 px-2 py-2 btn bg-blue-500 cursor-pointer" @click="next"
      >Next Post</span
    >
  </div>
</template>

<script>
export default {
  async asyncData({ params, $axios, $nuxt }) {
    const post = await $axios.$get('https://api.nuxtjs.dev/posts/' + params.id)
    return { post }
  },
  data() {
    return {
      id: undefined,
    }
  },
  methods: {
    next() {
      this.id += 1

      this.$router.push(`/posts/${this.id}`)
    },
  },
  mounted() {
    this.id = parseInt(this.$route.params.id)
  },
}
</script>
