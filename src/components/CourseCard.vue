<template>
  <div class="col-6">
    <div class="card my-card mb-3 bg-lighter-gray" style="max-width: 540px;">
      <div class="row g-0">
        <div class="col-md-4">
          <div class="my-div">
            <img :src="`/img/course-${img}.jpg`" class="img-fluid rounded-start" :alt="title">
          </div>
        </div>
        <div class="col-md-8">
          <div class="card-body">
            <h5 class="card-title text-primary">{{ price }}</h5>
            <p class="card-text fw-bold">{{ title }}</p>
            <i class="fa-regular fa-file-lines fa-2xs me-2"></i>
            <p class="card-text me-3 my-card-text"><small class="text-muted">{{ lessons }} Lessons</small></p>
            <i class="fa-regular fa-user fa-2xs me-2"></i>
            <p class="card-text my-card-text"><small class="text-muted">{{ students }} Students</small></p>
          </div>
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
  width: 140px;
  margin: auto;
  border-radius: 50%;
  overflow: hidden;

  img {
    aspect-ratio: 1 / 1;
    object-fit: cover;
  }
}

.my-card-text {
  display: inline-block;
  font-size: 12px;
}

i {
  vertical-align: middle;
}
</style>