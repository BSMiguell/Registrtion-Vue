<template>
  <label class="switch">
    <input type="checkbox" @change="switchTheme" />
    <span class="slider round"></span>
  </label>
</template>

<script>
export default {
  methods: {
    switchTheme(e) {
      e.target.checked
        ? document.documentElement.classList.add("white")
        : document.documentElement.classList.remove("white");
    },
  },
};
</script>

<style lang="scss" scoped>
.switch {
  position: fixed;
  top: 20px;
  right: 20px;
  display: inline-block;
  width: 40px;
  height: 24px;
}

/* Hide default HTML checkbox */
.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

/* The slider */
.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 20px;
  width: 20px;
  left: 2px;
  bottom: 2px;
  background-color: white;
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

input:checked + .slider {
  background-color: var(--info-color);
}

input:focus + .slider {
  box-shadow: 0 0 1px var(--info-color);
}

input:checked + .slider:before {
  transform: translateX(16px);
}

/* Rounded sliders */
.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}
</style>
