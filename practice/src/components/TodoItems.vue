<template>
  <li>{{ todo.text }}</li>
</template>

<script>
export default {
  props: {
    todo: Object,
  },
};
</script>
