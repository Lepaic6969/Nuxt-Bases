<template>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
        <a class="navbar-brand" href="/">Intro Nuxt</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
                <NuxtLink to="/" class="nav-link active">Default</NuxtLink>
                <!-- <a class="nav-link active" aria-current="page" href="#">Default</a> -->
            </li>
            <li class="nav-item">
                <NuxtLink  class="nav-link active" aria-current="page" href="/home">Home</NuxtLink>
            </li>
            <li class="nav-item">
                <NuxtLink class="nav-link active" aria-current="page" href="/about">About</NuxtLink>
            </li>
            <li class="nav-item">
                <NuxtLink class="nav-link active" aria-current="page" href="/posts">Post</NuxtLink>
            </li>
            <!-- Esta ruta es sólo de ejemplo (Por practicidad) -->
            <li class="nav-item">
                <NuxtLink class="nav-link active" aria-current="page" href="/posts123">Error</NuxtLink>
            </li>
        </ul>
        </div>
    </div>
    </nav>
</template>

<script vue>

</script>

<style>

</style>