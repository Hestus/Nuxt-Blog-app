<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
import AdminPostForm from "~/components/Admin/AdminPostForm.vue";

export default {
  components: { AdminPostForm },

  data() {
    return {
      loadedPost: {
        author: "Manas Mishra",
        title: "My awesome Post",
        content: "Super Amazing, thanks for that",
        thumbnailLink:
          "https://about.fb.com/wp-content/uploads/2021/10/Meta-Planets-img-16x9-1.jpg?w=1200",
      },
    };
  },
};
</script>

<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}
@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>