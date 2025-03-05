<script>
  import { Linkedin, Mail } from 'lucide-svelte';
</script>

<!-- Desktop: Floating on left side, vertically centered -->
<div class="fixed left-6 top-1/2 -translate-y-1/2 z-40 hidden md:flex flex-col items-center ml-10">
  <div class="flex flex-col gap-6">
    <a href="https://github.com/yourusername" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
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
</div>

<!-- Mobile: Above chevron in each section -->
<div class="flex justify-center gap-6 mt-8 mb-4 md:hidden">
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
  <a href="https://linkedin.com/in/yourusername" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
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