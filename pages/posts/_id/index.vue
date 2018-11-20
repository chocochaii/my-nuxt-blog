<template>
  <div class="single-post-page grid">
    <section class="post">
      <h1 class="post-title">Title</h1>
      <div class="post-details">
        <div class="post-detail">Last updated on xxx</div>
        <div class="post-detail">Written by NAME</div>
      </div>
      <p class="post-content">The post content</p>
    </section>
    <section class="post-feedback">
      <p>Let me know what you think about the post, send a mail to <a href="mailto:feedback@my-awesome-domain.com">feedback@my-awesome-domain.com</a></p>
    </section>
  </div>
</template>

<style lang="scss" scoped>
.single-post-page {
  text-align: center;
  .post {
    .post-title {
      font-size: 24px;
      margin: 0;
    }
    .post-details {
      padding: 20px 0;
      border-bottom: 1px solid #666666;
      .post-detail {
        font-size: 18px;
      }
    }
    .post-content {
      text-align: left;
    }
  }
  .post-feedback {
    padding: 20px;
  }
}
</style>

