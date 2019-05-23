<template>
  <div id="app">
    <v-app id="inspire">
      <AppToolbar></AppToolbar>
      <v-layout class="container-after-toolbar"  grid-list-xl>
        <v-layout row wrap>
          <v-flex xs3 class="max-height">
            <AppMenu></AppMenu>
          </v-flex>
          <v-flex xs9>
            <v-container>
              <router-view></router-view>
            </v-container>
          </v-flex>
        </v-layout>
      </v-layout>
      <AppFooter :links="links" />
    </v-app>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import AppFooter from '@/components/AppFooter.vue';
import AppToolbar from '@/components/AppToolbar.vue';
import AppMenu from '@/components/AppMenu.vue';
import '@/assets/main.css';


@Component({
    components: {
      AppFooter,
      AppToolbar,
      AppMenu,
    },
  })
  export default class extends Vue {
    public links: string[] =  [
      'Home',
      'About Us',
      'Team',
      'Services',
      'Blog',
      'Contact Us',
    ];
  }
</script>