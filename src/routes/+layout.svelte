<script>
    import "../app.css";//tailwind css imported

    let Home = "home";
    let soju = "soju";
    let cntbr = "yo";
    let git = "git.soju.me";


  </script>

<nav class="p-2 text-center navbar-center bg-purple-400">

<strong><a class=" p-2 normal-case text-xl text-white" href="/">{Home.toUpperCase()}</a></strong>
<strong><a class=" p-2 normal-case text-xl text-white" href="/soju">{soju.toUpperCase()}</a></strong>
<strong><a class=" p-2 normal-case text-xl text-white" href="/yo">{cntbr.toUpperCase()}</a></strong>

</nav>
  <slot />
