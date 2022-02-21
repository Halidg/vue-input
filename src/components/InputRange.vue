<template>
  <h2 class="h2">{{modelValue}}%</h2>

  <div class="range-container">
    <input class="range"
      :value="modelValue"
      type="range"
      @input="$emit('update:modelValue', $event.target.value)"
      :step="0.1"
    >
  </div>
</template>

<script>
export default {
  props:{
    modelValue: {
      type:Number,
      required:true
    }
  }
}
</script>

<style lang="scss" scoped>
.range-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 25px;
  margin-bottom: 25px;
}

.range {
  -webkit-appearance: none;
  background: linear-gradient(90deg, #1E9600,#FFF200,#FF0000);
  border-radius: 12px;
  width: 100%;
  height: 20px;
  outline: none;
  &::-webkit-slider-thumb {
    -webkit-appearance: none;
    background: white;
    width: 15px;
    height: 15px;
    border-radius: 18px;
    cursor: pointer;  
  }
}

.h2 {
  color: #AAAAAA;
}
</style>