<template>
  <router-link
    class="event-link"
    :to="{ name: 'EventDetails', params: { id: event.id } }"
  >
    <div class="event-card">
      <span>@{{ event.time }} on {{ event.date }}</span>
      <h4>{{ event.title }}</h4>
    </div>
  </router-link>
</template>

<script>
export default {
  name: 'EventCard',
  props: {
    event: {
      type: Object,
    },
  },
  data() {
    return {}
  },
}
</script>

<style scoped>
.event-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid hsl(213, 23%, 70%);
  border-radius: 5px;
  transition: all 0.3s ease-in-out;
}

.event-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}

.event-card > span {
  color: hsl(213, 23%, 50%);
}

.event-card h4 {
  color: hsl(213, 23%, 20%);
}

.event-link {
  text-decoration: none;
}
</style>
