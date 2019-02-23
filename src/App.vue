<template>
  <div id="app">
    <v-app>
      <v-content>
        <v-container>
          <v-layout>
            <v-flex>
              <v-tabs>
                <v-tab v-for="i in 24">
                  link {{i}}
                </v-tab>
              </v-tabs>
            </v-flex>
          </v-layout>
          <v-layout>
            <v-btn @click="changeDir()">
              change dir
            </v-btn>
            <div>
              rtl: {{ $vuetify.rtl }}
            </div>
          </v-layout>
        </v-container>
      </v-content>
    </v-app>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  methods: {
    changeDir() {
      this.$vuetify.rtl = !this.$vuetify.rtl
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
