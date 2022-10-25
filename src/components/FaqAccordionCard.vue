<!-- * SCRIPT -->
<script setup lang="ts">
import { ref } from "vue";

// images
import illusBoxDesktop from "@/assets/images/illustration-box-desktop.svg";
import illusWomanDesktop from "@/assets/images/illustration-woman-online-desktop.svg";
import illusWomanMobile from "@/assets/images/illustration-woman-online-mobile.svg";

import bgPatternDesktop from "@/assets/images/bg-pattern-desktop.svg";
import bgPatternMobile from "@/assets/images/bg-pattern-mobile.svg";

import iconArrowDown from "@/assets/images/icon-arrow-down.svg";

const faqs = ref([
  {
    id: 1,
    question: "How many team members can I invite?",
    answer:
      "You can invite up to 2 additional users on the Free plan. There is no limit on team members for the Premium plan.",
  },
  {
    id: 2,
    question: "What is the maximum file upload size?",
    answer:
      "No more than 2GB. All files in your account must fit your allotted storage space.",
  },
  {
    id: 3,
    question: "How do I reset my password?",
    answer:
      "Click “Forgot password” from the login page or Change password” from your profile page. A reset link will be emailed to you.",
  },
  {
    id: 4,
    question: "Can I cancel my subscription?",
    answer:
      "Yes! Send us a message and we'll process your request no questions asked.",
  },
  {
    id: 5,
    question: "Do you provide additional support?",
    answer:
      "Chat and email support is available 24/7. Phone lines are open during normal business hours.",
  },
]);
</script>

<!-- * TEMPLATE -->
<template>
  <!-- @ faq -->
  <article class="faq-card">
    <!-- # faq__illus-container -->
    <div class="faq-card__illus-container">
      <img
        class="faq-card__illus"
        :src="illusWomanMobile"
        alt=""
        aria-hidden="true"
      />
      <img
        class="faq-card__illus-shadow"
        :src="bgPatternMobile"
        alt=""
        aria-hidden="true"
      />
    </div>

    <div class="faq-card__content-container">
      <!-- # faq__heading -->
      <h1 class="faq-card__heading">FAQ</h1>
      <!-- # faq__questions-container -->
      <div
        class="faq-card__questions-container"
        v-for="faq in faqs"
        :key="faq.id"
      >
        <h2 class="faq-card__question">
          {{ faq.question }}
          <img
            class="faq-card__icon"
            :src="iconArrowDown"
            alt="click to reveal answer"
          />
        </h2>
        <p class="faq-card__answer">{{ faq.answer }}</p>
      </div>
    </div>
  </article>
</template>

<!-- * STYLE -->
<style scoped>
.faq-card {
  position: relative;
  max-width: 32.7rem;
  height: 53.5rem;
  padding: 13.2rem 2.4rem 4.8rem;
  background: #fff;
  border-radius: var(--border-radius);

  /* TODO: add top margin to match design */
  box-shadow: 0 5rem 5rem -2rem rgba(53 18 122 / 0.497159);
}

.faq-card__illus {
  z-index: 5;
}
.faq-card__illus-shadow {
  z-index: -1;
  position: absolute;
  bottom: -3rem;
  left: 0;
}
.faq-card__illus-container {
  position: absolute;
  top: -10.5rem;
  left: 50%;
  transform: translate(-50%);
  width: 23.7rem;
  height: auto;
}

.faq-card__heading {
  font-size: 3.2rem;
  text-align: center;
  font-weight: 700;
  color: var(--pri-blue-very-dark-desaturated);
}

.faq-card__questions-container {
}
.faq-card__question {
}
.faq-card__icon {
}
.faq-card__answer {
}
</style>
