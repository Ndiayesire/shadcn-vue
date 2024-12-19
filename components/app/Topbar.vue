<script setup lang="ts">
import { watch } from "vue";

const colorMode = useColorMode();

const setColorTheme = (newTheme: "light" | "dark") => {
  colorMode.preference = newTheme;
};

watch(
  () => colorMode.preference,
  (newTheme) => {
    const htmlElement = document.documentElement;
    if (newTheme === "dark") {
      htmlElement.classList.add("dark");
    } else {
      htmlElement.classList.remove("dark");
    }
  }
);
</script>

<template>
  <div
    class="border-b bg-transparent dark:bg-transparent backdrop-blur-xl bg-opacity-30 dark:bg-opacity-30 border-gray-300 dark:border-gray-800 flex h-14 w-full items-center sticky z-40 top-0"
  >
    <div class="flex justify-between items-center p-4 w-full">
      <div class="flex gap-3 items-center">
        <svg
          class="h-6 w-6"
          viewBox="0 0 256 256"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g clip-path="url(#clip0_102_1338)">
            <path
              d="M208 128L128 208"
              stroke="#41B883"
              stroke-width="16"
              stroke-linecap="round"
              stroke-linejoin="round"
            ></path>
            <path
              d="M192 40L40 192"
              stroke="#41B883"
              stroke-width="16"
              stroke-linecap="round"
              stroke-linejoin="round"
            ></path>
          </g>
          <defs>
            <clipPath id="clip0_102_1338">
              <rect width="256" height="256" fill="white"></rect>
            </clipPath>
          </defs>
        </svg>
        <h1 class="font-base font-bold dark:text-white">shadcn-vue</h1>

        <ul
          class="flex gap-10 ml-40 text-gray-500 dark:text-gray-300 text-sm font-medium transition-colors"
        >
          <li class="dark:hover:text-white"><NuxtLink to="/about">Docs</NuxtLink></li>
          <li class="dark:hover:text-white">
            <NuxtLink to="/">Components</NuxtLink>
          </li>
          <li class="dark:hover:text-white">
            <NuxtLink to="/">Themes</NuxtLink>
          </li>
          <li class="dark:hover:text-white">
            <NuxtLink to="/">Examples</NuxtLink>
          </li>
          <li class="dark:hover:text-white">
            <NuxtLink to="/">Blocks</NuxtLink>
          </li>
          <li class="dark:hover:text-white">
            <NuxtLink to="/">Githubs</NuxtLink>
          </li>
        </ul>
      </div>

      <div class="flex gap-3 mr-8">
        <Input
          placeholder="Search documentation..."
          class="h-8 w-[15rem] dark:bg-black dark:border-gray-800 rounded-lg"
        />

        <div class="flex gap-1 items-center">
          <button
            class="inline-flex items-center justify-center gap-2 whitespace-nowrap rounded-md text-sm font-medium transition-colors focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50 [&amp;_svg]:pointer-events-none [&amp;_svg]:size-4 [&amp;_svg]:shrink-0 hover:bg-accent hover:text-accent-foreground w-9 h-9"
            type="button"
            aria-haspopup="dialog"
            aria-expanded="false"
            aria-controls=""
            data-state="closed"
          >
            <!--[--><svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="lucide lucide-paintbrush-icon w-4 h-4"
            >
              <path d="m14.622 17.897-10.68-2.913"></path>
              <path
                d="M18.376 2.622a1 1 0 1 1 3.002 3.002L17.36 9.643a.5.5 0 0 0 0 .707l.944.944a2.41 2.41 0 0 1 0 3.408l-.944.944a.5.5 0 0 1-.707 0L8.354 7.348a.5.5 0 0 1 0-.707l.944-.944a2.41 2.41 0 0 1 3.408 0l.944.944a.5.5 0 0 0 .707 0z"
              ></path>
              <path
                d="M9 8c-1.804 2.71-3.97 3.46-6.583 3.948a.507.507 0 0 0-.302.819l7.32 8.883a1 1 0 0 0 1.185.204C12.735 20.405 16 16.792 16 15"
              ></path>
            </svg>
          </button>
          <button
            class="inline-flex items-center justify-center gap-2 whitespace-nowrap rounded-md text-sm font-medium transition-colors focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50 [&amp;_svg]:pointer-events-none [&amp;_svg]:size-4 [&amp;_svg]:shrink-0 hover:bg-accent hover:text-accent-foreground w-9 h-9"
            type="button"
            aria-haspopup="dialog"
            aria-expanded="false"
            data-state="closed"
          >
            <svg viewBox="0 0 15 15" width="1.2em" height="1.2em" class="w-5 h-5">
              <path
                fill="currentColor"
                fill-rule="evenodd"
                d="M7.07.65a.85.85 0 0 0-.828.662l-.238 1.05q-.57.167-1.08.448l-.91-.574a.85.85 0 0 0-1.055.118l-.606.606a.85.85 0 0 0-.118 1.054l.574.912q-.28.509-.447 1.079l-1.05.238a.85.85 0 0 0-.662.829v.857a.85.85 0 0 0 .662.829l1.05.238q.166.57.448 1.08l-.575.91a.85.85 0 0 0 .118 1.055l.607.606a.85.85 0 0 0 1.054.118l.911-.574q.51.28 1.079.447l.238 1.05a.85.85 0 0 0 .829.662h.857a.85.85 0 0 0 .829-.662l.238-1.05q.57-.166 1.08-.447l.911.574a.85.85 0 0 0 1.054-.118l.606-.606a.85.85 0 0 0 .118-1.054l-.574-.911q.282-.51.448-1.08l1.05-.238a.85.85 0 0 0 .662-.829v-.857a.85.85 0 0 0-.662-.83l-1.05-.237q-.166-.57-.447-1.08l.574-.91a.85.85 0 0 0-.118-1.055l-.606-.606a.85.85 0 0 0-1.055-.118l-.91.574a5.3 5.3 0 0 0-1.08-.448l-.239-1.05A.85.85 0 0 0 7.928.65zM4.92 3.813a4.5 4.5 0 0 1 1.795-.745L7.071 1.5h.857l.356 1.568a4.5 4.5 0 0 1 1.795.744l1.36-.857l.607.606l-.858 1.36c.37.527.628 1.136.744 1.795l1.568.356v.857l-1.568.355a4.5 4.5 0 0 1-.744 1.796l.857 1.36l-.606.606l-1.36-.857a4.5 4.5 0 0 1-1.795.743L7.928 13.5h-.857l-.356-1.568a4.5 4.5 0 0 1-1.794-.744l-1.36.858l-.607-.606l.858-1.36a4.5 4.5 0 0 1-.744-1.796L1.5 7.93v-.857l1.568-.356a4.5 4.5 0 0 1 .744-1.794L2.954 3.56l.606-.606zM9.026 7.5a1.525 1.525 0 1 1-3.05 0a1.525 1.525 0 0 1 3.05 0m.9 0a2.425 2.425 0 1 1-4.85 0a2.425 2.425 0 0 1 4.85 0"
                clip-rule="evenodd"
              ></path>
            </svg>
          </button>
          <a
            class="inline-flex items-center justify-center gap-2 whitespace-nowrap rounded-md text-sm font-medium ring-offset-background transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 [&amp;_svg]:pointer-events-none [&amp;_svg]:size-4 [&amp;_svg]:shrink-0 hover:bg-accent hover:text-accent-foreground w-9 h-9"
            href="https://github.com/unovue/shadcn-vue"
            target="_blank"
            ><!--[--><svg
              viewBox="0 0 15 15"
              width="1.2em"
              height="1.2em"
              class="w-5 h-5"
            >
              <path
                fill="currentColor"
                fill-rule="evenodd"
                d="M7.5.25a7.25 7.25 0 0 0-2.292 14.13c.363.066.495-.158.495-.35c0-.172-.006-.628-.01-1.233c-2.016.438-2.442-.972-2.442-.972c-.33-.838-.805-1.06-.805-1.06c-.658-.45.05-.441.05-.441c.728.051 1.11.747 1.11.747c.647 1.108 1.697.788 2.11.602c.066-.468.254-.788.46-.969c-1.61-.183-3.302-.805-3.302-3.583a2.8 2.8 0 0 1 .747-1.945c-.075-.184-.324-.92.07-1.92c0 0 .61-.194 1.994.744A7 7 0 0 1 7.5 3.756A7 7 0 0 1 9.315 4c1.384-.938 1.992-.743 1.992-.743c.396.998.147 1.735.072 1.919c.465.507.745 1.153.745 1.945c0 2.785-1.695 3.398-3.31 3.577c.26.224.492.667.492 1.343c0 .97-.009 1.751-.009 1.989c0 .194.131.42.499.349A7.25 7.25 0 0 0 7.499.25"
                clip-rule="evenodd"
              ></path></svg
          ></a>
          <button
            class="inline-flex items-center justify-center gap-2 whitespace-nowrap rounded-md text-sm font-medium ring-offset-background transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 [&amp;_svg]:pointer-events-none [&amp;_svg]:size-4 [&amp;_svg]:shrink-0 hover:bg-accent hover:text-accent-foreground w-9 h-9"
            aria-label="Toggle dark mode"
            @click="
              setColorTheme(useColorMode().preference === 'dark' ? 'light' : 'dark')
            "
          >
            <svg
              viewBox="0 0 15 15"
              width="1.2em"
              height="1.2em"
              class="w-5 h-5 text-foreground"
            >
              <path
                fill="currentColor"
                fill-rule="evenodd"
                d="M2.9.5a.4.4 0 0 0-.8 0v.6h-.6a.4.4 0 1 0 0 .8h.6v.6a.4.4 0 1 0 .8 0v-.6h.6a.4.4 0 0 0 0-.8h-.6zm3 3a.4.4 0 1 0-.8 0v.6h-.6a.4.4 0 1 0 0 .8h.6v.6a.4.4 0 1 0 .8 0v-.6h.6a.4.4 0 0 0 0-.8h-.6zm-4 3a.4.4 0 1 0-.8 0v.6H.5a.4.4 0 1 0 0 .8h.6v.6a.4.4 0 0 0 .8 0v-.6h.6a.4.4 0 0 0 0-.8h-.6zM8.544.982l-.298-.04c-.213-.024-.34.224-.217.4q.211.305.389.632A6.602 6.602 0 0 1 2.96 11.69c-.215.012-.334.264-.184.417q.103.105.21.206l.072.066l.26.226l.188.148l.121.09l.187.131l.176.115q.18.115.37.217l.264.135l.26.12l.303.122l.244.086a6.6 6.6 0 0 0 1.103.26l.317.04l.267.02q.19.011.384.011a6.6 6.6 0 0 0 6.56-7.339l-.038-.277a6.6 6.6 0 0 0-.384-1.415l-.113-.268l-.077-.166l-.074-.148a6.6 6.6 0 0 0-.546-.883l-.153-.2l-.199-.24l-.163-.18l-.12-.124l-.16-.158l-.223-.2l-.32-.26l-.245-.177l-.292-.19l-.321-.186l-.328-.165l-.113-.052l-.24-.101l-.276-.104l-.252-.082l-.325-.09l-.265-.06zm1.86 4.318a7.6 7.6 0 0 0-.572-2.894a5.601 5.601 0 1 1-4.748 10.146a7.6 7.6 0 0 0 3.66-2.51a.749.749 0 0 0 1.355-.442a.75.75 0 0 0-.584-.732q.093-.174.178-.355A1.25 1.25 0 1 0 10.35 6.2q.052-.442.052-.9"
                clip-rule="evenodd"
              ></path>
            </svg>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
