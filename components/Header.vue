<template>
  <header
    class="sans-serif"
    :class="{
      'navbar-top': scrollPosition < scrollOffset,
      'navbar-scroll': scrollPosition > scrollOffset,
      'navbar-open': navbarOpen,
    }"
  >
    <div class="cover bg-left bg-center-l">
      <div class="bg-black-80">
        <nav class="dt w-100 mw8 center">
          <div class="dtc w2 v-mid pa3">
            <a
              href="/"
              class="dib w2 h2 pa1 ba b--white-90 grow-large border-box"
            >
              <svg
                class="link white-90 hover-white"
                data-icon="dribbble"
                viewBox="0 0 32 32"
                fill="currentColor"
              >
                <title>dribbble icon</title>
                <path
                  d="M16 0 A16 16 0 0 0 0 16 A16 16 0 0 0 16 32 A16 16 0 0 0 32 16 A16 16 0 0 0 16 0 M5 11.5 A12 12 0 0 1 11 5 A46 46 0 0 1 13.5 9.25 A46 46 0 0 1 5 11.5 M15 4 A12 12 0 0 1 21.5 5.25 A46 46 0 0 1 17 7.75 A50 50 0 0 0 15 4 M4 16 A50 50 0 0 0 15 13 A46 46 0 0 1 16 15.5 A26 26 0 0 0 6 22.5 A12 12 0 0 1 4 16 M18.5 11.5 A50 50 0 0 0 25 8 A12 12 0 0 1 28 13.75 A26 26 0 0 0 19.75 14.5 A50 50 0 0 0 18.5 11.5 M17 19.5 A46 46 0 0 1 18 28 A12 12 0 0 1 8.75 25.5 A22 22 0 0 1 17 19.5 M20.75 18.25 A22 22 0 0 1 28 17.75 A12 12 0 0 1 22 26.5 A50 50 0 0 0 20.75 18.25"
                ></path>
              </svg>
            </a>
          </div>
          <div class="dtc v-mid tr pa3">
            <a
              class="f6 fw4 hover-white no-underline white-70 dn dib-ns pv2 ph3"
              href="/"
              >How it Works</a
            >
            <a
              class="f6 fw4 hover-white no-underline white-70 dn dib-ns pv2 ph3"
              href="/"
              >Pricing</a
            >
            <a
              class="f6 fw4 hover-white no-underline white-70 dn dib-l pv2 ph3"
              href="/"
              >About</a
            >
            <a
              class="f6 fw4 hover-white no-underline white-70 dn dib-l pv2 ph3"
              href="/"
              >Careers</a
            >
            <a
              class="f6 fw4 hover-white no-underline white-70 dib ml2 pv2 ph3 ba"
              href="/"
              >Sign Up</a
            >
          </div>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      navbarOpen: false,
      scrollOffset: 100,
      scrollPosition: 0,
      menu: [
        { name: "Overview", to: "#" },
        { name: "Components", to: "#" },
        { name: "Plugins", to: "#" },
        { name: "Examples", to: "#" },
        { name: "Support", to: "#" },
      ],
    };
  },

  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY;
    },
  },

  mounted() {
    this.updateScroll();
    window.addEventListener("scroll", this.updateScroll);
  },
};
</script>
