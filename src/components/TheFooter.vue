<template>
  <footer class="text-medium-gray">
    <div class="container">
      <div class="row">
        <div class="col">
          <h6 class="text-dark fw-bold">Address</h6>
          <address>
            382 NE 191st St # 87394 Miami, FL 33179-3899<br>
            +1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)<br>
            <a href="support@maxcoach.com">support@maxcoach.com</a>
          </address>

          <div>
            <i v-for="(socialIcon, i) in socialIcons" :key="i" :class="socialIcon"></i>
          </div>
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
      exploreList: ["Start here", "Blog", "About us", "Success story", "Courses", "Contact us"],
      informationList: ["Membership", "Purchase guide", "Privacy policy", "Terms of services"],
      socialIcons: ["fa-brands fa-facebook-square", "fa-brands fa-twitter", "fa-brands fa-instagram", "fa-brands fa-linkedin"]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables";
@import "../assets/scss/utilities";

a {
  color: $medium-gray;
  text-decoration: none;

  &:hover {
    color: $dark-gray;
    text-decoration: underline;
  }
}

i {
  margin-right: 1.5rem;
  color: $light-gray;
}

</style>