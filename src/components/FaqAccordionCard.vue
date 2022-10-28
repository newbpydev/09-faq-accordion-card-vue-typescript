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
  <article class="faq">
    <div class="faq-card">
      <!-- # faq__illus-container -->
      <div class="faq-card__illus-container">
        <div class="faq-card__illus" aria-hidden="true" role="img" />
        <div class="faq-card__illus-shadow" role="img" aria-hidden="true" />
      </div>
      <div class="faq-card__content-container">
        <!-- # faq__heading -->
        <h1 class="faq-card__heading">FAQ</h1>
        <div class="faq-card__qa-container">
          <!-- # faq__questions-container -->
          <details
            class="faq-card__questions-container"
            v-for="faq in faqs"
            :key="faq.id"
          >
            <summary class="faq-card__question active">
              {{ faq.question }}
              <img
                class="faq-card__icon"
                :src="iconArrowDown"
                alt="click to reveal answer"
              />
            </summary>
            <p class="faq-card__answer">{{ faq.answer }}</p>
          </details>
        </div>
      </div>
    </div>
  </article>
</template>

<!-- * STYLE -->
<style scoped>
.faq {
  margin-top: 6.3rem;
}
.faq-card {
  position: relative;
  width: 32.7rem;
  height: 53.5rem;
  padding: 13.2rem 2.4rem 4.8rem;
  background: #fff;
  border-radius: var(--border-radius);

  /* TODO: add top margin to match design */
  box-shadow: 0 5rem 5rem -2rem rgba(53 18 122 / 0.497159);
}
.faq-card__illus-container {
  position: absolute;
  top: -10.8rem;
  left: 50%;
  transform: translate(-50%);
  width: 23.7rem;
  height: auto;
}

.faq-card__illus {
  z-index: 5;
  height: 18rem;
  width: auto;
  background-image: url("@/assets/images/illustration-woman-online-mobile.svg");
}
.faq-card__illus::after {
  z-index: -1;
  content: "";
  position: absolute;
  top: 3rem;
  height: 0rem;
  background: transparent;
  width: 100%;
  box-shadow: 0 10rem 7rem 1rem rgba(53 18 122 / 0.497159);
}
.faq-card__illus-shadow {
  z-index: -1;
  position: absolute;
  top: 10.8rem;
  left: 0rem;

  width: 24rem;
  height: 14.5rem;

  background-image: url("@/assets/images/bg-pattern-mobile.svg");
  background-repeat: no-repeat;
}

.faq-card__heading {
  font-size: 3.2rem;
  text-align: center;
  font-weight: 700;
  color: var(--pri-blue-very-dark-desaturated);
  margin-bottom: 1.9rem;
}

.faq-card__questions-container {
  border-bottom: 1px solid var(--dividers-blue-light-grayish);
  padding: 1.2rem 0;
}

.faq-card__qa-container {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 29.5rem;
}
.faq-card__question {
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 1.3rem;
  line-height: 1.6;
  color: var(--neut-blue-very-dark-grayish);
  letter-spacing: 0.01rem;
  cursor: pointer;
  transition: margin 0.5s ease;
}

.faq-card__question:hover {
  color: var(--pri-red-soft);
}

details[open] > .faq-card__question {
  font-size: 1.3rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
  color: var(--pri-blue-very-dark-desaturated);
}

.faq-card__icon {
  width: 0.8rem;
  transition: all 0.3s;
  /* height: 0.4rem */
}
details[open] .faq-card__icon {
  transform: rotate(180deg);
}

.faq-card__answer {
  color: var(--neut-blue-dark-grayish);
  width: 95%;
  opacity: 0;
  line-height: 1.8;
  letter-spacing: 0.004rem;
  transition: all 3s ease;
}

details[open] .faq-card__answer {
  opacity: 1;
}

/* 1440 = 90em */
@media (min-width: 90em) {
  .faq {
    position: relative;
    margin-top: 0;
  }

  .faq-card {
    width: 92rem;
    height: 50.9rem;
    padding: 6.5rem 9.5rem 8.3rem 47.5rem;
    margin-left: 4.5rem;
    overflow: hidden;
  }

  .faq::before {
    content: "";
    position: absolute;
    top: 20.3rem;
    left: -4.8rem;
    height: 15rem;
    width: 19.1rem;
    z-index: 99;

    background-image: url("@/assets/images/illustration-box-desktop.svg");
  }
  .faq::after {
    content: "";
    position: absolute;
    top: 18rem;
    left: 0.3rem;
    width: 9rem;
    height: 0rem;
    box-shadow: 0 12rem 3.5rem 0.5rem rgb(0 0 0);
  }

  .faq-card__illus-container {
    top: 48.7%;
    left: -6.7%;
    transform: translate(-10%, -50%);
  }

  .faq-card__illus {
    position: relative;
    height: 35.9rem;
    width: 47.2rem;
    background-image: url("@/assets/images/illustration-woman-online-desktop.svg");
  }

  .faq-card__illus-shadow {
    position: absolute;
    top: -36.5rem;
    left: -49.2rem;
    height: 94.4rem;
    width: 97rem;
    background-image: url("@/assets/images/bg-pattern-desktop.svg");
    background-repeat: no-repeat;
  }

  .faq-card__heading {
    text-align: left;
  }

  .faq-card__questions-container {
  }

  .faq-card__question {
    font-size: 1.4rem;
    padding-right: 1.7rem;
  }

  details[open] > .faq-card__question {
    font-size: 1.4rem;
  }

  .faq-card__answer {
  }
}
</style>
