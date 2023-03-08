<template>
  <div class="q-pa-md" style="max-width: 300px">
    <q-form class="q-gutter-md">
      <q-input outlined label="Enter a name" v-model="name" />
      <div class="q-ml-sm">
        <q-btn @click="formatMsg" label="Show Message" />
      </div>
      <p>{{ message }}</p>
    </q-form>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  setup() {
    let name = ref(null)
    let message = ref(null)
    return {
      name,
      message,
      formatMsg() {
        message.value = `Hello ${name.value}`;
      },
    }
  }
}
</script>