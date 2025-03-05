<div id="about" class="min-h-screen bg-gradient-to-b from-base-100 to-base-200 font-inter scroll-mt-16">
  <div class="flex w-full flex-col pt-10">
    <div class="divider text-4xl font-regular before:bg-base-content/30 after:bg-base-content/30">About Me</div>
    
    <div class="hero">
      <div class="hero-content flex-col lg:flex-row-reverse">
        <div class="avatar">
          <div class="mask mask-square w-96 h-96">
            <img src="https://avatar.iran.liara.run/public/boy" alt="Profile" />
          </div>
        </div>
        <div>
          <div class="py-6 text-lg leading-relaxed space-y-4">
            <p>
              I'm a third-year Computing Science student at the University of Alberta with a passion for technology. My coursework has given me hands-on experience in various areas, but I've found a particular passion for systems programming. Classes like Operating Systems and Computer Architecture have let me dive deep into languages such as C and in my free time I've been learning Rust.
            </p>
            
            <p>I've also broadened my skills in other areas:</p>
            
            <ul class="list-disc pl-6 space-y-2">
              <li>AI/ML: I built projects using Python, PyTorch, and tools like Pandas in my Machine Learning and Reinforcement Learning courses.</li>
              <li>Security: I developed a strong interest in cryptography and enjoy the challenge of solving its complex puzzles.</li>
              <li>Mobile Development: I expanded my skill set by creating a functional Android app using Java.</li>
            </ul>
            <p>
              I'm now looking for opportunities where I can grow and contribute my technical skills. While I love development work, I'm also open to roles in project management or technical consulting. Ultimately, I want to tackle interesting problems with a team that values continuous learning.
            </p>
          </div>
        </div>
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
      class="mx-auto cursor-pointer sm:block hover:stroke-primary transition-colors mt-16"
    >
      <path d="m7 6 5 5 5-5"/>
      <path d="m7 13 5 5 5-5"/>
    </svg>
  </div>
</div>

