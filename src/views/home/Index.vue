<template>
  <ContentComponent />
  <SectionFooterComponent />
</template>

<script>
import ContentComponent from "@/components/ContentComponent.vue";
import SectionFooterComponent from "@/components/SectionFooterComponent.vue";

export default {
  name: "HomePage",
  components: {
    ContentComponent,
    SectionFooterComponent,
  },
  mounted() {
    document.title = "Tran Mau Tri Tam | Inspiration"
  }
}
</script>
