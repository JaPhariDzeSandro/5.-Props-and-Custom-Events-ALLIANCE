<template>
  <section>
    <input type="text" placeholder="Name" v-on:input="changeName" />
    <input type="text" placeholder="Age" v-on:input="changeAge" />
  </section>
</template>

<script>
export default {
  data() {
    return {
      namename: "",
      ageage: "",
    };
  },
  emits:['changeableName','changeableAge'],
  methods: {
    changeName(event) {
      this.namename = event.target.value;
      this.$emit('changeableName', this.namename)
    },
    changeAge(event) {
      this.ageage = event.target.value;
      this.$emit('changeableAge', this.ageage)
    },
  },
};
</script>
