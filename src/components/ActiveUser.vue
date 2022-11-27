<template>
  <section>
    <header>
      <h2>Name: {{ uname }}</h2>
      <h3>Age: {{ uage }}</h3>
    </header>
  </section>
</template>

<script>
export default {
  props: {
    uname: {
      type: String,
      required: true,
    },
    uage: {
      type: Number,
      required: true,
    },
  },
};
</script>
