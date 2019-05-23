
<template>
 <v-footer
      height="auto"
     dark
     class="toolbar_footer"
    >
      <!-- <v-layout
        justify-center
        row
        wrap
      >
        <v-btn
          v-for="link in links"
          :key="link"
          color="white"
          flat
          round
        >
          {{ link }}
        </v-btn> -->
        <v-flex
          dark
          py-3
          text-xs-center
          white--text
          xs12
        >
          &copy;2019 — <strong>ITHeads</strong>
        </v-flex>
      </v-layout>
    </v-footer>

</template>

<script lang="ts">
  import { Component, Vue, Prop } from 'vue-property-decorator';
  @Component({
          props: {
              links: Array,
          },
      })
  export default class AppFooter extends Vue {
    public links!: string[];
  }
</script>