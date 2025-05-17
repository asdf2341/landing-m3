<template>
 <button class="scroll-to-top">
      <svg class="scroll-arrow" width="10" height="16" viewBox="0 0 10 13" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M5.00049 0.414062L0.293494 5.12106C-0.0975059 5.51206 -0.0975059 6.14406 0.293494 6.53506C0.684494 6.92606 1.31649 6.92606 1.70749 6.53506L4.00049 4.24206V11.8281C4.00049 12.3801 4.44749 12.8281 5.00049 12.8281C5.55349 12.8281 6.00049 12.3801 6.00049 11.8281V4.24206L8.29349 6.53506C8.48849 6.73006 8.74449 6.82806 9.00049 6.82806C9.25649 6.82806 9.5125 6.73006 9.70749 6.53506C10.0985 6.14406 10.0985 5.51206 9.70749 5.12106L5.00049 0.414062Z" fill="#414651"/>
        </svg>
        
    </button>

  </template>
    <script>
import { onMounted } from 'vue'

export default {
  name: 'Projects',
  setup() {
    // Lifecycle hook: Runs once after the component is mounted (DOM is ready)
    onMounted(() => {
      // Get the scroll-to-top button from the DOM
      const button = document.querySelector('.scroll-to-top')

      // Add scroll event listener to the window
      window.addEventListener('scroll', () => {
        const scrollY = window.scrollY || document.documentElement.scrollTop

        if (button) {
          // Show the button if scroll is more than 300px
          button.style.display = scrollY > 300 ? 'block' : 'none'
        }
      })

      // Add click listener to the button for smooth scroll to top
      if (button) {
        button.addEventListener('click', (e) => {
          e.preventDefault()
          window.scrollTo({
            top: 0,
            behavior: 'smooth',
          })
        })
      }
    })
  },
}
</script>


