<template>
  <div
    class="flex column flex-center"
    style="overflow: auto; min-width: 50%; max-width: 50%"
  >
    <q-input
      outlined
      class="q-mb-md"
      v-model="text"
      type="text"
      label="Username"
      id="loginUsername"
    />
    <q-input
      v-model="password"
      outlined
      class="q-mb-md"
      type="password"
      label="Password"
      :dense="dense"
    />
    <q-btn class="glossy q-mb-md" color="red-10" label="Login" />
  </div>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "LoginComponent",
  setup() {
    return {
      text: ref(""),
      password: ref(""),
    };
  },
});
</script>
