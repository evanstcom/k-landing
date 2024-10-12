<template>
  <div class="flex gap-2 items-center">
    <label class="custom-checkbox" :class="{ checked }">
      <input type="checkbox" @change="handleChange" />
      <div class="slider"></div>
    </label>
    <span class="label mt-1">{{ label }}</span>
  </div>
</template>

<script>
export default {
  name: "CustomCheckbox",
  props: {
    label: {
      type: String,
      default: "Checkbox",
    },
    value: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      isChecked: this.value,
    };
  },
  computed: {
    checked() {
      return this.isChecked;
    },
  },
  methods: {
    handleChange() {
      this.isChecked = !this.isChecked;
      this.$emit("input", this.isChecked);
    },
  },
};
</script>

<style scoped>
.custom-checkbox {
  display: flex;
  align-items: center;
  cursor: pointer;
}

.custom-checkbox input {
  display: none;
}

.slider {
  width: 40px;
  height: 20px;
  background-color: #ccc;
  border-radius: 20px;
  position: relative;
  transition: background-color 0.2s;
  margin-right: 10px;
}

.slider:before {
  content: "";
  position: absolute;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  background-color: white;
  left: 1px;
  bottom: 1px;
  transition: transform 0.2s;
}

.custom-checkbox.checked .slider {
  background-color: #316fee; /* Зеленый цвет для включенного состояния (iOS-стиль) */
}

.custom-checkbox.checked .slider:before {
  transform: translateX(20px); /* Сдвиг кнопки при включении */
}

.label {
  font-size: 14px;
  color: #333;
}
</style>
