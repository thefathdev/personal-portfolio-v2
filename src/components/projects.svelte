<script lang="ts">
  import { TextLink, ProjectCard, Project } from "./ui";

  export let projects: Project[];
</script>

<div
  id="projects"
  class="min-h-screen flex flex-col justify-center max-w-5xl mx-auto px-8 md:px-20 lg:px-24 xl:px-8 py-20"
>
  <div class="flex gap-2 items-center mb-2 sm:mb-4">
    <div class="w-14 h-[2px] bg-gray-500 md:w-16" />
    <h2 class="text-gray-900 font-bold text-2xl sm:text-4xl lg:text-5xl">
      Project I've Built
    </h2>
  </div>
  <div class="mb-6 sm:mb-8 text-base sm:text-xl">
    <TextLink href="https://github.com/whatTheFath"
      >View my repositories</TextLink
    >
  </div>
  <div class="grid grid-cols-1 min-[486px]:grid-cols-2 gap-8 md:grid-cols-3">
    {#each projects as project (project.name)}
      <ProjectCard {project} />
    {/each}
  </div>
</div>
