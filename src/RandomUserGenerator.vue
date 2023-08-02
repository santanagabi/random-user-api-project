<template>
  <div>
    <!-- Importar o UserCard -->
    <UserCard></UserCard>
  </div>
</template>

<script>
import UserCard from './components/UserCard.vue';

export default {
  name: 'RandomUserGenerator',
  components: {
    UserCard
  }
}
</script>

<style>

</style>
