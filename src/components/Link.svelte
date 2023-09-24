<script lang="ts">
  export let text: string;
  export let href: string;
</script>

<a {href} class="flex space-x-2 text-sm hover:text-teal-300">
  <span><slot /></span>
  <span>{text}</span>
</a>
