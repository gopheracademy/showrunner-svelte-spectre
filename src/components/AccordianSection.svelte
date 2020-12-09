<script>
  import { page } from "$app/stores";
  export let title;
  export let items = [];
  export let section;
  $: checked = $page.path.includes(section);
</script>

<div class="accordion">
  <input
    id="accordion-{section}"
    type="checkbox"
    name="docs-accordion-checkbox"
    hidden="true"
    {checked} />
  <label
    class="accordion-header c-hand"
    for="accordion-{section}">{title}</label>
  <div class="accordion-body">
    <ul class="menu menu-nav">
      {#each items as item}
        <li class="menu-item"><a href={item.target}>{item.label}</a></li>
      {/each}
    </ul>
  </div>
</div>
