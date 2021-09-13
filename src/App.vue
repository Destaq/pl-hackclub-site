<template>
  <body class="container mx-auto py-2 px-2">
    <div class="py-4">
      <div>
        <h1
          class="
            text-3xl
            mx-auto
            self-center
            justify-center
            text-center
            items-center
            justify-self-center
          "
        >
          Hack Club
        </h1>
        <h2 class="text-2xl mx-auto text-center">
          Park Lane International School
        </h2>
        <h3
          class="
            text-lg
            font-serif font-medium
            text-center
            uppercase
            mt-1.5
            mb-5
          "
        >
          Every Friday | 15:30 - 16:30 | K3
        </h3>
      </div>
      <div>
        <h1 class="font-bold text-2xl mb-5">
          The club for:
          <!-- The words that we want to have typerwriter effect -->
          <span
            class="txt-type"
            data-wait="3000"
            data-words='["coders", "makers", "learners", "hackers", "students"]'
          ></span>
        </h1>
      </div>
    </div>
    <div>
      <div class="">
        <p class="mb-2 -mt-2 italic">Time until next meetup</p>

        <vue-countdown
          :time="time"
          :interval="100"
          v-slot="{ days, hours, minutes, seconds }"
        >
          <div class="grid grid-flow-col gap-5 place-items-end auto-cols-max">
            <div>
              <span class="font-mono text-4xl countdown">
                <span :style="'--value: ' + days"></span>
              </span>
              days
            </div>
            <div>
              <span class="font-mono text-4xl countdown">
                <span :style="'--value:' + hours"></span>
              </span>
              hours
            </div>
            <div>
              <span class="font-mono text-4xl countdown">
                <span :style="'--value:' + minutes"></span>
              </span>
              min
            </div>
            <div>
              <span class="font-mono text-4xl countdown">
                <span :style="'--value:' + seconds"></span>
              </span>
              sec
            </div>
          </div>
        </vue-countdown>
      </div>
      <hr class="my-8 w-1/2 mx-auto" />
      <div
        class="card bg-base-200 lg:card-side bordered -pb-3 mx-auto xl:w-4/5"
      >
        <figure class="h-full">
          <img
            src="https://images.unsplash.com/photo-1555066931-4365d14bab8c?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&h=300&q=100"
            class="object-fill"
          />
        </figure>
        <div class="card-body py-4 lg:py-0 my-auto">
          <h2 class="card-title">About the Club</h2>
          <p>
            At Hack Club, you'll learn new skills, build projects, and connect
            with other Park Lane CS enthusiasts! Anyone from absolute beginner
            to seasoned veteran is welcome to join us.
          </p>
          <p class="mt-3 mb-0 pb-0">
            We're the first national branch of a
            <a class="link" href="https://www.hackclub.com"
              >global high school coding network</a
            >
            that provides hundreds of workshops, hosts hackathons (which we'll
            participate in), and brings teen programmers together.
          </p>
          <div class="flex mt-6">
            <a
              href="mailto:pupil.simon.ilincev@parklane-is.com?cc=pupil.david.sun@parklane-is.com&subject=Dropping%20in%20for%20Hack%20Club&body=Hey%20Simon%20and%20David%2C%0D%0A%0D%0ACount%20me%20in%20for%20this%20Friday's%20PLIS%20Hack%20Club%20session!%20Looking%20forward%20to%20seeing%20you%20there."
              class="btn btn-primary"
              >I'm Coming!</a
            >
            <p class="italic text-sm my-auto ml-2">
              There's free pizza <span class="not-italic">&#127829;</span>, you
              should!
            </p>
          </div>
        </div>
      </div>
    </div>
    <hr class="my-8 mx-auto w-1/2" />
    <div class="lg:grid lg:grid-cols-3 gap-x-4 mt-4 mx-auto">
      <div>
        <p class="text-2xl font-semibold mx-auto">Meet Your Leads</p>
        <p class="my-3">
          A pair of experienced IB Computer Science Higher Level students, we're
          excited about teaching, connecting, and growing with you.
        </p>
        <p class="my-3">
          We've both taken and passed the IGCSE Computer Science exam, and also
          spend a significant amount of time developing our tech skills at home.
        </p>
        <p class="my-3">
          You can read a bit more about our backgrounds here. And if you have
          any questions or concerns, feel free to reach out by email.
        </p>
      </div>
      <div class="mx-auto card bordered w-96 mb-4 md:mb-0 bg-base-200">
        <figure>
          <img src="../public/simon.jpeg" />
        </figure>
        <div class="card-body">
          <h2 class="card-title">
            Simon Ilincev
            <div class="badge mx-2 badge-secondary">12L</div>
          </h2>
          <p>
            Experienced in Python and JavaScript, I focus on full-stack web
            development with Flask, PostgreSQL, and Nuxt.js.
          </p>
          <p class="mt-4">
            I've built Python packages, chess game visualization tools, language
            learning platforms, and more. I look forward to sharing my knowledge
            and connecting with fellow coders!
          </p>
          <p class="mt-4">
            Also anticipating forming teams to join hackathons -
            <a class="link" href="https://devpost.com/software/surgelingo"
              >winning one</a
            >
            this year felt amazing!
          </p>
          <div class="justify-end card-actions grid grid-cols-2 gap-x-2">
            <a href="https://www.github.com/Destaq" class="btn btn-accent"
              >GitHub</a
            >
            <a href="https://www.simonilincev.com" class="btn btn-accent"
              >Website</a
            >
          </div>
        </div>
      </div>
      <div class="mx-auto card bordered w-96 bg-base-200">
        <figure>
          <img src="../public/david.jpeg" />
        </figure>
        <div class="card-body">
          <h2 class="card-title">
            David Sun
            <div class="badge mx-2 badge-secondary">12P</div>
          </h2>
          <p class="mt-4">
            Hello, my name is David Sun. I'm experienced with programming in
            Python and building projects using Arduino. Currently learning C#
            and 3d modelling with Blender.
          </p>
          <p class="mt-4">
            I'm fluent with 3 languages: English, Czech and Chinese. And I would
            say that I understand a bit Japanese. I look forward to working with
            you in the club.
          </p>
        </div>
      </div>
    </div>
  </body>
