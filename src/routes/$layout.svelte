<script context="module">
  export const prerender = true;

  export async function preload({ params }) {
    const headers = {
      Accept: "application/json",
      "Accept-Encoding": "gzip",
      "Content-Type": "application/json",
    };
    const response = await this.fetch(
      "https://showrunner-46b2.encoreapi.com/dev/conferences.GetCurrentByEvent",
      {
        method: "POST",
        headers: headers,
        body: JSON.stringify({ EventID: 1 }),
      }
    );
    return response.json().then((event) => {
      if (event.error) {
        throw new Error(event.error);
      }
      return { event };
    });
  }
</script>

<script>
  import Navbar from "$components/Navbar";

  import { setContext, onMount } from "svelte";

  import {
    user,
    userId,
    token,
    getToken,
    getUserInfo,
  } from "$components/stores/auth";
  onMount(async () => {
    console.log($user);
  });

  export let event;
  export let gcDetails = event.Event;
  setContext("gcDetails", gcDetails);
</script>

<style lang="scss">
  // Import full Spectre source code
  :global {
    // Example of project-name.scss
    // Define variables to override default ones
    $primary-color: #2e5bec;
    $dark-color: #3e396b;

    @import "node_modules/spectre.css/docs/src/scss/docs";
    @import "node_modules/spectre.css/src/spectre";
    @import "node_modules/spectre.css/src/spectre-icons";
    @import "node_modules/spectre.css/src/spectre-exp";
  }
</style>

<!-- page container 100% width container with max-width set to grid-lg (960px) -->
<div class="docs-container off-canvas off-canvas-sidebar-show">
  <Navbar />
  <slot />
</div>
<!-- page container -->
