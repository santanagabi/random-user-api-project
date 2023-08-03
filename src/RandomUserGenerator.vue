<template>
  <div>
    <!-- Importar o UserCard -->
    <UserCard></UserCard>
  </div>
</template>

<script>
// import axios from "axios";
import UserCard from "./components/UserCard.vue";

export default {
  name: "RandomUserGenerator",

  data() {
    return {
      user: null,
    };
  },

  components: {
    UserCard,
  },

  methos: {
    // Buscar na api usando axios
    // Async permite que a função espere até ser executada --> uso do await
    async fetchRandomUser() {

    }
  }
};
</script>

<style></style>
