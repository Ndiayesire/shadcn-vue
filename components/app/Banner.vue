<template>
  <div class="mx-auto flex flex-col items-center mt-[4rem] gap-2">
    <a
      href="/docs/components/auto-form.html"
      class="inline-flex items-center rounded-lg bg-gray-100 dark:bg-gray-800 px-3 py-1 text-sm font-medium"
      >✨ Extended: Auto Form, Charts
    </a>
    <h1 class="text-5xl font-bold leading-tight tracking-tighter">
      Build your component library.
    </h1>
    <span
      class="max-w-[750px] text-center text-lg font-base text-foreground"
      data-brr="1"
      data-allow-mismatch="true"
      style="
        display: inline-block;
        vertical-align: top;
        text-decoration: inherit;
        text-wrap: initial;
        max-width: 494px;
      "
    >
      Beautifully designed components that you can copy and paste into your apps.
      Accessible. Customizable. Open Source.</span
    >
    <div class="flex w-full items-center justify-center space-x-4 py-4">
      <Button class="bg-primary">Get started</Button>
      <Button variant="outline">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          fill="currentColor"
          class="w-6 h-6"
        >
          <path
            d="M12 2C6.477 2 2 6.485 2 12.021c0 4.426 2.865 8.17 6.839 9.504.5.092.683-.217.683-.482 0-.238-.009-.868-.014-1.703-2.782.604-3.369-1.342-3.369-1.342-.454-1.155-1.11-1.463-1.11-1.463-.907-.62.069-.608.069-.608 1.002.07 1.53 1.03 1.53 1.03.892 1.53 2.341 1.088 2.911.832.092-.647.349-1.089.635-1.34-2.22-.254-4.555-1.113-4.555-4.95 0-1.093.39-1.988 1.03-2.688-.104-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.584 9.584 0 0 1 12 6.844c.851.004 1.705.115 2.504.337 1.91-1.297 2.748-1.027 2.748-1.027.545 1.378.202 2.398.1 2.651.642.7 1.03 1.595 1.03 2.688 0 3.847-2.338 4.694-4.566 4.943.36.31.68.92.68 1.854 0 1.34-.012 2.423-.012 2.75 0 .268.18.579.688.48A10.021 10.021 0 0 0 22 12.021C22 6.485 17.523 2 12 2z"
          />
        </svg>
        Login with Email
      </Button>
    </div>
  </div>
</template>

<script setup>
import { Button } from "@/components/ui/button";
</script>
