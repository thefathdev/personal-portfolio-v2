<script lang="ts">
  export let href: string;
  export let type: "primary" | "secondary" = "primary";
</script>

<div class="group">
  <a
    {href}
    class={`text-base sm:text-lg ${
      type === "primary"
        ? "group-hover:text-blue-600"
        : "group-hover:text-white"
    }`}
  >
    <slot />
  </a>
  <div
    class={`w-full h-[2px] ${
      type === "primary" ? "bg-blue-600" : "bg-white"
    } scale-x-0 -translate-x-1/2 group-hover:scale-x-100  group-hover:translate-x-0 transition-transform`}
  />
</div>
