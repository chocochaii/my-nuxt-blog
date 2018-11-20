<template>
  <section class="posts-list grid">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :id="post.id"
      :thumbnail="post.thumbnail"
      :title="post.title"
      :previewText="post.previewText" />
  </section>
</template>

<script>
import PostPreview from "@/components/posts/PostPreview.vue";

export default {
  components: {
    PostPreview
  },
  data() {
    return {
      posts: [
        {
          id: "1",
          thumbnail:
            "https://i2-prod.mirror.co.uk/incoming/article11812659.ece/ALTERNATES/s1200/The-Feline-World-Gathers-For-The-Supreme-Cat-Show-2017.jpg",
          title: "Meow World!",
          previewText: "Meow's gonna rule this world"
        },
        {
          id: "2",
          thumbnail:
            "https://i2-prod.mirror.co.uk/incoming/article11812659.ece/ALTERNATES/s1200/The-Feline-World-Gathers-For-The-Supreme-Cat-Show-2017.jpg",
          title: "Meow Sun!",
          previewText: "Meow's gonna rule the Sun"
        },
        {
          id: "3",
          thumbnail:
            "https://i2-prod.mirror.co.uk/incoming/article11812659.ece/ALTERNATES/s1200/The-Feline-World-Gathers-For-The-Supreme-Cat-Show-2017.jpg",
          title: "Meow Moon!",
          previewText: "Meow's gonna rule the Moon"
        },
        {
          id: "4",
          thumbnail:
            "https://i2-prod.mirror.co.uk/incoming/article11812659.ece/ALTERNATES/s1200/The-Feline-World-Gathers-For-The-Supreme-Cat-Show-2017.jpg",
          title: "Meow Mars!",
          previewText: "Meow's gonna rule the Mars"
        }
      ]
    };
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
