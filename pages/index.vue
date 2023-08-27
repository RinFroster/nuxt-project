<template>
  <main>
    <section>
      <div class="container">
        <h1 class="text-4xl font-bold text-center text-red-500">
          Hi - This is my Project
        </h1>
        <div>Demo Post</div>
        <div>{{ posts }}</div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const posts = await $content(`/posts`).fetch()
    return {
      posts,
    }
  },
}
</script>
