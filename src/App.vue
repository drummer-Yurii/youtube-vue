<template>
    <TheHeader @open-mobile-sidebar="openMobileSidebar" />
    <TheSidebarSmall />
    <TheSidebar />
    <TheSidebarMobile 
      :is-open="isMobileSidebarOpen" 
      @close="closeMobileSidebar" 
    />
    <TheCatigories />
    <TheVideos />
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheSidebarSmall from './components/TheSidebarSmall.vue';
import TheSidebar from './components/TheSidebar.vue';
import TheSidebarMobile from './components/TheSidebarMobile.vue';
import TheCatigories from './components/TheCatigories.vue';
import TheVideos from './components/TheVideos.vue';

export default {
  components: {
      TheHeader,
      TheSidebarSmall,
      TheSidebar,
      TheSidebarMobile,
      TheCatigories,
      TheVideos
  },

  data() {
    return {
      isMobileSidebarOpen: false
    }
  },

  methods: {
    openMobileSidebar() {
      this.isMobileSidebarOpen = true
    },
    closeMobileSidebar() {
      this.isMobileSidebarOpen = false
    }
  },
}
</script>
