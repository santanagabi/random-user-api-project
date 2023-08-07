<template>
  <div>
    <!-- Importar o UserCard -->
    <button @click="fetchRandomUser" class="random-user-button">Get random user</button>
    <UserCard :user="user" />
  </div>
</template>

<script>
import axios from "axios";
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

  methods: {
    async fetchRandomUser() {
      try {
        const response = await axios.get("https://randomuser.me/api/");
        this.user = response.data.results[0];
      } catch (error) {
        console.log("Em caso de erro", error);
      }
    },
  },
};
</script>

<style>
.random-user-button {
  background-color: #4caf50;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  font-size: 16px;
  transition: background-color 0.3s ease;
}

.random-user-button:hover {
  background-color: #45a049;
}
</style>
