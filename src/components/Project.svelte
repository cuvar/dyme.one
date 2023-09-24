<script lang="ts">
  import Link from "./Link.svelte";

  export let name: string;
  export let description: string;
  export let url: string;
  export let gh: string;

  const realUrl = new URL(url);
  const realGHUrl = new URL(gh);
  const hostUrl = realUrl.host;
  const hostGhUrl = realGHUrl.pathname.slice(1);
</script>

<div
  class="flex flex-col space-y-4 rounded-md border border-transparent px-4 py-4 hover:bg-slate-800"
>
  <h2 class="text-xl font-bold">{name}</h2>
  <p>{description}</p>
  <Link href={url} text={hostUrl}>
    <span
      ><svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width={1.5}
        stroke="currentColor"
        class="h-5 w-5"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M13.19 8.688a4.5 4.5 0 011.242 7.244l-4.5 4.5a4.5 4.5 0 01-6.364-6.364l1.757-1.757m13.35-.622l1.757-1.757a4.5 4.5 0 00-6.364-6.364l-4.5 4.5a4.5 4.5 0 001.242 7.244"
        />
      </svg>
    </span>
  </Link>
  <Link href={gh} text={hostGhUrl}>
    <span
      ><svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
        class="lucide lucide-github"
        ><path
          d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"
        /><path d="M9 18c-4.51 2-5-2-7-2" /></svg
      >
    </span>
  </Link>
</div>
