<template>
  <div>
    <p>{{ message }}</p>
    <button @click="updateMessage">Update Message</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const message = ref("Hello, Vue!");

    const updateMessage = () => {
      message.value = "Hello, Vue updated!";
    };

    return {
      message,
      updateMessage,
    };
  },
};
</script>
