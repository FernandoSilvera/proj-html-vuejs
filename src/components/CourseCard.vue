<template>
  <div class="card my-card mb-3" style="max-width: 540px;">
    <div class="row g-0">
      <div class="col-md-4 my-div">
        <img :src="`/img/course-${img}.jpg`" class="img-fluid rounded-start" :alt="title">
      </div>
      <div class="col-md-8">
        <div class="card-body">
          <h5 class="card-title">{{ price }}</h5>
          <p class="card-text">{{ title }}</p>
          <p class="card-text"><small class="text-muted">{{ lessons }} Lessons</small></p>
          <p class="card-text"><small class="text-muted">{{ students }} Students</small></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CourseCard",
  props: {
    img: Number,
    price: String,
    title: String,
    lessons: Number,
    students: Number
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables";
@import "../assets/scss/utilities";

.card {
  border: 0px;
}

.my-div {
    border-radius: 50%;
    overflow: hidden;
  }
</style>