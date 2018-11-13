<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get the latest meow news!</h1>
    </section>
    <section class="featured-posts">
      <PostPreview
        id="1"
        thumbnail="https://i2-prod.mirror.co.uk/incoming/article11812659.ece/ALTERNATES/s1200/The-Feline-World-Gathers-For-The-Supreme-Cat-Show-2017.jpg"
        title="Meow World!"
        previewText="Meow's gonna rule this world" />
      <PostPreview
        id="2"
        thumbnail="https://i2-prod.mirror.co.uk/incoming/article11812659.ece/ALTERNATES/s1200/The-Feline-World-Gathers-For-The-Supreme-Cat-Show-2017.jpg"
        title="Meow Sun!"
        previewText="Meow's gonna rule the Sun" />
      <PostPreview
        id="3"
        thumbnail="https://i2-prod.mirror.co.uk/incoming/article11812659.ece/ALTERNATES/s1200/The-Feline-World-Gathers-For-The-Supreme-Cat-Show-2017.jpg"
        title="Meow Moon!"
        previewText="Meow's gonna rule the Moon" />
    </section>
  </div>
</template>

<script>
import PostPreview from "@/components/posts/PostPreview.vue";

export default {
  components: {
    PostPreview
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
