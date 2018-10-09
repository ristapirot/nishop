<template>
  <v-app>
    <v-toolbar
      app
      :clipped-left="clipped"
    >
      <v-toolbar-title class="logo display-2 font-weight-bold">
        <span style="color: red;">N</span>
        <span>i</span>
        <span>s</span>
        <span>h</span>
        <span>o</span>
        <span>p</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>
    <v-content>
      <HelloWorld/>
    </v-content>
    <v-footer :fixed="fixed" app>
      <span>&copy; 2017</span>
    </v-footer>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data () {
    return {
      clipped: false,
      drawer: true,
      fixed: false,
      phone: false,
      mail: false,
      items: [{
        icon: 'bubble_chart',
        title: 'Inspire'
      }],
      miniVariant: false,
      right: true,
      rightDrawer: false
    }
  },
  methods: {
    phoneClick () {
      this.phone = true;
      this.mail = false;
    },
    mailClick () {
      this.phone = false;
      this.mail = true;
    }
  }
}
</script>

<style>
  .logo {
    font-family: 'Lato', sans-serif;
  }

  .phone-card {
    width: 70%;
    margin: 2em auto;

  }
</style>

