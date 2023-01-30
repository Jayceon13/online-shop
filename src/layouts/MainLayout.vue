<template>
  <q-layout>
      <store-header></store-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import StoreHeader from "components/StoreHeader";


export default defineComponent({
  name: 'MainLayout',
  components: {
    StoreHeader,
  },


})
</script>
