<template>
  <div>
    <div class="row">
      <div class="col-md-6 left-box">
        <!-- chars: if you want only numbers in your captcha -->
        <VueClientRecaptcha
          :value="inputValue"
          chars="123456789"
          :hidelines="false"
          custom-text-color="black"
          @getCode="getCaptchaCode"
          @isValid="checkValidCaptcha"
        >
          <template #icon>
            <span style="color: blue">Reload Captcha</span>
          </template>
        </VueClientRecaptcha>

        <input
          type="text"
          v-model="inputValue"
          placeholder="masukan captha dengan benar!"
        />
      </div>
    </div>
    <div class="row">
      <div class="col-md-6 left-box">
        <input
          type="button"
          value="Save Data"
          class="btn btn-primary"
          @click="save()"
        />
      </div>
    </div>
  </div>
</template>
<script>
import VueClientRecaptcha from "vue-client-recaptcha";
export default {
  components: {
    VueClientRecaptcha,
  },
  data() {
    return {
      inputValue: null,
      isValidCaptcha: false,
    };
  },
  methods: {
    getCaptchaCode(capthaResult) {
      /* you can access captcha code */
      console.log(capthaResult);
    },
    checkValidCaptcha(capthaResult) {
      /* expected return boolean if your value and captcha code are same return True otherwise return False */
      console.log("this is captha valid " + capthaResult);
      this.isValidCaptcha = capthaResult;
    },
    save() {
      /* you can call variable Or return checkValidCaptcha function */
      console.log("this is from click " + this.isValidCaptcha);
      if (this.isValidCaptcha) {
        alert("Your Form Submited! captcha is valid");
      } else {
        alert("Your Form Not Submited! captcha is inValid");
      }
    },
  },
};
</script>