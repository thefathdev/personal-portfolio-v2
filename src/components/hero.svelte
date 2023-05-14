<script lang="ts">
  import { TextLink } from "./ui";
</script>

<div
  id="home"
  class="min-h-screen flex flex-col justify-center max-w-5xl mx-auto px-8 md:px-20 lg:px-24 xl:px-8 py-16"
>
  <p class="text-lg sm:text-2xl text-blue-600 font-medium mb-1 sm:mb-4">
    Hi!, my name is
  </p>
  <h1
    class="text-3xl sm:text-5xl lg:text-7xl font-bold text-gray-900 mb-1 sm:mb-4"
  >
    Fathul Irfaan Abdillah.
  </h1>
  <h2
    class="text-3xl sm:text-5xl lg:text-7xl font-bold text-gray-500 mb-4 sm:mb-6"
  >
    I craft things for{" "}
    <span class="text-blue-600 inline-block relative">
      <span class="z-10">the web.</span>
      <span
        class="inline-block absolute w-full left-0 translate-x-1 translate-y-1 blur-sm opacity-50 z-0"
      >
        the web.
      </span>
    </span>
  </h2>
  <div class="text-base sm:text-xl font-medium text-gray-500 max-w-[54ch]">
    I’m a javascript developer focused on building{" "}
    <TextLink href="https://web.dev/learn/accessibility/">accessible</TextLink> and{" "}
    <TextLink href="https://web.dev/learn/design/">responsive website.</TextLink
    > Leveraging solution with best-practice technologies is my guiding compass.
  </div>
</div>
