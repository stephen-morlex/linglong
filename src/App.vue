<template>
  <div class="font-custom-font text-lg md:relative sm:flex sm:bg-gray-900 text-white sm:min-h-screen" id="app">
    <nav class="nav sm:w-48 sm:h-full bg-transparent sm:fixed">
      <div
        class="bg-gray-900 justify-between items-center p-4 sm:text-center flex logo sm:mt-8 sm:mb-20"
      >
        <a href="/">
          <svg width="50mm" height="28mm" viewBox="0 0 74 52" xmlns="http://www.w3.org/2000/svg">
            <text
              x="-.926"
              y="31.892"
              fill="#ffffff"
              font-family="sans-serif"
              font-size="10.583"
              letter-spacing="0"
              stroke="#03fcff"
              stroke-width=".265"
              word-spacing="0"
              style="line-height:1.25"
            >
              <tspan
                x="-.926"
                y="31.892"
                font-size="17.639"
                style="font-feature-settings:normal;font-variant-caps:normal;font-variant-ligatures:normal;font-variant-numeric:normal"
              >
                <tspan>MOR</tspan>
                <tspan>LEX</tspan>
              </tspan>
            </text>
          </svg>
        </a>
        <button
          type="button"
          @click="toggle"
          class="px-2 text-gray-500 hover:text-white focus:outline-none focus:text-white"
        >
          <svg
            class="h-10 w-10 fill-current text-gray-500 hover:text-white sm:hidden"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
          >
            <path
              v-if="isOpen"
              d="M10 8.586L2.929 1.515 1.515 2.929 8.586 10l-7.071 7.071 1.414 1.414L10 11.414l7.071 7.071 1.414-1.414L11.414 10l7.071-7.071-1.414-1.414L10 8.586z"
            />
            <path v-if="!isOpen" d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
          </svg>
        </button>
      </div>
      <div
        class="w-full sm:flex sm:items-center sm:justify-center bg-gray-900"
        :class="{'hidden':!isOpen, 'block' : isOpen}"
      >
        <ul class="items-center justify-center px-32">
          <li class="flex items-center justify-between mb-8">
            <router-link to="/" class="flex items-center sm:justify-center">
              <svg
                class="border-l border-gray-800 text-purple-600 fill-current h-16 w-16"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
              >
                <path
                  class="heroicon-ui"
                  d="M13 20v-5h-2v5a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2v-7.59l-.3.3a1 1 0 1 1-1.4-1.42l9-9a1 1 0 0 1 1.4 0l9 9a1 1 0 0 1-1.4 1.42l-.3-.3V20a2 2 0 0 1-2 2h-3a2 2 0 0 1-2-2zm5 0v-9.59l-6-6-6 6V20h3v-5c0-1.1.9-2 2-2h2a2 2 0 0 1 2 2v5h3z"
                />
              </svg>
              <span class="text-white ml-4">HOME</span>
            </router-link>
          </li>
          <li class="flex items-center justify-between mb-8">
            <router-link to="/services" class="flex items-center justify-center">
              <svg
                class="text-purple-600 fill-current h-16 w-16"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
              >
                <path
                  class="heroicon-ui"
                  d="M17 22a2 2 0 0 1-2-2v-1a1 1 0 0 0-1-1 1 1 0 0 0-1 1v1a2 2 0 0 1-2 2H8a2 2 0 0 1-2-2v-3H5a3 3 0 1 1 0-6h1V8a2 2 0 0 1 2-2h3V5a3 3 0 1 1 6 0v1h3a2 2 0 0 1 2 2v3a2 2 0 0 1-2 2h-1a1 1 0 0 0-1 1 1 1 0 0 0 1 1h1a2 2 0 0 1 2 2v3a2 2 0 0 1-2 2h-3zm3-2v-3h-1a3 3 0 1 1 0-6h1V8h-3a2 2 0 0 1-2-2V5a1 1 0 0 0-1-1 1 1 0 0 0-1 1v1a2 2 0 0 1-2 2H8v3a2 2 0 0 1-2 2H5a1 1 0 0 0-1 1 1 1 0 0 0 1 1h1a2 2 0 0 1 2 2v3h3v-1a3 3 0 1 1 6 0v1h3z"
                />
              </svg>

              <span class="text-white ml-4">Services</span>
            </router-link>
          </li>
          <li class="flex items-center justify-between mb-8">
            <router-link to="/about" class="flex items-center justify-center">
              <svg
                class="text-purple-600 fill-current h-16 w-16"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
              >
                <path
                  class="heroicon-ui"
                  d="M12 12a5 5 0 1 1 0-10 5 5 0 0 1 0 10zm0-2a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm9 11a1 1 0 0 1-2 0v-2a3 3 0 0 0-3-3H8a3 3 0 0 0-3 3v2a1 1 0 0 1-2 0v-2a5 5 0 0 1 5-5h8a5 5 0 0 1 5 5v2z"
                />
              </svg>

              <span class="text-white ml-4">About&nbsp;Me</span>
            </router-link>
          </li>
          <li class="flex items-center justify-between mb-8">
            <router-link to="/contact" class="flex items-center justify-center">
              <svg
                class="text-purple-600 fill-current h-16 w-16"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
              >
                <path
                  class="heroicon-ui"
                  d="M4 4h16a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V6c0-1.1.9-2 2-2zm16 3.38V6H4v1.38l8 4 8-4zm0 2.24l-7.55 3.77a1 1 0 0 1-.9 0L4 9.62V18h16V9.62z"
                />
              </svg>
              <span class="text-white ml-4">Contact</span>
            </router-link>
          </li>
        </ul>
      </div>
      <footer class="hidden sm:absolute sm:bottom-0 sm:items-center">
        <div class="sm:flex justify-between items-center">
          <div class="text-gray-700 text-center px-4 py-2 m-2">
            <svg
              class="feather feather-facebook text-facebook stroke-current"
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z" />
            </svg>
          </div>
          <div class="text-gray-700 text-center px-4 py-2 m-2">
            <svg
              class="feather feather-twitter text-twitter stroke-current"
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <path
                d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"
              />
            </svg>
          </div>
          <div class="text-gray-700 text-center px-4 py-2 m-2">
            <svg
              class="feather feather-github text-github stroke-current"
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <path
                d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"
              />
            </svg>
          </div>
        </div>
        <div class="flex justify-center items-center mt-4">
          <p class="text-gray-200">
            @ 2019
            <a href="/">
              <Span class="text-purple-600">Morlex</Span>.
            </a>
          </p>
        </div>
      </footer>
    </nav>
    <div class="w-full sm:ml-56 text-base text-black">
      <div class="container sm:mx-auto sm:py-8">
        <loading-bar
	class="someClass"
	id="someId"
	:progress=10
	direction="left"
	error="true">
</loading-bar>
        <transition name="fade" mode="out-in">
          <router-view />
        </transition>
      </div>
      <div
        class="flex justify-between items-center bottom-0 bg-gray-900 w-full h-12 text-white px-8 mt-2"
      >
        <div>
          @2019
          <span class="text-purple-600 mr-2">|</span>
          <span>
            <a href>Morlex</a>
          </span>
        </div>
        <div>
          <ul class="flex items-center justify-center">
            <li class="mr-3">
              <a href="#">
                <svg
                  class="feather feather-facebook text-facebook stroke-current"
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z" />
                </svg>
              </a>
            </li>
            <li class="mr-3">
              <a href="#">
                <svg
                  class="feather feather-twitter text-twitter stroke-current"
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path
                    d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"
                  />
                </svg>
              </a>
            </li>
            <li>
              <a href="#">
                <svg
                  class="feather feather-github text-github stroke-current"
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path
                    d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"
                  />
                </svg>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: [],
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    }
  }
}
</script>
<style lang="scss">
@import "src/assets/css/main.scss";
</style>
