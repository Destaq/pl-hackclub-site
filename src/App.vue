<template>
  <body>
    <div class="container mx-auto">
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
      </div>
      <div>
        <h1 class="font-semibold">
          The club for:
          <!-- The words that we want to have typerwriter effect -->
          <span
            class="txt-type"
            data-wait="3000"
            data-words='["makers", "coders", "learners", "hackers"]'
          ></span>
        </h1>
      </div>
      <div>
        <p>Time until next meetup</p>

        <div class="grid grid-flow-col gap-5 place-items-end auto-cols-max">
          <div>
            <span class="font-mono text-4xl countdown">
              <span style="--value: 15"></span>
            </span>
            days
          </div>
          <div>
            <span class="font-mono text-4xl countdown">
              <span style="--value: 10"></span>
            </span>
            hours
          </div>
          <div>
            <span class="font-mono text-4xl countdown">
              <span style="--value: 24"></span>
            </span>
            min
          </div>
          <div>
            <span class="font-mono text-4xl countdown">
              <span style="--value: 60"></span>
            </span>
            sec
          </div>
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
    let typeSpeed = 60;

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

export default {
  name: "App",
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
