<template>
    <div class="user-card-container" v-if="user">
      <img :src="user.picture.large" alt="User Avatar" class="user-avatar" />
      <h2 class="user-name">{{ user.name.title }} {{ user.name.first }} {{ user.name.last }}</h2>
      <p class="user-location">
        Location: {{ user.location.country }} - {{ user.location.state }}
        {{ user.location.city }}
      </p>
      <p class="user-age">Age: {{ user.registered.age }}</p>
      <p class="user-email">E-mail: {{ user.email }}</p>
    </div>
  
    <div v-if="!user" class="loading-message">
      <span>Loading ...</span>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      user: Object,
    },
  };
  </script>
  
  <style>
  .user-card-container {
    background: rgb(132, 182, 216);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 300px;
    border-radius: 6px;
  }
  
  .user-avatar {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin-bottom: 10px;
  }
  
  .user-name {
    margin: 0;
    font-size: 1.5rem;
  }
  
  .user-location,
  .user-age,
  .user-email {
    font-size: 1rem;
  }
  
  .loading-message {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 300px;
    border-radius: 6px;
  }
  </style>
  