<script context="module">
  import '../global.scss';
  import _uk from 'uikit/dist/js/uikit.min.js';
  import _Icons from 'uikit/dist/js/uikit-icons.min.js';
  import Scrollbar from 'smooth-scrollbar';
  
  Scrollbar.init(document.querySelector('html'));
</script>

<nav class="uk-navbar-container" uk-navbar>
    <div class="uk-navbar-left">

        <ul class="uk-navbar-nav">
            <li class="uk-active"><a href="#example">UIKit navbar exmaple</a></li>
            <li>
                <a href="#example">Parent</a>
                <div class="uk-navbar-dropdown">
                    <ul class="uk-nav uk-navbar-dropdown-nav">
                        <li class="uk-active"><a href="#example">Active</a></li>
                        <li><a href="#example">Item</a></li>
                        <li><a href="#example">Item</a></li>
                    </ul>
                </div>
            </li>
            <li><a href="#example">Item</a></li>
        </ul>

    </div>
</nav>

<slot />
