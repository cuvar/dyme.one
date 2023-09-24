<script lang="ts">
  import type { ProjectItem } from "../utils/types.ts";
  import Project from "./Project.svelte";

  const projects: ProjectItem[] = [
    {
      name: "panal",
      description: "widget-based dashboard for managing life",
      url: "https://panal.dyme.one",
      gh: "https://github.com/cuvar/panal",
    },
    // {
    //   name: "swiper-action",
    //   description: "Simple react component for swipe-to-action",
    //   url: "https://github.com/cuvar/swiper-action",
    //   gh: "https://github.com/cuvar/swiper-action",
    // },
    {
      name: "vocab",
      description: "A simple vocabulary app for learning new words",
      url: "https://vocab.dyme.one",
      gh: "https://github.com/cuvar/vocab",
    },
  ];
</script>

<div class="grid grid-cols-1 gap-8 md:grid-cols-2 xl:grid-cols-2">
  {#each projects as project, i}
    <Project
      name={project.name}
      description={project.description}
      url={project.url}
      gh={project.gh}
    />
  {/each}
</div>
