<template>
  <div>
    <h2>Captcha With Composition API</h2>
    <CaptchaWithCompositionAPI />
  </div>
  <div style="margin-top: 6rem">
    <h2>Captcha With Option API</h2>
    <CaptchaWithOptionAPI />
  </div>
  <div style="margin-top: 6rem">
    <h2>Submit Form</h2>
    <SampleOnSaveWithOptionAPI />
  </div>
</template>

<script >
import CaptchaWithCompositionAPI from "./components/CaptchaWithCompositionAPI";
import CaptchaWithOptionAPI from "./components/CaptchaWithOptionAPI";
import SampleOnSaveWithOptionAPI from "./components/SampleOnSaveWithOptionAPI";

export default {
  components: {
    CaptchaWithCompositionAPI,
    CaptchaWithOptionAPI,
    SampleOnSaveWithOptionAPI,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