</template>

<script>
class TypeWriter {
  constructor(txtElement, words, wait = 3000) {
    this.txtElement = txtElement;
    this.words = words;
    this.txt = "";
    this.wordIndex = 0;
    this.wait = parseInt(wait, 10);
    this.type();
    this.isDeleting = false;
  }

  type() {
    // Current index of word
    const current = this.wordIndex % this.words.length;
    // Get full text of current word
    const fullTxt = this.words[current];

    // Check if deleting
    if (this.isDeleting) {
      // Remove characters
      this.txt = fullTxt.substring(0, this.txt.length - 1);
    } else {
      // Add charaters
      this.txt = fullTxt.substring(0, this.txt.length + 1);
    }

    // Insert txt into element
    this.txtElement.innerHTML = `<span class="txt">${this.txt}</span>`;

    // Initial Type Speed
    let typeSpeed = 50;

    if (this.isDeleting) {
      // Increase speed by half when deleting
      typeSpeed /= 2;
    }

    // If word is complete
    if (!this.isDeleting && this.txt === fullTxt) {
      // Make pause at end
      typeSpeed = this.wait;
      // Set delete to true
      this.isDeleting = true;
    } else if (this.isDeleting && this.txt === "") {
      this.isDeleting = false;
      // Move to next word
      this.wordIndex++;
      // Pause before start typing
      typeSpeed = 500;
    }

    setTimeout(() => this.type(), typeSpeed);
  }
}

// Init On DOM Load
document.addEventListener("DOMContentLoaded", init);

// Init App
function init() {
  const txtElement = document.querySelector(".txt-type");
  const words = JSON.parse(txtElement.getAttribute("data-words"));
  const wait = txtElement.getAttribute("data-wait");
  // Init TypeWriter
  new TypeWriter(txtElement, words, wait);
}

import VueCountdown from "@chenfengyuan/vue-countdown";

export default {
  name: "App",
  components: {
    VueCountdown,
  },
  head() {
    return {
      title: "PLIS Hack Club",
    };
  },
  computed: {
    time() {
      var now = new Date();
      var firstday = new Date(now.setDate(now.getDate() - now.getDay()));
      var friday = new Date(now.setDate(now.getDate() - now.getDay() + 11)); // note: decrease by seven next week
      friday.setHours(15, 30);

      return friday - firstday;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<style scoped>
/* CSS RESET */

/* ADD CURSOR */
.txt-type > .txt {
  border-right: 0.08rem solid #fff;
  padding-right: 2px;
  /* Animating the cursor */
  animation: blink 0.6s infinite;
}

/* ANIMATION */
@keyframes blink {
  0% {
    border-right: 0.08rem solid rgba(255, 255, 255, 1);
  }

  100% {
    border-right: 0.08rem solid rgba(255, 255, 255, 0.2);
  }
}

#page .section-background {
  background: white;
}

#page section * {
  color: black !important;
}

#page .content {
  width: 100%;
}
</style>
