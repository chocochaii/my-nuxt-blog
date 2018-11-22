<template>
  <section class="posts-list grid">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :id="post.id"
      :thumbnail="post.thumbnail"
      :title="post.title"
      :previewText="post.previewText"
      :is-admin="isAdmin" />
  </section>
</template>

<script>
import PostPreview from "@/components/posts/PostPreview.vue";

export default {
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false
    },
    posts: {
      type: Array,
      required: true
    }
  }
};
</script>

<style lang="scss" scoped>
.posts-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
</style>
