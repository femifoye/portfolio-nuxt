<template>
  <div class="work mb20" @mouseover="show()" @mouseleave="hide()">
    <!-- :style="{ 'background-image': 'url(' + work.screen + ')' }" -->
    <div class="image">
      <img :src="work.screen" alt="" />
    </div>
    <div v-if="showOverlay" class="work-overlay">
      <div class="overlay-inner">
        <div v-if="work.wip" class="in-progress-tag">
          <p class="f10 zero-margin">In Progress</p>
        </div>
        <div class="work-title">
          <h4>{{ work.name }}</h4>
        </div>
        <div class="work-desciption mt10">
          <p class="f12">{{ work.description }}</p>
        </div>
        <div class="work-action">
          <a v-if="!work.wip" :href="work.link"
            ><button class="btn visit-button">Visit</button></a
          >
          <a v-else :href="work.link"
            ><button class="btn subscribe-button">Subscribe</button></a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["work"],
  data: () => {
    return {
      showOverlay: false
    };
  },

  components: {},

  methods: {
    show() {
      this.showOverlay = true;
    },

    hide() {
      this.showOverlay = false;
    }
  }
};
</script>

<style>
.theme--light.v-card .work-overlay {
  color: white;
}

.work .image {
  text-align: center;
}

/* .work .image img {
  width: 50%;
} */

@media only screen and (min-width: 320px) {
  .work .image img {
    width: 100%;
  }
}

@media only screen and (min-width: 410px) {
  .work .image img {
    width: 90%;
  }
}

@media only screen and (min-width: 480px) {
  .work .image img {
    width: 80%;
  }
}

@media only screen and (min-width: 532px) {
  .work .image img {
    width: 70%;
  }
}

@media only screen and (min-width: 840px) {
  .work .image img {
    width: 60%;
  }
}

@media only screen and (min-width: 900px) {
  .work .image img {
    width: 50%;
  }
}
</style>
