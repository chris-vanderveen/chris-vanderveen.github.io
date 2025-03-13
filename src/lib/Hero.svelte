<script>
  import { Github, Linkedin, Mail } from 'lucide-svelte';
</script>

<div class="hero main-hero bg-gradient-to-b from-base-200 to-base-100 flex items-center justify-center" style="height: calc(100vh - 64px);">
    <div class="hero-content text-center w-full p-0">
      <div class="max-w-3xl mx-auto">
        <h1 class="text-5xl font-regular" style="font-family: 'IBM Plex Mono', monospace;">Hello, World! <br><span class="text-neutral-500">I'm Chris Vander Veen</span></h1>
        <p class="py-6" style="font-family: 'IBM Plex Mono', monospace;">
          Exploring tech, continuously learning, building things.
        </p>

        <!-- Social Icons -->
        <div class="flex justify-center gap-6 mt-8">
          <a href="https://github.com/chris-vanderveen" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
            <svg 
              xmlns="http://www.w3.org/2000/svg" 
              width="24" 
              height="24" 
              viewBox="0 0 24 24" 
              fill="none" 
              stroke="currentColor" 
              stroke-width="2" 
              stroke-linecap="round" 
              stroke-linejoin="round" 
              class="hover:stroke-primary transition-colors"
            >
              <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path>
            </svg>
          </a>
          <a href="https://www.linkedin.com/in/chris-vanderveen/" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
            <Linkedin class="w-6 h-6 hover:stroke-primary transition-colors" />
          </a>
          <button 
            on:click={() => {
              const contactSection = document.getElementById('contact');
              if (contactSection) {
                contactSection.scrollIntoView({ behavior: 'smooth' });
              }
            }}
            aria-label="Contact me"
            class="cursor-pointer"
          >
            <Mail class="w-6 h-6 hover:stroke-primary transition-colors" />
          </button>
        </div>

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
          class="mx-auto cursor-pointer hover:stroke-primary transition-colors mt-[10vh]"
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