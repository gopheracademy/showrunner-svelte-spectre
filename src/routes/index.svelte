<script>
  import Footer from "$components/Footer.svelte";

  import { getContext } from "svelte";
  let gcDetails;
  gcDetails = getContext("gcDetails");
</script>

<style lang="scss">
</style>

<div class="off-canvas-content">
  <div class="docs-content" id="content">
    <div class="container" id="getting-started">
      <h3 class="s-title">
        Getting started
        <a class="anchor" href="#getting-started" aria-hidden="true">#</a>
      </h3>
      <p>
        <strong>Spectre.css </strong>is a lightweight, responsive and modern CSS
        framework for faster and extensible development.
      </p>
      <p>
        Spectre provides basic styles for typography and elements, flexbox based
        responsive layout system, pure CSS components and utilities with best
        practice coding and consistent design language.
      </p>
      <div class="docs-demo columns">
        <div class="column col-6 col-xs-12">
          <div class="card">
            <div class="card-header">
              <div class="card-title h5">Installation</div>
            </div>
            <div class="card-body">How to install and use Spectre.css</div>
            <div class="card-footer">
              <a
                class="btn btn-primary"
                href="getting-started/installation.html">View</a>
            </div>
          </div>
        </div>
        <div class="column col-6 col-xs-12">
          <div class="card">
            <div class="card-header">
              <div class="card-title h5">Custom version</div>
            </div>
            <div class="card-body">Customize your version of Spectre.css</div>
            <div class="card-footer">
              <a
                class="btn btn-primary"
                href="getting-started/custom.html">View</a>
            </div>
          </div>
        </div>
        <div class="column col-6 col-xs-12">
          <div class="card">
            <div class="card-header">
              <div class="card-title h5">Browser support</div>
            </div>
            <div class="card-body">Browser compatibility and support</div>
            <div class="card-footer">
              <a
                class="btn btn-primary"
                href="getting-started/browsers.html">View</a>
            </div>
          </div>
        </div>
        <div class="column col-6 col-xs-12">
          <div class="card">
            <div class="card-header">
              <div class="card-title h5">What's new</div>
            </div>
            <div class="card-body">Changelog and release notes</div>
            <div class="card-footer">
              <a
                class="btn btn-primary"
                href="getting-started/whatsnew.html">View</a>
            </div>
          </div>
        </div>
        <div class="column col-6 col-xs-12">
          <div class="card">
            <div class="card-header">
              <div class="card-title h5">Accessibility</div>
            </div>
            <div class="card-body text-gray">Coming soon</div>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</div>
