<div id="projects" class="min-h-screen bg-gradient-to-b from-base-100 to-base-200 font-inter scroll-mt-16">
    <div class="flex w-full flex-col pt-10">
      <div class="divider text-4xl font-regular before:bg-base-content/30 after:bg-base-content/30">Projects</div>
      
      <div class="hero">
        <div class="hero-content flex-col lg:flex-row-reverse">
        </div>
      </div>
  
      <svg 
        on:click={() => {
          const contactSection = document.getElementById('contact');
          if (contactSection) {
            contactSection.scrollIntoView({ behavior: 'smooth' });
          }
        }}
        on:keydown={(e) => {
          if (e.key === 'Enter' || e.key === ' ') {
            const contactSection = document.getElementById('contact');
            if (contactSection) {
              contactSection.scrollIntoView({ behavior: 'smooth' });
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
        class="mx-auto cursor-pointer sm:block hover:stroke-primary transition-colors mt-16"
      >
        <path d="m7 6 5 5 5-5"/>
        <path d="m7 13 5 5 5-5"/>
      </svg>
    </div>
  </div>