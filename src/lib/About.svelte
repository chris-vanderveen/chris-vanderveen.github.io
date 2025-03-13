<script>
  import { ChevronsDown } from 'lucide-svelte';
</script>

<div id="about" class="min-h-screen bg-gradient-to-b from-base-100 to-base-200 font-inter scroll-mt-16 flex flex-col">
  <div class="flex-1 flex flex-col">
    <div class="divider text-4xl font-regular before:bg-gradient-to-l before:from-base-content/30 before:to-transparent after:bg-gradient-to-r after:from-base-content/30 after:to-transparent mt-10">About Me</div>
    
    <div class="hero flex justify-center pt-[10vh]">
      <div class="hero-content flex-col xl:flex-row-reverse">
        <div class="avatar flex justify-center">
          <div class="mask mask-square w-96 h-96">
            <img src="https://avatar.iran.liara.run/public/boy" alt="Profile" />
          </div>
        </div>
        <div class="text-center xl:text-left max-w-2xl mx-auto">
          <div class="py-6 text-lg leading-relaxed space-y-4">
            <p>
              I'm a third-year Computing Science student at the University of Alberta with a genuine passion for technology. My coursework has provided me with a solid foundation across various domains, exposing me to different aspects of computer science from systems programming to software development.
            </p>
            
            <p>Throughout my academic journey, I've explored several areas of technology:</p>
            
            <ul class="list-disc pl-6 space-y-2 inline-block text-left">
              <li>Systems & Security: I've developed an appreciation for low-level programming and secure system design through courses like Operating Systems and Computer Architecture.</li>
              <li>AI/ML: I've gained exposure to machine learning concepts and data analysis tools in my coursework.</li>
              <li>Mobile Development: I've expanded my practical skills by creating a functional Android app using Java.</li>
            </ul>
            <p>
              I'm dedicated to continuously learning and expanding my technical toolkit. As I approach graduation, I'm eager to apply my skills in the tech industry, regardless of the specific domain. I'm adaptable, quick to learn, and excited about the opportunity to contribute to meaningful projects in a collaborative environment.
            </p>
          </div>
        </div>
      </div>
    </div>
    
    <div class="flex justify-center pt-[5vh]">
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
        class="cursor-pointer hidden sm:block hover:stroke-primary transition-colors"
      >
        <path d="m7 6 5 5 5-5"/>
        <path d="m7 13 5 5 5-5"/>
      </svg>
    </div>
  </div>
</div>

