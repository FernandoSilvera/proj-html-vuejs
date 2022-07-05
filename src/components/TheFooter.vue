<template>
  <footer class="text-dark-gray">
    <div class="container">
      <div class="row">
        <div class="col-6">
          <h6 class="text-dark fw-bold">Address</h6>
        </div>

        <div class="col">
          <h6>Explore</h6>
        </div>

        <div class="col">
          <!-- "EXPLORE" second column -->
        </div>

        <div class="col">
          <h6>Information</h6>
        </div>
      </div>

      <div class="row">
        <div class="col-6">
          <address>
            382 NE 191st St # 87394 Miami, FL 33179-3899<br>
            +1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)<br>
            <a href="support@maxcoach.com">support@maxcoach.com</a>
          </address>

          <div>
            <i v-for="(socialIcon, i) in socialIcons" :key="i" :class="socialIcon"></i>
          </div>
        </div>

        <div class="col">
          <ul>
            <li v-for="(exploreLink, i) in exploreLinks" :key="i">
              <a v-if="i <= 2" href="#">{{ exploreLink }}</a>
            </li>
          </ul>
        </div>

        <div class="col">
          <ul>
            <li v-for="(exploreLink, i) in exploreLinks" :key="i">
              <a v-if="i >= 3" href="#">{{ exploreLink }}</a>
            </li>
          </ul>
        </div>

        <div class="col">
          <ul>
            <li v-for="(informationLink, i) in informationLinks" :key="i">
              <a href="#">{{ informationLink }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "TheFooter",
  data() {
    return {
      exploreLinks: ["Start here", "Blog", "About us", "Success story", "Courses", "Contact us"],
      informationLinks: ["Membership", "Purchase guide", "Privacy policy", "Terms of services"],
      socialIcons: ["fa-brands fa-facebook-square", "fa-brands fa-twitter", "fa-brands fa-instagram", "fa-brands fa-linkedin"]
    }
  },
  computed: {}
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables";
@import "../assets/scss/utilities";

a {
  color: $dark-gray;
  text-decoration: none;

  &:hover {
    color: $darker-gray;
    text-decoration: underline;
  }
}

h6 {
  color: black;
  font-weight: bold;
}

i {
  margin-right: 1.5rem;
  color: $light-gray;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

</style>