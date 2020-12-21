<template>
  <div class="about-me">
    <p>
      I'm Femi Abdul, A frontend developer with 4+ years of experience working
      with frontend technologies. I am currently based in
      <span class="highlight"
        >Dublin, Ireland
        <img
          class="img-12"
          src="https://img.icons8.com/color/48/000000/ireland.png"
        />
      </span>
      and open to new work opportunities. <br />
    </p>

    <p>
      My journey into Frontend development started with me tinkering with
      websites through the web browser console. I began recreating these
      websites to the best of my knowledge and got better one bug at a time.
    </p>

    <p>
      Alongisde my frontend background, I also have experience working with
      backend technologies, primarily using Ruby on Rails, Postgres, NodeJS,
      Python. These have proved to come in handy when i find myself working
      across the development spectrum.
    </p>

    <p>
      At the moment, I mostly write VueJS, Nuxt (for SSR), and Ruby on Rails. I
      also have experience writing React, Python, and PHP/Laravel.
    </p>

    <p>
      In my free time, i enjoy playing the piano and finding new places to eat.
    </p>
  </div>
</template>

<script>
export default {
  data: () => {
    return {};
  },

  components: {}
};
</script>

<style scoped>
.theme--dark.v-card .highlight {
  background-color: white;
  color: #121212;
  padding: 0 2px;
}

.theme--light.v-card .highlight {
  background-color: #121212;
  color: white;
  padding: 0 2px;
}
</style>
