<template>
  <div class="event-card">
    <h5>student name : {{ event.name }}</h5>
    <h5>Surname: {{ event.surname }}</h5>
    <h4>GPA : {{ event.gpa }}</h4>
  </div>
</template>

<script>
export default {
  name: 'EventStudentname',
  props: {
    event: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.event-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
}
.event-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}
</style>
