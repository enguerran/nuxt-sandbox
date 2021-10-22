<template>
  <div>
    <h1>Blog Posts</h1>
    <div>
      <ul v-for="post in posts" :key="post.id">
        <li>{{ post.title }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    posts: [
      {
        title: "lorem",
        description: "lorem ipsum",
      },
    ],
  }),
  async asyncData({ params, $http }) {
    const posts = await $http.$get(`https://api.nuxtjs.dev/posts`);
    console.log(posts);
    return { posts };
  },
};
</script>

<style>
</style>