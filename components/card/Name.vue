<script setup lang="ts">
interface NameProps {
  name: string;
  index: number;
}
const props = defineProps<NameProps>();

const emit = defineEmits([
  "remove",
]);

const removeName = () => {
  emit("remove", props.index);
}
</script>

<template>
  <div class="card">
    <h3>{{ name }}</h3>
    <p @click="removeName">x</p>
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
