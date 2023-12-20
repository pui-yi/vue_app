<template>
  <div v-for="evt in events" :key="evt.id">
      <div v-if="evt.id == id">
          <h1>{{ evt.title }}</h1>
          <p><span class="subtitle">Short description</span>: {{evt.description}}</p>
          <p><span class="subtitle">Location</span>: {{evt.location}}</p>
          <p><span class="subtitle">Start time</span>: {{evt.startTime}}</p>
      </div>
  </div>
</template>

<script>
import events from '../events.json'
export default {
  data() {
    return {
      id: this.$route.params.id,
      events: events
    }
  }
}
</script>

<style>
.subtitle {
  font-weight: bold;
}
</style>