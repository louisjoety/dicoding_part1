<template>
  <div class="course-search">
    <input v-model="searchQuery" placeholder="Search courses..." />
    <ul>
      <li v-for="course in filteredCourses" :key="course.id">
        <h3>{{ course.name }}</h3>
        <p>{{ course.summary }}</p>
        <a :href="course.course_link" target="_blank" rel="noopener">Learn More</a>
      </li>
    </ul>
  </div>
</template>

<script>
import coursesData from './courses.json';

export default {
  data() {
    return {
      searchQuery: '',
      courses: coursesData,
    };
  },
  computed: {
    filteredCourses() {
      const query = this.searchQuery.toLowerCase();
      return this.courses.filter(
        (course) =>
          course.name.toLowerCase().includes(query) ||
          course.summary.toLowerCase().includes(query) ||
          course.description.toLowerCase().includes(query)
      );
    },
  },
};
</script>

<style scoped>
/* Add your component-specific styles here */
</style>
