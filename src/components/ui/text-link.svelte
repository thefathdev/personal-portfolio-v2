<script lang="ts">
  export let href: string;
</script>

<span class="group relative">
  <a {href} target="_blank" class="text-blue-600 font-bold">
    <slot />
  </a>
  <div
    class="absolute bottom-0 left-0 w-full h-[2px] bg-blue-600 scale-x-0 -translate-x-1/2 group-hover:scale-x-100 group-hover:translate-x-0 transition-transform"
  />
</span>
