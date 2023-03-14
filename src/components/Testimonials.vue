<script>
import NavBar from './NavBar.vue'
// Should inherit from app. 
export default {
    data() {
        return {
            hotdog: this.hotdog,
        }
    },
    props: {
        hotdog: String
    },
    components: {NavBar},

}
</script>

<template>
  <header>
    <NavBar></NavBar>

  </header>
  <h4>Testimonials</h4>
  This is the testimonials page.
</template>

<style scoped>
</style>
