<template>
  <div class="container">
   <InputRange v-model="inputValue"/>
   <div class="block">
    <button class="button" @click="inputValue=25">25%</button>
    <button class="button" @click="inputValue=50">50%</button>
    <button class="button" @click="inputValue=75">75%</button>
    <button class="button" @click="inputValue=100">100%</button>     
  </div>
  </div>
</template>

<script>

import InputRange from './components/InputRange.vue'

export default {
  components:{InputRange},
  data() {
    return {
      inputValue: 15
    }
  }
}
</script>
<style lang="scss" scoped>
.container {
  margin: 0 auto;
  padding: 15px;
  max-width: 900px;
}

.block {
  display: flex;
  justify-content: space-between;
  width: 30%;
  margin: 0 auto;
}

.button {
  border-radius: 22px;
  border: none;
  padding: 10px 10px;
  color: white;
  background: #54618b;
  &:hover {
    cursor: pointer;
  }
}
</style>
