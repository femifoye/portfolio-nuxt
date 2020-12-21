<template>
  <v-app dark>
    <v-container>
      <v-row id="navigation">
        <v-col :cols="10" class="toggle-dark-mode">
          <v-switch inset v-model="dark" @click="toggleDark" />
          <div class="switch-label">
            <div v-if="!$vuetify.theme.isDark" class="dark">
              <i class="icon-24 las la-moon"></i>
            </div>
            <div v-else class="light">
              <i class="icon-24 las la-sun"></i>
            </div>
          </div>
        </v-col>
        <v-col :cols="2">
          <!-- <i class="icon-24 las la-bars"></i> -->
        </v-col>
      </v-row>

      <nuxt />
    </v-container>

    <v-footer app> </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      dark: true
    };
  },

  methods: {
    toggleDark() {
      this.$vuetify.theme.isDark = !this.$vuetify.theme.isDark;
    }
  },

  // watch: {
  //   dark: {
  //     handler(val) {
  //       this.$vuetify.theme.dark = !this.vuetify.theme.dark;
  //       console.log(this.$vuetify.theme.dark);
  //     }
  //   }
  // },

  mounted() {
    console.log(this.$vuetify);
  }
};
</script>

<style>
.btn-email {
  font-size: 14px;
  margin-top: 5px;
}
</style>
