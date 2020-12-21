<template>
  <v-container>
    <div class="panel-body">
      <div class="panel-heading">
        <div class="heading-text">
          {{ title }}
        </div>
        <div class="heading-action" @click="open = !open">
          <i class="icon-24 las la-caret-square-down"></i>
        </div>
      </div>
      <div v-if="open" class="panel-content mt20">
        <component :is="component"></component>
      </div>
    </div>
  </v-container>
</template>

<script>
import About from "../components/About";
import Work from "../components/Work";
import Stack from "../components/Stack";
export default {
  data: () => {
    return {
      open: false
    };
  },
  props: ["component", "title"],
  components: {
    About,
    Work,
    Stack
  }
};
</script>

<style scoped>
.panel-heading {
  display: flex;
  justify-content: space-between;
}
</style>
