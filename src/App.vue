<template>
  <div id="app" class="min-h-screen w-full bg-gray-200">
    <main>
      <component
        v-for="(component, index) in page.components"
        :key="index"
        :is="component.name"
        v-bind="component.props"
      />
    </main>
  </div>
</template>

<script>
import About from "./components/About";
import Contact from "./components/Contact";
import Features from "./components/Features";
import Hero from "./components/Hero";
import Services from "./components/Services";
import Team from "./components/Team";
export default {
  name: "App",
  components: {
    About,
    Contact,
    Features,
    Hero,
    Services,
    Team
  },
  data() {
    return {
      page: {
        components: [
          {
            name: "Hero",
            props: {}
          },
          {
            name: "Features",
            props: {}
          },
          {
            name: "About",
            props: {}
          },
          {
            name: "Team",
            props: {}
          },
          {
            name: "Services",
            props: {}
          },
          {
            name: "Contact",
            props: {}
          }
        ]
      }
    };
  }
};
</script>

<style>
</style>
