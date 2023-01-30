<template>
  <div class="header">
    <div class="links-page">
      <q-btn-toggle
        v-model="model"
        toggle-color="red"
        flat
        :options="[
          {label: 'SHOP', value: 'one'},
          {label: 'ABOUT', value: 'two'},
          {label: 'SUPPORT', value: 'three'}
        ]"
      />
    </div>
    <div class="logo-page">
      <img alt="" src="/BH13.svg">
    </div>
    <div class="icons-page">
      <q-btn flat style="color: #000000"  icon="img:/glass.svg"></q-btn>
      <q-btn flat style="color: #000000" icon="img:/cart.svg"></q-btn>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: "StoreHeader",

  setup () {
    return {
      model: ref('one')
    }
  }
}
</script>

<style scoped>
.header{
  display: flex;
  width: 100%;
  justify-content: center;
}
.links-page{
  margin-right: auto;
}
.logo-page {
  margin: auto;
}

.icons-page{
  margin-left: auto;
}
</style>
