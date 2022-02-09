<template>
  <div>
    <h1>HOME</h1>
    {{ title }}
  </div>
</template>

<script>
export default {
  setup() {
    const title = ref('ようこそ');
    return {
      title,
    };
  },
};
</script>
