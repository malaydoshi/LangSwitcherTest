<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
      <hr />
      <label for="lang">Select Your Language: </label>
      <select v-model="$i18n.locale" id="lang">
          <option v-for="(lang,i) in $i18n.availableLocales" :key="`Lang${i}`" :value="lang">{{lang}}</option>
      </select>
      <hr />
      <p>{{ $t('message') }}</p>
      <hr />
      <p>{{selectedLang}}</p>
  </div>
</template>

<script>

export default {
  name: 'app',
  components: {
    //HelloWorld
        },
        data() {
            return {
                //selectedLang: 'en',
                //availableLang: ['en','fr','ja']
            }
        }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
