<script lang="ts">
  import Button from "./button.svelte";
  import NavLink from "./nav-link.svelte";

  export let open: boolean = false;
</script>

<div
  class={`absolute md:hidden top-0 right-0 w-2/3 bg-blue-600  min-h-screen ${
    !open && "translate-x-full"
  } transition-transform z-40`}
>
  <nav class="flex flex-col gap-9 font-medium text-white items-center pt-20">
    <NavLink type="secondary" href="#about">About</NavLink>
    <NavLink type="secondary" href="#projects">Projects</NavLink>
    <NavLink type="secondary" href="#contact">Contact</NavLink>
    <Button size="md" type="secondary" href="#resume">Resume</Button>
  </nav>
</div>
