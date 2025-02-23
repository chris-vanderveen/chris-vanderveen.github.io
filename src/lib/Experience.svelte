<div id="experience" class="min-h-screen bg-gradient-to-b from-base-100 to-base-200 font-inter scroll-mt-16">
    <div class="flex w-full flex-col">
      <div class="divider text-4xl font-regular before:bg-base-content/30 after:bg-base-content/30">Experience</div>
      
      <div class="hero">
        <div class="hero-content flex-col lg:flex-row-reverse">
        </div>
      </div>
  
      <svg 
        on:click={() => {
          const experienceSection = document.getElementById('experience');
          if (experienceSection) {
            experienceSection.scrollIntoView({ behavior: 'smooth' });
          }
        }}
        on:keydown={(e) => {
          if (e.key === 'Enter' || e.key === ' ') {
            const experienceSection = document.getElementById('experience');
            if (experienceSection) {
              experienceSection.scrollIntoView({ behavior: 'smooth' });
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