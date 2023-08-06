<template>
  <div>
    <!-- Importar o UserCard -->
    <button @click="fetchRandomUser()">Obter usuário aleatório</button>
    <UserCard v-if="!user" />
  </div>
</template>

<script>
import axios from "axios";
import UserCard from "./components/UserCard.vue";

export default {
  name: "RandomUserGenerator",

  data() {
    return {
      // O usuário começa como nulo
      user: null,
    };
  },

  components: {
    UserCard,
  },

  methods: {
    // Buscar na api usando axios
    // Async permite que a função espere até ser executada --> uso do await
    async fetchRandomUser() {
      try {
        const response = await axios.get("https://randomuser.me/api/");
        console.log(response.data);
        // this.user = response.data.results[0]; // Define o usuário retornado na resposta
      } catch (error) {
        console.log('Em caso de erro', error);
      }
    },
  },
};
</script>

<style></style>
