<template>
  <main>
    <section id="jumbotron" class="text-center py-5">
      <div class="container">
        <h1 class="text-light">Learn At Your Own Pace!</h1>
        <p class="text-light-gray mb-4">Get teamed up with people of the same will.</p>
        <button class="btn btn-primary my-btn-primary">Get started for free</button>
      </div>
    </section>

    <section id="courses" class="bg-lighter-gray py-5">
      <div class="container">
        <div class="text-center py-3">
          <div class="mb-3"><span class="subtitle">Choose a course to get started</span></div>
          <h2>Latest Featured <span class="text-primary">Courses</span></h2>
        </div>

        <div class="row flex-wrap mb-5">
          <CourseCard v-for="(course, i) in coursesList" :key="i"
          :img="course.image"
          :price="course.price"
          :title="course.title"
          :lessons="course.lessons"
          :students="course.students">
          </CourseCard>
        </div>

        <div class="text-center mb-3">
          <button class="btn btn-primary my-btn-primary">View all courses -></button>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import CourseCard from './CourseCard.vue'

export default {
  name: "TheMain",
  components: {
    CourseCard,
  },
  data() {
    return {
      coursesList: [
        {
          image: 0,
          price: "$40.00",
          title: "Learning to Write as a Professional Author",
          lessons: 20,
          students: 50
        },
        {
          image: 1,
          price: "Free",
          title: "Customer-centric Info-Tech Strategies",
          lessons: 24,
          students: 769
        },
        {
          image: 2,
          price: "$19.00",
          title: "Open Programming Courses for Everyone: Python",
          lessons: 17,
          students: 62
        },
        {
          image: 3,
          price: "$26.00",
          title: "Academic Listening and Note-taking",
          lessons: 14,
          students: 67
        },
        {
          image: 4,
          price: "$39.00",
          title: "Master jQuery in a Short Period of Time",
          lessons: 6,
          students: 51
        },
        {
          image: 5,
          price: "$59.00",
          title: "Introduction to Javascript for Beginners",
          lessons: 14,
          students: 76
        },
      ]
    }
  }
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

  &:hover {
    background-color: white;
    color: $primary;
  }
}
</style>