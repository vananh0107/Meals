<template>
  <header>
    <!-- Navigation bar -->
    <nav
      class="relative flex w-full items-center justify-between bg-white py-2 text-neutral-600 shadow-lg hover:text-neutral-700 focus:text-neutral-700 dark:bg-orange-400 dark:text-neutral-200 md:flex-wrap md:justify-start "
      data-te-navbar-ref
    >
      <div class="flex w-full flex-wrap items-center justify-between px-3">
        <div class="flex items-center">
          <!-- Hamburger menu button -->
          <button
            class="border-0 bg-transparent px-2 text-xl leading-none transition-shadow duration-150 ease-in-out hover:text-neutral-700 focus:text-neutral-700 dark:hover:text-white dark:focus:text-white lg:hidden"
            type="button"
            data-te-collapse-init
            data-te-target="#navbarSupportedContentY"
            aria-controls="navbarSupportedContentY"
            aria-expanded="false"
            aria-label="Toggle navigation"
             @click="toggleActive"
          >
            <!-- Hamburger menu icon -->
            <span class="[&>svg]:w-5">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="h-7 w-7"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
                />
              </svg>
            </span>
          </button>
        </div>

        <!-- Navigation links -->
        <div
          class="!visible grow basis-[100%] items-center lg:!flex lg:basis-auto px-2"
          :class="{ hidden: isActive }"
          id="navbarSupportedContentY"
          data-te-collapse-item
        >
          <ul class="mr-auto flex flex-col lg:flex-row mx-auto" data-te-navbar-nav-ref>
            <li class="mb-4 lg:mb-0 lg:pr-2" data-te-nav-item-ref>
              <router-link
                class="block transition duration-150 ease-in-out hover:text-neutral-700 focus:text-neutral-700 disabled:text-black/30 dark:hover:text-white dark:focus:text-white lg:p-2 [&.active]:text-black/90"
                :to="{ name: 'home' }"
                data-te-nav-link-ref
                data-te-ripple-init
                data-te-ripple-color="light"
                >Home</router-link>
            </li>
            <li class="mb-4 lg:mb-0 lg:pr-2" data-te-nav-item-ref>
              <router-link
                class="block transition duration-150 ease-in-out hover:text-neutral-700 focus:text-neutral-700 disabled:text-black/30 dark:hover:text-white dark:focus:text-white lg:p-2 [&.active]:text-black/90"
                :to="{ name: 'byName' }"
                data-te-nav-link-ref
                data-te-ripple-init
                data-te-ripple-color="light"
                >Search Meals</router-link
              >
            </li>
            <li class="mb-4 lg:mb-0 lg:pr-2" data-te-nav-item-ref>
              <router-link
                class="block transition duration-150 ease-in-out hover:text-neutral-700 focus:text-neutral-700 disabled:text-black/30 dark:hover:text-white dark:focus:text-white lg:p-2 [&.active]:text-black/90"
                :to="{ name: 'byLetter' }"
                data-te-nav-link-ref
                data-te-ripple-init
                data-te-ripple-color="light"
                >Meals By Letter</router-link
              >
            </li>
            <li class="mb-2 lg:mb-0 lg:pr-2" data-te-nav-item-ref>
              <router-link
                class="block transition duration-150 ease-in-out hover:text-neutral-700 focus:text-neutral-700 disabled:text-black/30 dark:hover:text-white dark:focus:text-white lg:p-2 [&.active]:text-black/90"
                :to="{ name: 'ingredients' }"
                data-te-nav-link-ref
                data-te-ripple-init
                data-te-ripple-color="light"
                >Meals By Ingredients</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>
<script>
export default {
  data() {
    return {
      isActive: true
    };
  },
  methods: {
    toggleActive() {
      this.isActive = !this.isActive;
    }
  }
};
</script>
