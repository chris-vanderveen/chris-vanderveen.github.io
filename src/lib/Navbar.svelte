<script lang="ts">
    import { onMount } from "svelte";
    import { themeChange } from "theme-change";
    import { base } from '$app/paths';

    onMount(() => {
        themeChange(false);
    });
</script>

<div class="navbar bg-base-100 drop-shadow-sm px-4 md:px-8 lg:px-16 sticky top-0 z-50">
    <div class="navbar-start">
      <div class="dropdown">
        <div tabindex="0" role="button" class="btn btn-ghost lg:hidden rounded-full">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"> <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M4 6h16M4 12h8m-8 6h16" /> </svg>
        </div>
        <ul class="menu menu-sm dropdown-content bg-base-100 rounded-box z-1 mt-3 w-52 p-2 shadow">
          <li><a class="rounded" on:click|preventDefault={() => document.getElementById('about')?.scrollIntoView({ behavior: 'smooth' })} href="#about">About</a></li>
          <li><a class="rounded" on:click|preventDefault={() => document.getElementById('experience')?.scrollIntoView({ behavior: 'smooth' })} href="#experience">Experience</a></li>
          <li><a class="rounded" on:click|preventDefault={() => document.getElementById('projects')?.scrollIntoView({ behavior: 'smooth' })} href="#projects">Projects</a></li>
          <li><a class="rounded" on:click|preventDefault={() => document.getElementById('contact')?.scrollIntoView({ behavior: 'smooth' })} href="#contact">Contact</a></li>
        </ul>
      </div>
      <div class="relative h-10 w-32 ml-4">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 28 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="absolute top-0 left-0 h-9">
          <path d="M6 3H5a2 2 0 0 0-2 2v5a2 2 0 0 1-2 2 2 2 0 0 1 2 2v5c0 1.1.9 2 2 2h1"/>
          <path d="M22 21h1a2 2 0 0 0 2-2v-5c0-1.1.9-2 2-2a2 2 0 0 1-2-2V5a2 2 0 0 0-2-2h-1"/>
          <text x="14" y="16" text-anchor="middle" font-size="10" font-family="'Geist Mono', monospace" fill="currentColor" stroke="none">CV</text>
        </svg>
      </div>
    </div>
    <div class="navbar-center hidden lg:flex">
      <ul class="menu menu-horizontal px-1">
        <li><a class="rounded" on:click|preventDefault={() => document.getElementById('about')?.scrollIntoView({ behavior: 'smooth' })} href="#about">About</a></li>
        <li><a class="rounded" on:click|preventDefault={() => document.getElementById('experience')?.scrollIntoView({ behavior: 'smooth' })} href="#experience">Experience</a></li>
        <li><a class="rounded" on:click|preventDefault={() => document.getElementById('projects')?.scrollIntoView({ behavior: 'smooth' })} href="#projects">Projects</a></li>
        <!-- <li><a class="rounded" on:click|preventDefault={() => document.getElementById('contact')?.scrollIntoView({ behavior: 'smooth' })} href="#contact">Contact</a></li> -->
        <li><a class="rounded" href="{base}/CV_2025.pdf" download>Download CV</a></li>
      </ul>
    </div>
    <div class="navbar-end">
        <label class="swap swap-rotate">
            <input type="checkbox" data-toggle-theme="lofi,black" />
            <svg class="swap-off h-6 w-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
              <circle cx="12" cy="12" r="4"/>
              <path d="M12 2v2"/>
              <path d="M12 20v2"/>
              <path d="m4.93 4.93 1.41 1.41"/>
              <path d="m17.66 17.66 1.41 1.41"/>
              <path d="M2 12h2"/>
              <path d="M20 12h2"/>
              <path d="m6.34 17.66-1.41 1.41"/>
              <path d="m19.07 4.93-1.41 1.41"/>
            </svg>
            <svg class="swap-on h-6 w-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
              <path d="M12 3a6 6 0 0 0 9 9 9 9 0 1 1-9-9Z"/>
            </svg>
          </label>
    </div>
  </div>
  
<style>
    @import url('https://fonts.googleapis.com/css2?family=Geist+Mono&display=swap');
</style>
  