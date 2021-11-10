<template>
    <section class="post-list">
      <PostPreview
        id="1"
        :is-admin="isAdmin"
        title="Hello First post"
        thumbnail="https://about.fb.com/wp-content/uploads/2021/10/Meta-Planets-img-16x9-1.jpg?w=1200"
        previewText="This is my first post!"
      />
      <PostPreview
        id="2"
        :is-admin="isAdmin"
        title="Hello Second Post"
        thumbnail="https://about.fb.com/wp-content/uploads/2021/10/Meta-Planets-img-16x9-1.jpg?w=1200"
        previewText="This is my second post!"
      />
      <PostPreview
        id="3"
        :is-admin="isAdmin"
        title="Hello Third Post"
        thumbnail="https://about.fb.com/wp-content/uploads/2021/10/Meta-Planets-img-16x9-1.jpg?w=1200"
        previewText="This is my third post!"
      />
    </section>
</template>

<script>
import PostPreview from "@/components/Posts/PostPreview.vue";
export default {
    components: {
    PostPreview,
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false,
    }
  }
}
</script>

<style scoped>
.post-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>