<template>
  <div class="contact items-center justify-center px-8 sm:px-0">
     <h2
        class="flex items-center justify-center font-semibold uppercase text-purple-600 text-2xl mb-8 border-b-2 border-gray-800 p-4 xl:text-3xl"
      >Contact Me</h2>
    <form class="w-full sm:mb-0" method="post" data-netlify="true">

      <div class="flex flex-wrap -mx-3 mb-6">
        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >Full Name</label>
          <input
            class="appearance-none block w-full bg-gray-900 text-gray-700 border border-purple-600 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            name="name"
            type="text"
            placeholder="Enter your full name..."
          />
        </div>
        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >Email</label>
          <input
            class="appearance-none block w-full bg-gray-900 text-gray-700 border border-purple-600 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            name="email"
            type="text"
            placeholder="Enter your full email..."
          />
        </div>
      </div>
      <div class="flex flex-wrap -mx-3 mb-6">
        <div class="w-full px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-password"
          >Message</label>
          <textarea
            class="appearance-none block w-full bg-gray-900 text-gray-700 border border-purple-600 rounded py-12 px-2 mb-3 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-password"
            name="message"
            type="password"
            placeholder="Your message..."
          />
        </div>
      </div>
      <button
        class="font-semibold bg-purple-600 rounded-lg shadow-lg py-3 px-4 text-white uppercase hover:bg-purple-900"
        type="submit"
      >Send Message</button>
    </form>
  </div>
</template>
