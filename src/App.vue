<template>
  <ul>
    <learning-resource
      v-for="res in storedResources"
      :key="res.id"
      :title="res.title"
      :description="res.description"
      :link="res.link"
    ></learning-resource>
  </ul>
</template>
<script>
import LearningResource from "./components/learning-resources/LearningResource.vue";
export default {
  components: { LearningResource },
  data() {
    return {
      storedResources: [
        {
          id: "official-guide",
          title: "Official Guide",
          description: "The official vue.js documentation",
          link: "http://vuejs.org",
        },
        {
          id: "Google",
          title: "Google",
          description: "Learn to google",
          link: "http://google.org",
        },
      ],
    };
  },
};
</script>
