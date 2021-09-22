<script context="module">
  import '../global.scss';
  import 'uikit/dist/js/uikit.min.js';
  import 'uikit/dist/js/uikit-icons.min.js';
</script>

<script>
  import Scrollbar from 'smooth-scrollbar';
  import { onMount } from 'svelte';
  import NProgress from 'nprogress';
  import 'nprogress/nprogress.css';
  import { navigating } from '$app/stores';
  console.log(navigating)
  
  onMount(() => {
    Scrollbar.initAll();
  })
  
</script>

<svelte:window
  on:sveltekit:navigation-start={() => NProgress.start()}
  on:sveltekit:navigation-end={() => NProgress.done()} />

<nav class="uk-navbar-container" uk-navbar>
  <div class="uk-navbar-left">

      <ul class="uk-navbar-nav">
        <li><a href="/">Home</a></li>
        <li><a href="/page2">Page 2</a></li>
        <li>
          <a href="/">Dropdown</a>
          <div class="uk-navbar-dropdown">
            <ul class="uk-nav uk-navbar-dropdown-nav">
              <li><a href="/">Active</a></li>
              <li><a href="/">Item</a></li>
              <li><a href="/">Item</a></li>
            </ul>
          </div>
        </li>
      </ul>

  </div>
</nav>

<slot />
