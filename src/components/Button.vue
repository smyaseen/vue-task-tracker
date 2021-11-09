<template>
  <button @click="$emit('onClick')" :style="{ background: color }" class="btn">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: String,
    color: String,
  },
  emits: ["onClick"],
};
</script>
