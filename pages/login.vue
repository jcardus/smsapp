<template>
<div>
  <!--suppress HtmlDeprecatedAttribute -->
  <v-col align="center">
    <h1>
    Welcome to smsApp
    </h1>
  </v-col>
  <firebase-u-i>
  </firebase-u-i>
</div>
</template>

<script>
import FirebaseUI from "../components/FirebaseUI";
export default {
  name: 'login',
  components: {FirebaseUI},
  layout: 'empty'
}
</script>
