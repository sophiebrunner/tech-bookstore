<template>
  <button :class="cssBaseButton" @click="buttonClick"><slot /></button>
</template>

<script>
export default {
  name: "BaseButton",
  props: {
    variant: {
      type: String,
      default: "primary",
      validator(propValue) {
        return ["primary", "secondary"].includes(propValue);
      },
    },
  },
  computed: {
    cssBaseButton() {
      return ["btn", `btn--${this.variant}`];
    },
  },
  methods: {
    buttonClick() {
      this.$emit("buttonClick");
    },
  },
  emits: ["buttonClick"],
};
</script>

<style scoped>
.btn {
  border: 3px solid transparent;
  border-radius: 3px;
  padding: 5px;
  cursor: pointer;
}

.btn--primary {
  border-color: var(--primary-dark);
  background-color: var(--primary);
  color: #fff;
}

.btn--primary:hover {
  border-color: var(--primary);
  background-color: var(--primary-dark);
}

.btn--secondary {
  border-color: var(--primary);
  background-color: transparent;
  color: var(--primary);
}

.btn--secondary:hover {
  background-color: var(--primary);
  color: #fff;
}
</style>
