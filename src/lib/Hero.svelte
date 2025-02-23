<div class="hero main-hero bg-gradient-to-b from-base-200 to-base-100 flex items-center justify-center" style="height: calc(100vh - 64px);">
    <div class="hero-content text-center w-full p-0">
      <div class="max-w-3xl mx-auto">
        <h1 class="text-5xl font-regular" style="font-family: 'IBM Plex Mono', monospace;">Hello, World! <br><span class="text-neutral-500">I'm Chris Vander Veen</span></h1>
        <p class="py-6" style="font-family: 'IBM Plex Mono', monospace;">
          Exploring tech, learning always, building things.
        </p>

        <svg 
          on:click={() => {
            const aboutSection = document.getElementById('about');
            if (aboutSection) {
              aboutSection.scrollIntoView({ behavior: 'smooth' });
            }
          }}
          on:keydown={(e) => {
            if (e.key === 'Enter' || e.key === ' ') {
              const aboutSection = document.getElementById('about');
              if (aboutSection) {
                aboutSection.scrollIntoView({ behavior: 'smooth' });
              }
            }
          }}
          tabindex="0"
          role="button"
          xmlns="http://www.w3.org/2000/svg" 
          width="24" 
          height="24" 
          viewBox="0 0 24 24" 
          fill="none" 
          stroke="currentColor" 
          stroke-width="2" 
          stroke-linecap="round" 
          stroke-linejoin="round" 
          class="mx-auto cursor-pointer hover:stroke-primary transition-colors mt-16"
        >
          <path d="m7 6 5 5 5-5"/>
          <path d="m7 13 5 5 5-5"/>
        </svg>
      </div>
    </div>
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;700&display=swap');
</style>