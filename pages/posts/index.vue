<template>
  <div class="posts-page">
    <PostList />
  </div>
</template>

<script>
import PostPreview from "@/components/Posts/PostPreview.vue";
import PostList from "../../components/Posts/PostList.vue";
export default {
  components: {
    PostPreview,
    PostList,
  },
};
</script>

<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>