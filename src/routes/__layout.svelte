<script>
export let navOpen = false

export function handleNav() {
    navOpen = !navOpen  
}

</script>

<div class="container">
     <!-- START NAV -->
    <div class="box">
    <nav class="navbar">
        <div class="container">
                <div class="navbar-brand">
                    <a class="navbar-item" href="../">
                        <img src="https://bulma.io/images/bulma-logo.png" alt="Logo">
                    </a>
                    <span on:click={handleNav} class="navbar-burger burger" data-target=" navbarMenu">
                        <span></span>
                        <span></span>
                        <span></span>
                    </span>
                </div>
                <div  id="navbarMenu" class:is-active={navOpen} class="navbar-menu">
                    <div class="navbar-end">
                        <div class=" navbar-item">
                            <div class="control has-icons-left">
                                <input class="input is-rounded" type="email" placeholder="Search">
                                <span class="icon is-left">
                                    <i class="fa fa-search"></i>
                                </span>
                            </div>
                        </div>
                        <a href="/" class="navbar-item is-size-5 has-text-weight-semibold">
                            Home
                        </a>
                        <a href="/" class="navbar-item is-size-5 has-text-weight-semibold">
                            About
                        </a>
                        <a href="/" class="navbar-item is-size-5 has-text-weight-semibold">
                            Contact
                        </a>
                        </div>
                    </div>
                </div>
            </nav>
        </div>
        <slot></slot>
</div>
  <!-- END NAV -->

<!-- footer -->
<footer class="footer">
    <div class="content has-text-centered">
      <p>
        <strong>Styled with Bulma</strong> by Andrew Shoemaker &copy;
      </p>
    </div>
  </footer>