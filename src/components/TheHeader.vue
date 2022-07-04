<template>
  <header class="bg-dark-purple py-3">
    <div class="container">
      <div class="row align-items-center">
        <div class="col">
          <img src="/img/light-logo.png" alt="logo maxcoach">
        </div>

        <div class="col-9">
          <nav>
            <ul class="m-0">
              <li v-for="(navLink, i) in navLinks" :key="i">
                <a href="#">{{ navLink }}</a>
                <i class="fa-solid fa-angle-down fa-2xs my-angle-down"></i>
              </li>
              <li><i class="fa-solid fa-cart-shopping fa-2xs"></i></li>
              <li><i class="fa-solid fa-user"></i></li>
              <li>
                <div>
                <input type="text" placeholder="Search..." aria-label="Search" aria-describedby="button-addon2">
                <button class="btn bg-white" type="button" id="button-addon2"><i class="fa-solid fa-magnifying-glass"></i></button>
                </div>
              </li>
            </ul>
          </nav>
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

img {
  width: 50%;
}

li {
  display: inline-block;
  margin-right: 1.5rem;
  color: white;

  a {
    margin-right: 4px;
    color: white;
    text-decoration: none;

    &:hover {
      text-decoration: underline;
    }
  }

  .my-angle-down {
    vertical-align: middle;
  }
}
</style>