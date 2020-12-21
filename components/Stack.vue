<template>
  <div>
    <v-row class="stack">
      <v-col :cols="4" class="tech-stack" v-for="tech in stack" :key="tech.id">
        <div class="stack-image">
          <img :src="tech.icon" alt="" />
        </div>
        <div class="stack-name">
          <h5>{{ tech.name }}</h5>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      stack: [
        {
          id: 1,
          name: "JavaScript",
          icon:
            "https://res.cloudinary.com/house16-design-studio/image/upload/v1608575249/portfolio/javascript-icon.svg"
        },
        {
          id: 2,
          name: "Vue JS",
          icon:
            "https://res.cloudinary.com/house16-design-studio/image/upload/v1608575249/portfolio/vue-icon.svg"
        },
        {
          id: 3,
          name: "React JS",
          icon:
            "https://res.cloudinary.com/house16-design-studio/image/upload/v1608575249/portfolio/react-icon.svg"
        },
        {
          id: 4,
          name: "Ruby On Rails",
          icon:
            "https://res.cloudinary.com/house16-design-studio/image/upload/v1608575249/portfolio/ruby-on-rails-icon.svg"
        },
        {
          id: 5,
          name: "Python",
          icon:
            "https://res.cloudinary.com/house16-design-studio/image/upload/v1608575249/portfolio/python-icon.svg"
        },
        {
          id: 6,
          name: "HTML",
          icon:
            "https://res.cloudinary.com/house16-design-studio/image/upload/v1608575249/portfolio/html-icon.svg"
        }
      ]
    };
  },

  components: {}
};
</script>

<style scoped>
.stack-image img {
  width: 60px;
  height: 60px;
}

.stack {
  text-align: center;
}
</style>
