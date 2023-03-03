<template>
  <VueClientRecaptcha @getCode="getCaptchaCode" />
  <small>{{ captchaCodeVarComposition }}</small>
</template>

<script >
/* eslint-disable no-undef, @typescript-eslint/no-unused-vars, no-unused-vars */
import { ref } from "vue";
import VueClientRecaptcha from "vue-client-recaptcha";
import "vue-client-recaptcha/dist/style.css";
export default {
  components: {
    VueClientRecaptcha,
  },
  setup() {
    /* pass value to captcha  */
    const captchaCodeVarComposition = ref(null);

    const getCaptchaCode = (value) => {
      /* you can access captcha code */
      console.log(value);
      captchaCodeVarComposition.value = value;
    };
    return {
      getCaptchaCode,
      captchaCodeVarComposition,
    };
  },
};
</script>
