<template>
  <div class="events">
    <EventStudentname v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventStudentname from '@/components/EventStudentname.vue'
import EventStudent from '@/services/EventStudent.js'
export default {
  name: 'student',
  components: {
    EventStudentname
    // register it as a child component
  },
  data() {
    return {
      events: null
    }
  },
  created() {
    EventStudent.getEvents()
      .then((response) => {
        this.events = response.data
      })
      .catch((error) => {
        console.log(error)
      })
  }
}
</script>
<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
