<template>
  <q-page class="flex flex-center">
    <div
      class="flex flex-center"
      style="overflow: hidden; min-width: 50%; max-width: 50%"
    >
      <img
        alt="Quasar logo"
        src="~assets/index-page-image.jpg"
        style="width: 960px; height: 917px"
      />
    </div>
    <div
      class="flex column flex-center"
      style="overflow: auto; min-width: 50%; max-width: 50%"
    >
      <q-input outlined v-model="text" label="Username" class="q-mb-md" />
      <q-input
        outlined
        v-model="email"
        label="Email"
        class="q-mb-md"
        type="email"
      />
      <q-input
        outlined
        v-model="password"
        label="Password"
        class="q-mb-md"
        type="password"
      />
      <q-btn class="glossy q-mb-md" color="red-10" label="Create Account" />
      <q-btn class="glossy" color="red-10" label="Cancel" to="/" />
    </div>
  </q-page>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "IndexPage",

  setup() {
    return {
      text: ref(""),
      email: ref(""),
      password: ref(""),
    };
  },
});
</script>
