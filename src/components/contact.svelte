<script lang="ts">
  import { Button } from "./ui";
</script>

<div
  id="contact"
  class="min-h-screen flex flex-col justify-center max-w-5xl mx-auto px-8 md:px-20 lg:px-24 xl:px-8 py-16"
>
  <div class="flex items-center gap-2 justify-center mb-6 sm:mb-10">
    <div class="w-10 h-[2px] bg-gray-500" />
    <h2 class="text-gray-900 font-bold text-3xl sm:text-5xl lg:text-6xl">
      Get In Touch
    </h2>
    <div class="w-10 h-[2px] bg-gray-500" />
  </div>
  <div class="flex justify-center">
    <p
      class="text-base sm:text-xl font-medium text-gray-500 max-w-[54ch] mb-4 sm:mb-9 text-center"
    >
      Well, whether you have a question for me or just look around. Feel free to
      contact me!
    </p>
  </div>
  <div class="flex justify-center">
    <Button href="mailto:abdillahfathu@gmail.com" size="lg">Say Hello</Button>
  </div>
</div>
