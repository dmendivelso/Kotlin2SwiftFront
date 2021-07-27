<template>
  <b-container fluid>
    <b-row align-v="center">
      <b-col sm="5">
        <b-form-textarea
          id="textarea-rows"
          v-model="code"
          placeholder="Your code here"
          rows="30"
        ></b-form-textarea>
      </b-col>
      <b-col sm="2">
        <b-button size="lg" @click="translateCode">Traducir</b-button>
        <b-button size="lg" v-clipboard:copy="codeTranslated"
          >Copiar codigo</b-button
        >
      </b-col>

      <b-col sm="5">
        <b-form-textarea
          id="textarea-rows"
          v-model="codeTranslated"
          placeholder="Your code translated here"
          rows="30"
          readonly
        ></b-form-textarea>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import axios from "axios";
axios.defaults.baseURL = "http://localhost:9000/";
axios.defaults.headers["Content-Type"] = "application/text";

export default {
  data() {
    return {
      code: "",
      codeTranslated: "",
    };
  },
  methods: {
    translateCode() {
      axios.post("translate", this.code.toString()).then((response) => {
        this.codeTranslated = response.data;
      });
    },
  },
};
</script>

<style scoped>
.col-sm-5 {
  padding: 0em 4.5em;
}

.btn {
  width: 90%;
  margin-top: 1em;
  margin-bottom: 1em;
}
textarea {
  background-color: #000 !important;
  border: 1px solid #000 !important;
  color: #e9d41b !important;
  padding: 8px !important;
  font-family: courier new !important;
}
</style>
