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
    async fetchRandomUser() {
      
    }
  }
};
</script>

<style></style>
