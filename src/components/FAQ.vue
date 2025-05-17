<template>
  <section class="faq-section" id="faq">
    <div class="faq-header container">
      <h2 class="header-name">Frequently asked questions</h2>
      <p class="projects-description">
        Answers to the most common questions about our services and processes.
      </p>
    </div>

    <div class="faq-container container">
      <div
        class="faq-item"
        v-for="(item, index) in faqData"
        :key="index"
        :class="{ 'show-answer': openIndex === index }"
      >
        <div class="faq-question" @click="toggle(index)">
          <span class="questions">{{ item.question }}</span>
          <span class="toggle-container">
            <span class="expand" v-if="openIndex !== index">
              <img src="@/assets/plus-circle.svg" alt="Toggle Icon" />
            </span>
            <span class="close" v-else>
              <img src="@/assets/minus-circle.svg" alt="Toggle Icon" />
            </span>
          </span>
        </div>
        <div class="faq-answer" v-if="openIndex === index">
          <span class="answer">{{ item.answer }}</span>
        </div>
      </div>
    </div>
  </section>
</template>




<script setup>
import { ref } from 'vue'

const faqData = [
  {
    question: 'Do you develop both websites and mobile apps?',
    answer:
      'Yes, we specialize in developing both websites and mobile applications...',
  },
  {
    question: 'How long does it take to develop a project?',
    answer:
      'The time required to develop a project depends on its complexity and scope...',
  },
  {
    question: 'What technologies do you use?',
    answer:
      'We use a wide range of technologies depending on the project requirements...',
  },
  {
    question: 'Can you redesign an existing website or app?',
    answer:
      'Yes, we specialize in redesigning existing websites and mobile apps...',
  },
  {
    question: 'Do you provide post-launch support?',
    answer:
      'Yes, we provide comprehensive post-launch support...',
  },
  {
    question: 'How do I get a quote for my project?',
    answer:
      'To get a quote for your project, simply reach out to us with your project details...',
  },
]

const openIndex = ref(null)

function toggle(index) {
  openIndex.value = openIndex.value === index ? null : index
}

</script>


<style>


</style>