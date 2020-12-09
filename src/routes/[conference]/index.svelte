<script context="module">
  export const prerender = true;
  export async function preload({ params }) {
    return { conference: params.conference };
  }
</script>

<script>
  export let conference;
  import { getContext } from "svelte";

  const gcDetails = getContext("gcDetails");
</script>

<style>
</style>

{gcDetails.Name}
