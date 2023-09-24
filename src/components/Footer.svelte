<script>
  import Link from "./Link.svelte";
</script>

<footer
  class="flex w-full items-center justify-center space-x-4 bg-slate-900 py-6 text-neutral-200 absolute bottom-0 left-0"
>
  <button
    type="button"
    class="text-sm hover:text-teal-300"
    onClick={() => {
      window.CC.showSettings(0); // 0 steht für den Delay, nachdem das Popup aufpoppt
    }}
  >
    Cookies
  </button>
  <Link href="/imprint" text={"Imprint"} />
</footer>
