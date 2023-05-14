<script context="module" lang="ts">
  export interface Project {
    techs: string[] | undefined | null;
    repo: string | undefined | null;
    preview: string | undefined | null;
    desc: string | undefined | null;
    name: string;
  }
</script>

<script lang="ts">
  export let project: Project;

  let { techs, repo, preview, desc, name } = project;
</script>

<div class="flex flex-col group hover:shadow-lg py-8 px-6">
  <div class="flex justify-between items-center mb-6">
    <a
      href={preview}
      target="_blank"
      class="opacity-0 group-hover:opacity-100 transition-opacity"
    >
      <span class="sr-only">go to repository</span>
      <svg
        class="fill-gray-500 hover:fill-blue-600 hover:cursor-pointer"
        width="48"
        height="48"
        viewBox="0 0 32 32"
        fill="#71717A"
        xmlns="http://www.w3.org/2000/svg"
        aria-hidden
      >
        <path
          d="M10 6V8H5V19H16V14H18V20C18 20.2652 17.8946 20.5196 17.7071 20.7071C17.5196 20.8946 17.2652 21 17 21H4C3.73478 21 3.48043 20.8946 3.29289 20.7071C3.10536 20.5196 3 20.2652 3 20V7C3 6.73478 3.10536 6.48043 3.29289 6.29289C3.48043 6.10536 3.73478 6 4 6H10ZM21 3V11H19V6.413L11.207 14.207L9.793 12.793L17.585 5H13V3H21Z"
          fill="inherit"
        />
      </svg>
    </a>
    <!-- Github Icon  -->
    <a
      href={repo}
      target="_blank"
      class=" hover:-translate-y-2 transition-transform"
    >
      <span class="sr-only">go to repository</span>
      <svg
        class="hover:fill-blue-600 hover:cursor-pointer"
        width="32"
        height="32"
        viewBox="0 0 32 32"
        fill="#71717A"
        xmlns="http://www.w3.org/2000/svg"
        aria-hidden
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M15.9989 4C9.37254 4 4 9.37254 4 16.0004C4 21.3022 7.43804 25.7996 12.2065 27.3871C12.8069 27.4969 13.0257 27.1263 13.0257 26.8081C13.0257 26.5237 13.0154 25.7686 13.0095 24.7675C9.67163 25.4924 8.96737 23.1586 8.96737 23.1586C8.4215 21.7729 7.63473 21.4038 7.63473 21.4038C6.5452 20.6591 7.71724 20.6738 7.71724 20.6738C8.9217 20.7593 9.55523 21.9107 9.55523 21.9107C10.6256 23.7443 12.3642 23.2146 13.0478 22.9081C13.1568 22.1324 13.4662 21.6035 13.8095 21.3037C11.145 21.0009 8.34341 19.971 8.34341 15.3727C8.34341 14.0629 8.8112 12.9918 9.57881 12.1527C9.45505 11.8492 9.04325 10.6293 9.69594 8.97695C9.69594 8.97695 10.7037 8.65429 12.9962 10.2072C13.9532 9.94125 14.9801 9.80791 16.0004 9.80349C17.0192 9.80791 18.0461 9.94125 19.0045 10.2072C21.2956 8.65429 22.3011 8.97695 22.3011 8.97695C22.956 10.6293 22.5442 11.8492 22.4205 12.1527C23.1895 12.9918 23.6544 14.0629 23.6544 15.3727C23.6544 19.9828 20.8484 20.9972 18.175 21.2941C18.606 21.6646 18.9898 22.3969 18.9898 23.5166C18.9898 25.1204 18.975 26.4147 18.975 26.8081C18.975 27.1293 19.1909 27.5027 19.8001 27.3856C24.5649 25.7951 28 21.3007 28 16.0004C28 9.37254 22.6267 4 15.9989 4Z"
          fill="inherit"
        />
      </svg>
    </a>
  </div>

  <h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-4">{name}</h3>
  <p class="text-base md:text-xl font-medium text-gray-500 mb-28">{desc}</p>
  <ul class="flex gap-x-6 gap-y-4 flex-wrap">
    {#each techs as tech (tech)}
      <li class="text-sm font-medium text-gray-600">
        {tech}
      </li>
    {/each}
  </ul>
</div>
