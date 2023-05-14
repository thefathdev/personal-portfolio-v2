<script lang="ts">
  import Button from "./button.svelte";
  import MobileMenu from "./mobile-menu.svelte";
  import NavLink from "./nav-link.svelte";

  let openMenu = false;

  const toggleMenu = () => {
    openMenu = !openMenu;
  };
</script>

<header
  class="fixed w-full backdrop-blur bg-white/40 px-6 lg:px-20 py-5 flex justify-between items-center pointer-events-auto"
>
  <a href="#home" class="group text-gray-900 text-2xl sm:text-3xl font-bold">
    {"<"}
    <span
      class="inline-block opacity-0 -translate-x-2/4 group-hover:opacity-100 group-hover:-translate-x-0 transition"
    >
      Fath{" "}
    </span>
    <span
      class="inline-block -translate-x-12 group-hover:translate-x-2 transition-transform"
    >
      {"/>"}
    </span>
  </a>
  <nav
    class="hidden md:flex gap-9 font-medium text-gray-500 items-center pointer-events-auto"
  >
    <NavLink href="#about">About</NavLink>
    <NavLink href="#projects">Projects</NavLink>
    <NavLink href="#contact">Contact</NavLink>
    <Button href="#resume">Resume</Button>
  </nav>
  <div
    tabIndex={0}
    class="flex flex-col gap-2 md:hidden items-end z-50 cursor-pointer pointer-events-auto"
    on:click={() => toggleMenu()}
    on:keyup={(e) => {
      if (e.code === "Enter") {
        toggleMenu();
      }
    }}
  >
    <div
      aria-hidden
      class={`w-10 h-[3px] ${
        !openMenu ? "bg-blue-600" : "bg-white rotate-45 translate-y-3"
      } transition duration-200`}
    />
    <div
      aria-hidden
      class={`w-9 h-[3px] ${
        !openMenu ? "bg-blue-600" : "bg-white opacity-0 -translate-x-16"
      }  transition duration-300`}
    />
    <div
      aria-hidden
      class={`h-[3px] ${
        !openMenu
          ? "bg-blue-600 w-8"
          : "bg-white -rotate-45 w-10 -translate-y-2.5"
      }  transition duration-200`}
    />
    <span class="sr-only">open mobile menu</span>
  </div>
  <MobileMenu open={openMenu} />
</header>
