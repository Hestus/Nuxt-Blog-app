<template>
  <form @submit.prevent="onSave">
    <app-control-input v-model="editedPost.author">
      Author Name
    </app-control-input>
    <app-control-input v-model="editedPost.title">Title</app-control-input>
    <app-control-input v-model="editedPost.thumbnailLink">
      Thumbnail Link
    </app-control-input>
    <app-control-input control-type="textarea" v-model="editedPost.content">
      Content
    </app-control-input>
    <app-button type="submit">Save</app-button>
    <app-button
      type="button"
      style="margin-left: 10px"
      btn-style="cancel"
      @click="handleRequestToCancel"
    >
      Cancel
    </app-button>
  </form>
</template>

<script>
import { ref } from "@vue/composition-api";
import { useRouter } from "@nuxtjs/composition-api";
import AppButton from "~/components/UI/AppButton.vue";
import AppControlInput from "~/components/UI/AppControlInput.vue";
export default {
  components: { AppControlInput, AppButton },
  props: {
    post: {
      type: Object,
      required: false,
    },
  },
  setup(props) {
    const editedPost = ref(
      props.post
        ? { ...props.post }
        : {
            author: "",
            title: "",
            thumbnailLink: "",
            content: "",
          }
    );

    function onSave() {
      // Save the post
      console.log(editedPost.value);
    }

    const router = useRouter()
    function handleRequestToCancel() {
      // Navigate Back
      router.push("/admin")
      // this.$router.push("/admin");
    }

    return {
      editedPost,
      onSave,
      handleRequestToCancel,
    };
  },
};
</script>