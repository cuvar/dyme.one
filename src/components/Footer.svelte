<script>
  import Link from "./Link.svelte";
</script>

<footer
  class="flex w-full items-center justify-center space-x-4 py-6 text-neutral-200 absolute bottom-0 left-0"
>
  <button type="button" class="text-sm hover:text-teal-300" data-cc="c-settings"
    >Cookies</button
  >
  <Link href="/imprint" text={"Imprint"} />
</footer>
