<template>
  <nuxt-link :to="'/posts/' + id" class="post-preview">
    <article>
      <div class="post-thumbnail">
        <div class="thumbnail" :style="getPostThumbnail"></div>
      </div>
      <div class="post-content">
        <h1>{{ title }}</h1>
        <p>{{ previewText }}</p>
      </div>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    id: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    previewText: {
      type: String,
      required: true
    },
    thumbnail: {
      type: String,
      required: true
    }
  },
  computed: {
    getPostThumbnail() {
      return {
        "background-image": "url('" + this.thumbnail + "')"
      };
    }
  }
};
</script>

<style lang="scss" scoped>
.post-preview {
  display: block;
  min-width: 300px;
  border: 1px solid #eeeeee;
  margin-bottom: 30px;
  .post-thumbnail {
    height: 200px;
    overflow: hidden;
    .thumbnail {
      width: 100%;
      height: 100%;
      background-size: cover;
      background-repeat: no-repeat;
      background-position: center;
      background-color: white;
      transition: all 0.5s;
    }
  }
  .post-content {
    text-align: center;
    background: white;
    padding: 10px;
  }
  &:hover {
    .post-thumbnail {
      .thumbnail {
        transform: scale(1.2);
      }
    }
    .post-content {
      background: #eeeeee;
    }
  }
}
</style>

