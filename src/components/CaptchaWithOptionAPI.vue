<template>
  <VueClientRecaptcha @getCode="getCaptchaCode" />
  <small>{{ captchaCodeVar }}</small>
</template>

<script >
import VueClientRecaptcha from "vue-client-recaptcha";
import "vue-client-recaptcha/dist/style.css";
export default {
  components: {
    VueClientRecaptcha,
  },
  data() {
    return {
      captchaCodeVar: null,
    };
  },
  methods: {
    getCaptchaCode(value) {
      /* you can access captcha code */
      console.log(value);
      this.captchaCodeVar = value;
    },
  },
};
</script>
