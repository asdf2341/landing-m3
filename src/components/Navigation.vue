<template>
<header class="primary-header container">
<nav class="primary-nav content hamburger-menu">
  <div class="logo">
    <a href="#"><img src="assets/logoo.svg" alt="logo" /> </a>
    <h1>Applet</h1>
  </div>

  <input id="menu__toggle" type="checkbox" />
  <label class="menu__btn" for="menu__toggle">
    <span></span>
  </label>

  <ul class="menu__box">
    <li><a class="menu__item" href="#about">About</a></li>
    <li><a class="menu__item" href="#projects">Projects</a></li>
    <li><a class="menu__item" href="#faq">FAQ</a></li>
    <li><a class="menu__item" href="#contact">Contacts</a></li>
    <li>
      <input type="checkbox" id="theme-toggle" hidden />
      <label for="theme-toggle" class="theme-switch">
        <svg
          class="sun-svg"
          width="26"
          height="26"
          viewBox="0 0 26 26"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M13 1V3.76923"
            stroke="#535862"
            stroke-width="2"
            stroke-miterlimit="10"
            stroke-linecap="round"
          />
          <path
            d="M13 22.2307V24.9999"
            stroke="#535862"
            stroke-width="2"
            stroke-miterlimit="10"
            stroke-linecap="round"
          />
          <path
            d="M21.4854 4.51465L19.5273 6.47273"
            stroke="#535862"
            stroke-width="2"
            stroke-miterlimit="10"
            stroke-linecap="round"
          />
          <path
            d="M6.47273 19.5273L4.51465 21.4854"
            stroke="#535862"
            stroke-width="2"
            stroke-miterlimit="10"
            stroke-linecap="round"
          />
          <path
            d="M24.9999 13H22.2307"
            stroke="#535862"
            stroke-width="2"
            stroke-miterlimit="10"
            stroke-linecap="round"
          />
          <path
            d="M3.76923 13H1"
            stroke="#535862"
            stroke-width="2"
            stroke-miterlimit="10"
            stroke-linecap="round"
          />
          <path
            d="M21.4854 21.4854L19.5273 19.5273"
            stroke="#535862"
            stroke-width="2"
            stroke-miterlimit="10"
            stroke-linecap="round"
          />
          <path
            d="M6.47273 6.47273L4.51465 4.51465"
            stroke="#535862"
            stroke-width="2"
            stroke-miterlimit="10"
            stroke-linecap="round"
          />
          <path
            d="M13 17.6153C15.549 17.6153 17.6154 15.5489 17.6154 12.9999C17.6154 10.4509 15.549 8.38452 13 8.38452C10.451 8.38452 8.38464 10.4509 8.38464 12.9999C8.38464 15.5489 10.451 17.6153 13 17.6153Z"
            stroke="#535862"
            stroke-width="2"
            stroke-miterlimit="10"
            stroke-linecap="round"
          />
        </svg>
        <svg
          class="moon-svg"
          width="26"
          height="26"
          viewBox="0 0 26 26"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M7.46154 6.07692C7.46154 4.31038 7.72173 2.5225 8.38462 1C3.97519 2.91942 1 7.42231 1 12.5385C1 19.4206 6.57942 25 13.4615 25C18.5777 25 23.0806 22.0248 25 17.6154C23.4775 18.2783 21.6896 18.5385 19.9231 18.5385C13.041 18.5385 7.46154 12.959 7.46154 6.07692Z"
            fill="#94979C"
            stroke="#94979C"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
      </label>
    </li>
  </ul>
</nav>
</header>
</template>

<script>
import { onMounted, ref } from 'vue'

export default {
  setup() {
    const isDark = ref(false)

    onMounted(() => {
      const savedTheme = localStorage.getItem('theme')
      if (savedTheme === 'dark') {
        isDark.value = true
        document.documentElement.setAttribute('data-theme', 'dark')
      }
    })

    const toggleTheme = () => {
      isDark.value = !isDark.value
      document.documentElement.setAttribute('data-theme', isDark.value ? 'dark' : 'light')
      localStorage.setItem('theme', isDark.value ? 'dark' : 'light')
    }

    return { isDark, toggleTheme }
  }
}
</script>



<style>

</style>