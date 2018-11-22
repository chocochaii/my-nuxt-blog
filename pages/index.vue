<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get the latest meow news!</h1>
    </section>
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
import PostList from "@/components/posts/PostList.vue";

export default {
  components: {
    PostList
  },
  computed: {
    loadedPosts() {
      return this.$store.getters.loadedPosts;
    }
  }
};
</script>


<style lang="scss" scoped>
.home-page {
  .intro {
    position: relative;
    height: 300px;
    background-image: url("~assets/images/main-page-header.jpg");
    background-position: center;
    background-size: cover;
    h1 {
      position: absolute;
      font-size: 24px;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  }
}
</style>
