<template>
  <div class="works">
    <single-work
      v-for="work in works"
      :key="work.id"
      :work="work"
    ></single-work>
  </div>
</template>

<script>
import SingleWork from "../components/works/SingleWork";
export default {
  data: () => {
    return {
      works: [
        {
          id: 1,
          name: "Bookatutor",
          description:
            "Built a prototype that allows University students find Tutors in their area. Tutors are matched to students based on student competency levels in interested subjects",
          wip: false,
          link: "https://guarded-chamber-71286.herokuapp.com/",
          screen:
            "https://res.cloudinary.com/house16-design-studio/image/upload/v1608571819/portfolio/bookatutor-screen-new.png"
        },
        {
          id: 2,
          name: "Trakjungle",
          description:
            "A platform for music creatives in the African region to make money selling their beats online. Trakjungle is currently in demo.",
          wip: true,
          link: "http://trakjungle.com",
          screen:
            "https://res.cloudinary.com/house16-design-studio/image/upload/v1608571819/portfolio/trakjungle-screen-new.png"
        }
      ],

      showOverlay: false
    };
  },

  components: {
    SingleWork
  },

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
.works {
  position: relative;
}
.work {
  width: 100%;
  height: 200px;
  background-size: cover;
  background-position: center;
  position: relative;
}

.work-overlay {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.9);
}

.in-progress-tag {
  position: absolute;
  right: 5%;
  top: 3%;
  padding: 2px 4px;
  background-color: #1976d2;
  border-radius: 5px;
}

.overlay-inner {
  padding: 5px 10px;
  margin-top: 15px;
}

.work-title,
.work-description,
.work-action {
  text-align: center;
}
</style>
