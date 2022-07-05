<template>
  <main>
    <section id="jumbotron" class="text-center py-5">
      <div class="container">
        <h1 class="text-light">Learn At Your Own Pace!</h1>
        <p class="text-light-gray mb-4">Get teamed up with people of the same will.</p>
        <button class="btn btn-primary my-btn-primary">Get started for free</button>
      </div>
    </section>

    <section id="courses" class="py-5">
      <div class="container">
        <div class="text-center py-3">
          <div class="mb-3"><span class="subtitle">Choose a course to get started</span></div>
          <h2>Latest Featured <span class="text-primary">Courses</span></h2>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: "TheMain"
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables";
@import "../assets/scss/utilities";

#jumbotron {
  background-color: $dark-purple;
}

.my-btn-primary {
  padding: 1rem 1.5rem;
  font-size: 14px;
  font-weight: 600;
  color: white;
}
</style>