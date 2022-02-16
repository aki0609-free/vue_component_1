<template>
  <li>
    <h2>{{ friend.name }}</h2>
    <button @click="toggleDetails">
      {{ detailsAreVisible ? "Hide" : "Show" }} Details
    </button>
    {{ detailsAreVisible }}
    <ul v-if="detailsAreVisible">
      <li><strong>Phone:</strong>{{ friend.phone }}</li>
      <li><strong>Email:</strong>{{ friend.email }}</li>
    </ul>
  </li>
</template>

<script>
import { reactive, ref } from "vue";

export default {
  setup() {
    let detailsAreVisible = ref(false);
    const friend = reactive({
      id: "manuel",
      name: "Manuel Lorenz",
      phone: "0123 45678 90",
      email: "manuel@localhost.com",
    });

    const toggleDetails = () => {
      detailsAreVisible.value = !detailsAreVisible.value;
    };

    return {
      detailsAreVisible,
      friend,
      toggleDetails,
    };
  },
};
</script>
