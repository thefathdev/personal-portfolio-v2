<script lang="ts">
  export let href: string;
  export let type: "primary" | "secondary" = "primary";
  export let size: "md" | "lg" = "md";
</script>

<a
  {href}
  class={`text-base sm:text-lg ${
    type === "primary"
      ? " text-blue-600 border-blue-600 hover:bg-blue-600/10 drop-shadow-[0_35px_35px_rgba(37,99,235,0.5)]"
      : "text-white border-white hover:bg-white/10 drop-shadow-[0_35px_35px_rgba(0,0,0,0.5)]"
  }  font-bold ${
    size === "lg"
      ? "py-3.5 px-7 sm:text-xl sm:py-4 sm:px-8"
      : "py-2 px-5 sm:text-lg"
  }  border-solid border-2  rounded-xl 
transition-colors`}
>
  <slot />
</a>
