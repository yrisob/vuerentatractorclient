<template>
<v-container grid-list-xl>
  <v-layout row wrap>
    <v-flex xs4 offset-xs4 >
    <v-img   :src="require('@/assets/logo.png')" />
    </v-flex>
    <v-flex xs12>
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
    </v-flex>
  </v-layout>
</v-container>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

@Component({
  components: {
    HelloWorld,

  },
})
export default class Home extends Vue {}
</script>
