
<template>
  <div class="sm:px-16 ss:px-12 px-5">
    <Navbar />
    <div class="right-pattern">
      <img
        src="./assets/images/pattern.png"
        alt=""
        class="absolute -right-5 top-0 sm:inline-block hidden"
      />
    </div>
    <Header />
    <Education />
    <Reason />
    <Contact />
    <Events />
    <Comments />
    <Footer />
  </div>
</template>

<script>
import {
  Navbar,
  Header,
  Education,
  Reason,
  Contact,
  Events,
  Comments,
  Footer,
} from "./components";
export default {
  components: { 
    Navbar, 
    Header, 
    Education, 
    Reason, 
    Contact, 
    Events,
    Comments,
    Footer
   },
};
</script>

<style scoped>
</style>
