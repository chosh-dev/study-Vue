<template>
  <div>
    Celcius=
    <input type="number" :value="c" @change="setC" />
    Fahrenheit=
    <input type="number" :value="f" @change="setF" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      c: 0,
      f: 32,
    };
  },
  methods: {
    setC(e, c = e.target.value) {
      this.c = c;
      this.f = c * (9 / 5) + 32;
    },
    setF(e, f = e.target.value) {
      this.f = f;
      this.c = (f - 32) * (5 / 9);
    },
  },
};
</script>

<style lang="scss" scoped></style>
