<script>
    import "../app.css";
  </script>

 <nav>
    <a class="font-bold text-2xl" href="/">SVELTEFLIX</a>

    <div>
        <a href="/search">Search</a>
        <a href="/watching">watchlist</a>
        <a href="/login">Login</a>
    </div>
 </nav>

<main class="flex-1">
    <slot />
</main>

<footer class="text-center">
    <p>Data provided by <a href="https://www.themoviedb.org/
        " class="text-cyan-400/90">TMDB</a>. Built with <span class="text-netflix">SvelteKit</span> by <span class="text-netflix underline">Fex</span> </p>
</footer>
 <style>
    nav{
        @apply flex items-center justify-between text-netflix py-3
    }

    nav div {
        @apply flex items-center gap-3
    }

    nav div a {
        @apply text-lg capitalize
    }
 </style>