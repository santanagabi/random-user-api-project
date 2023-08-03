<!-- Aqui colocar o conteúdo do user card -->
<template>
  <div class="user-card">
    {{ 'Aqui é o User Card' }}
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
.user-card {
    background: rgb(132, 182, 216);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 300px;
    border-radius: 6px;
}
</style>
