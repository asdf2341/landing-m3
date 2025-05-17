<template>
   <section class="projects-wrapper " id="projects">
        <div class="projects-container">
          <div class="header-content  container">
            <h3 class="projects-heading">Latest projects</h3>
            <h2 class="header-name">Innovations we’re proud of</h2>
            <p class="projects-description">
              Explore our portfolio of innovative, tailored solutions delivering
              exceptional results for our clients.
            </p>
          </div>
          <div class="button-project">
          <div class="projects-grid" id="project-container">
            <!-- Project 1 -->
            <article class="project-card">
             
            </article>

            <!-- Project 2 -->
           
          </div>

          <button
            class="view-all-btn"
          @click="goToProjectsPage"
          >
            View all projects
          </button>
        </div>
        </div>
      </section>
</template>



<script>
import { ref, onMounted } from 'vue'

export default {
  name: 'Projects',
  setup() {
    const projects = ref([])
    const goToProjectsPage = () => {
  window.location.href = 'projectsW1440.html'
}
    const fetchProjects = async () => {
      try {
        const response = await fetch('./projects.json')
        if (!response.ok) {
          throw new Error(`HTTP error! Status: ${response.status}`)
        }
        const data = await response.json()

        if (!data || typeof data !== 'object' || !Array.isArray(data.result)) {
          throw new Error("Invalid JSON structure: 'result' key missing or not an array")
        }

        projects.value = shuffleArray(data.result).slice(0, 3)
      } catch (error) {
        console.error('Error fetching articles:', error)
      }
    }

    const shuffleArray = (array) => {
      for (let i = array.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1))
        ;[array[i], array[j]] = [array[j], array[i]]
      }
      return array
    }

    const formatDuration = (days) => {
      if (days < 7) return `${days} days`
      if (days <= 31) return `${Math.round(days / 6)} weeks`
      return `${Math.round(days / 30)} months`
    }

    onMounted(() => {
      fetchProjects()
    })

    return { projects, formatDuration }
  }
}
</script>



<style>
</style>