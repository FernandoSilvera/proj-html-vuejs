<template>
  <header class="bg-dark-purple">
    <div class="container">
      <div class="row row-cols-3">
        <div class="col">
          <img src="/img/light-logo.png" alt="logo maxcoach">
        </div>

        <div class="col">
          <nav>
            <ul>
              <li v-for="(navLink, i) in navLinks" :key="i">
                <a href="#">{{ navLink }}</a>
                
              </li>
            </ul>
          </nav>
        </div>

        <div class="col">

        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "TheHeader",
  data() {
    return {
      navLinks: ["Home", "Pages", "Courses", "Features", "Blog", "Shop",],
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables";
@import "../assets/scss/utilities";

li {
  display: inline-block;
  margin-right: 1rem;

  a {
    color: white;
    text-decoration: none;
  }
}
</style>