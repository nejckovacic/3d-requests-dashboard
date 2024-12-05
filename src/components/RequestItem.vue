<template>
    <div class="request-item">
      <!-- First Row: Title and Status -->
      <div class="request-header">
        <h3 class="request-title">{{ request.name }}</h3>
        <p :class="statusClass" class="request-status">
          {{ request.status ? "Complete" : "Incomplete" }}
        </p>
      </div>
  
      <!-- Second Row: Short Description -->
      <p class="request-description">
        {{ request.shortDescription }}
      </p>
  
      <!-- Third Row: Date -->
      <p class="request-date">
        Date: {{ formattedDate }}
      </p>
  
      <!-- Fourth Row: Buttons -->
      <div class="request-actions">
        <button @click="toggleDetails">
          {{ isExpanded ? "Hide Details" : "Show Details" }}
        </button>
        <a :href="request.link" target="_blank" class="link-icon">
          🔗
        </a>
      </div>
  
      <!-- Expandable Long Description -->
      <transition name="fade">
        <div v-if="isExpanded" class="request-details" v-html="request.longDescription"></div>
      </transition>
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
    computed: {
      statusClass() {
        return this.request.status ? "complete" : "incomplete";
      },
      formattedDate() {
        return new Date(this.request.date).toLocaleDateString();
      }
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
    background-color: #ffffff;
    border: 1px solid #d9d9d9;
    border-radius: 8px;
    padding: 1rem;
    margin-bottom: 1rem;
    box-shadow: 0px 2px 6px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
  }
  
  /* Title and Status Row */
  .request-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 0.5rem;
  }
  
  .request-title {
    font-size: 1.25rem;
    font-weight: bold;
  }
  
  .request-status {
    font-weight: bold;
    padding: 0.3rem 0.6rem;
    border-radius: 5px;
  }
  
  .complete {
    color: green;
    background-color: rgba(0, 128, 0, 0.1);
  }
  
  .incomplete {
    color: red;
    background-color: rgba(255, 0, 0, 0.1);
  }
  
  /* Description Row */
  .request-description {
    margin: 0.5rem 0;
    font-size: 1rem;
    color: #555;
  }
  
  /* Date Row */
  .request-date {
    margin-bottom: 0.5rem;
    font-size: 0.9rem;
    color: #888;
  }
  
  /* Buttons Row */
  .request-actions {
    display: flex;
    justify-content: center;
    gap: 1rem;
    margin-top: 0.5rem;
  }
  
  button {
    border-radius: 8px;
    border: 1px solid transparent;
    padding: 0.6em 1.2em;
    font-size: 1em;
    font-weight: 500;
    background-color: #646cff;
    color: white;
    cursor: pointer;
    transition: all 0.25s;
  }
  button:hover {
    background-color: #535bf2;
  }
  
  .link-icon {
    font-size: 1.5rem;
    text-decoration: none;
    color: #646cff;
    transition: color 0.3s;
  }
  .link-icon:hover {
    color: #535bf2;
  }
  
  /* Expandable Long Description */
  .request-details {
    margin-top: 0.5rem;
    background-color: #f3f3f3;
    padding: 0.5rem;
    border-radius: 6px;
  }
  
  /* Markdown Content Styling */
  .markdown-content {
    margin: 0;
    padding: 0;
    font-size: 0.95rem;
    color: #555;
    white-space: pre-wrap;
  }
  
  /* Headings */
  .markdown-content h1,
  .markdown-content h2,
  .markdown-content h3 {
    margin: 0.5rem 0;
    font-size: 1.1rem;
    font-weight: bold;
  }
  
  /* Paragraphs */
  .markdown-content p {
    margin: 0.5rem 0;
    line-height: 1.5;
  }
  
  /* Lists */
  .markdown-content ul {
    margin: 0.5rem 0 0.5rem 1rem;
    padding: 0;
    list-style-type: disc;
  }
  
  /* Links */
  .markdown-content a {
    color: #646cff;
    text-decoration: none;
  }
  .markdown-content a:hover {
    color: #535bf2;
  }
  
  /* Fade Transition */
  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 0.3s ease;
  }
  .fade-enter-from,
  .fade-leave-to {
    opacity: 0;
  }
  </style>
  