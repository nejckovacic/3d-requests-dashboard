<template>
    <div class="request-item">
        <div class="request-summary">
            <h3>{{ request.name }}</h3>
            <p>Status: {{ request.status ? "Complete" : "Incomplete" }}</p>
            <button @click="toggleDetails">
                {{ isExpanded ? "Hide Details" : "Show Details" }}
            </button>
        </div>
        <div v-if="isExpanded" class="request-details">
            <p>{{ request.description }}</p>
            <a :href="request.link" target="_blank">View Design</a>
        </div>
    </div>
</template>

<script>
export default {
    name: "RequestItem",
    props: {
        request: Object
    },
    data() {
        return {
            isExpanded: false
        };
    },
    methods: {
        toggleDetails() {
            this.isExpanded = !this.isExpanded;
        }
    }
};
</script>

<style scoped>
.request-item {
    border: 1px solid #ccc;
    padding: 15px;
    margin-bottom: 15px;
    border-radius: 5px;
}
</style>