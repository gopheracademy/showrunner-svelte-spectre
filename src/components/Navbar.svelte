<script>
  import AccordianMenu from "./AccordianMenu.svelte";
</script>

<style lang="scss">
  .off-canvas-sidebar {
    background: #f7f8f9;
  }
</style>

<div class="docs-navbar">
  <a class="off-canvas-toggle btn btn-link btn-action" href="#sidebar"><i
      class="icon icon-menu" /></a>
  <div class="btns d-flex">
    <a class="btn btn-primary ml-1" href="/tickets" target="_blank">Register
      Now!</a>
    <a class="btn btn-secondary ml-1" href="/login/github" target="_blank">Log
      In</a>
  </div>
</div>
<div class="docs-sidebar off-canvas-sidebar" id="sidebar">
  <div class="docs-brand">
    <a class="docs-logo" href="/">
      <h2>GOPHERCON</h2><small
        class="label label-secondary text-bold">2021</small></a>
  </div>
  <div class="docs-nav">
    <AccordianMenu />
    <div class="accordion">
      <input
        id="accordion-dashboard"
        type="checkbox"
        name="docs-accordion-checkbox"
        hidden="true"
        checked="" />
      <a href="/dashboard"><label
          class="accordion-header c-hand"
          for="accordion-dashboard">My GC</label></a>
    </div>
  </div>
</div><a class="off-canvas-overlay" href="#close" />
