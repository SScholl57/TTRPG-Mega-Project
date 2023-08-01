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
      <SignUpComponent v-if="signUpDisplayed" />
      <LoginComponent v-else />
      <q-btn
        class="glossy"
        color="red-10"
        :label="signUpText"
        @click="onSignUpClicked"
      />
    </div>
  </q-page>
</template>

<script>
import { defineComponent, ref } from "vue";
import SignUpComponent from "components/SignUpComponent.vue";
import LoginComponent from "src/components/LoginComponent.vue";

export default defineComponent({
  name: "IndexPage",

  components: {
    SignUpComponent,
    LoginComponent,
  },

  setup() {
    const signUpDisplayed = ref(false);
    const signUpText = ref("Sign Up");
    return {
      signUpText,
      signUpDisplayed,
      onSignUpClicked() {
        signUpDisplayed.value = !signUpDisplayed.value;
        if (signUpDisplayed.value) {
          signUpText.value = "Cancel";
        } else {
          signUpText.value = "Sign Up";
        }
      },
    };
  },
});
</script>
