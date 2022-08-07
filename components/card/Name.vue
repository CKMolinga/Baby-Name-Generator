<script setup lang="ts">
interface NameProps {
  name: string;
}
const props = defineProps<NameProps>();
</script>

<template>
  <div class="card">
    <h3>{{ name }}</h3>
    <p>x</p>
  </div>
</template>

<style scoped>
.card {
  background-color: rgb(27, 60, 138);
  color: #fff;
  border-radius: 0.1rem;
  padding: 1rem;
  margin: 0 0.5rem 1rem 0;
  width: 28%;
  text-align: center;
  position: relative;
}

.card p {
  position: absolute;
  top: -29%;
  left: 92.5%;
  cursor: pointer;
  color: rgba(0, 0, 0, 0.178);
  font-size: 1.5rem;
}
</style>
