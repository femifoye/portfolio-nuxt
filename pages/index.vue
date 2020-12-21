<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <div class="text-center">
        <img
          id="avatar"
          src="~/assets/images/femi-bitmoji.png"
          alt="Femi Abdul - Software Enigneer"
        />
      </div>
      <v-card>
        <v-card-title class="headline">
          <div class="sub-heading w-100 mb20">
            <h4 class="text-center">
              Hi, I'm Femi <span class="hand">🖐🏽</span>
            </h4>
          </div>
          <div class="big-heading text-center">
            <h3>
              Frontend Engineer with a passion for building digital experiences
            </h3>
            <div class="heading-icons text-center mt20">
              <a class="github" :href="githubLink"
                ><i class="icon-32 lab la-github"></i
              ></a>
              <a class="linkedin" :href="linkedinLink"
                ><i class="icon-32 lab la-linkedin"></i
              ></a>
              <a class="twitter" :href="twitterLink"
                ><i class="icon-32 lab la-twitter"></i
              ></a>
            </div>
          </div>
        </v-card-title>
        <v-card-text> </v-card-text>
      </v-card>
      <v-card class="panels">
        <panel
          dark
          class="panel mb10"
          v-for="pan in panels"
          :component="pan.component"
          :title="pan.title"
          :key="pan.id"
        ></panel>
      </v-card>
      <div class="contact">
        <h4>Interested in working with me?</h4>
        <a href="mailto:femi.html@gmail.com"
          ><button class="btn btn-email">Contact</button></a
        >
      </div>
    </v-col>
  </v-row>
</template>

<script>
import Logo from "~/components/Logo.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";
import Panel from "../components/Panel";

export default {
  data: () => {
    return {
      githubLink: "https://github.com/femifoye",
      twitterLink: "https://twitter.com/femifoye",
      linkedinLink: "https://linkedin.com/in/taofeek-femi-abdul",
      panels: [
        { id: 1, title: "About Me", component: "about" },
        { id: 2, title: "Work", component: "work" },
        { id: 3, title: "Tech Stack", component: "stack" }
      ]
    };
  },
  components: {
    Logo,
    VuetifyLogo,
    Panel
  }
};
</script>

<style scoped>
.big-heading h3 {
  word-break: break-word;
}

.theme--dark.v-card .panel {
  border-bottom: 1px solid grey;
}

.theme--light.v-card .panel {
  border-bottom: 1px solid #121212;
}

.hand {
  position: absolute;
  animation-name: wave;
  animation-duration: 3s;
  animation-iteration-count: infinite;
  margin: 0 5px;
}

.contact {
  text-align: center;
  padding: 20px 0;
}

@keyframes wave {
  0% {
    transform: rotate(0);
  }
  25% {
    transform: rotate(-45deg);
  }
  50% {
    transform: rotate(45deg);
  }
  100% {
    transform: rotate(0);
  }
}
</style>
