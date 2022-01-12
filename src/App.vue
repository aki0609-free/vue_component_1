<template>
  <section>
    <h2>My Friends</h2>
    <ul>
      <friend-contact></friend-contact>
      <friend-contact></friend-contact>
    </ul>
  </section>
</template>

<script>
import FriendContact from './components/FriendContact.vue';
export default {
  components: { FriendContact },
  data() {
    return {
      frinds: [
        {
          id: "manuel",
          name: "Manuel Lorenz",
          phone: "0123 45678 90",
          email: "manuel@localhost.com",
        },
        {
          id: "julie",
          name: "Julie Jones",
          phone: "3210 4568 90",
          email: "julie@localhost.com",
        },
      ],
    };
  },
};
</script>
