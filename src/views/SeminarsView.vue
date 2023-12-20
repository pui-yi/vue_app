<template>
   <h1>Our Seminars in December</h1>
   <div v-for="evt in events" :key="evt.id" class="event">
        <router-link :to="{ name: 'Details', params: { id: evt.id }}">
            <h2>{{ evt.title }}</h2>
        </router-link>
   </div>
</template>

<script>
import events from '../events.json'
export default {
    data() {
        return {
            events: events
        }
    }
}
</script>

<style>
.event {
    margin-bottom: 1rem;
    padding: 1rem;
    background-color: azure;
}

</style>