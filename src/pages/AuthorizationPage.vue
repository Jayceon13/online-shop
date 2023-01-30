<template>
  <div>
    <q-form
      @submit="onSubmit"
      @reset="onReset"
      class="q-gutter-md"
      method="post"
    >
      <q-input
        filled
        v-model="email"
        label="E-mail *"
        :rules="[
       (val, rules) => rules.email(val) || 'Please enter a valid email address'
       ]"
      />
      <q-input v-model="password" filled :type="isPwd ? 'password' : 'text'" hint="Password with toggle">
        <template v-slot:append>
          <q-icon
            :name="isPwd ? 'visibility_off' : 'visibility'"
            class="cursor-pointer"
            @click="isPwd = !isPwd"
          />
        </template>
      </q-input>
      <div>
        <q-btn label="Submit" type="submit" color="black" id="feedback-form" formaction="/.netlify/functions/send-email"/>
        <q-btn label="Reset" type="reset" color="primary" flat class="q-ml-sm" />
      </div>
    </q-form>
  </div>
</template>

<script>
import {defineComponent} from "vue";
import { ref } from 'vue'

export default defineComponent({
  name: 'AuthorizationPage',
    setup () {
      return {
        password: ref(''),
        isPwd: ref(true),

        email: ref(''),
      }
  }
})
</script>

<style scoped>

</style>
