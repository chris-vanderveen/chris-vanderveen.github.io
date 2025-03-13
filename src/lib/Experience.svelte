<script>
  import InfoCard from './InfoCard.svelte';
  
  // Example experience data - you can replace with your actual experience
  const experiences = [
    {
      title: "Business Development Intern",
      company: "Riipen Level-UP | TGT Solutions",
      period: "Feb 2025 - March 2025",
      description: "Developed comprehensive IT and cybersecurity product offerings for entrepreneurs and small businesses, including detailed pricing models. Created professional sales materials for multiple service lines including Disaster Recovery Planning, Cybersecurity Committee Establishment, and Incident Response Planning.\n\nResearched and packaged technical solutions such as Patch Management, EDR, Data Encryption, and Backup Systems into accessible offerings for individual entreprenuers and small businesses.",
      skills: [],
      variant: "left",
      githubUrl: ""
    },
    {
      title: "Language Data Annotator",
      company: "Transperfect DataForce",
      period: "July 2024 - Sept 2024",
      description: "Evaluated AI chatbot responses against quality, relevance, and safety benchmarks. Engineered and refined targeted prompts to assess model performance across various domains.\n\nPerformed comparative analysis between competing AI systems to identify strengths and weaknesses. Collaborated with annotation team to ensure consistent evaluation standards and quality control.",
      skills: [],
      variant: "right",
      githubUrl: ""
    },
    {
      title: "Coding Data Annotator",
      company: "DataAnnotation",
      period: "Jan 2024 - Sept 2024",
      description: "Evaluated AI-generated code snippets across multiple programming languages for correctness, efficiency, and adherence to style standards. Assessed algorithm implementations and data structures for functionality and performance optimization.\n\nDelivered comprehensive quality feedback with specific recommendations for code improvements and optimization techniques.",
      skills: ["HTML/CSS", "JavaScript", "Python"],
      variant: "left",
      githubUrl: ""
    },
    {
      title: "Lead Operator",
      company: "White Swan Environmental Ltd.",
      period: "June 2017 - Aug 2022",
      description: "Led a small team of operators in high-risk oilfield waste disposal operations, ensuring compliance with AER regulatory standards. Managed comprehensive data tracking systems through spreadsheets for daily operational analytics and reporting.\n\nDeveloped and implemented enhanced safety protocols that improved workplace safety metrics while maintaining operational efficiency. Demonstrated strong leadership and communication skills while coordinating complex logistics in hazardous materials handling.",
      skills: [],
      variant: "right",
      githubUrl: ""
    }
  ];
</script>

<div id="experience" class="min-h-screen bg-gradient-to-b from-base-200 to-base-100 font-inter scroll-mt-16">
  <div class="flex w-full flex-col pt-10">
    <div class="divider text-4xl font-regular before:bg-base-content/30 after:bg-base-content/30">Experience</div>
    
    <div class="container mx-auto px-[5vw] pt-[10vh]">
      {#each experiences as experience, i}
        <InfoCard 
          title={experience.title}
          company={experience.company}
          period={experience.period}
          description={experience.description}
          skills={experience.skills}
          variant={i % 2 === 0 ? "left" : "right"}
          githubUrl={experience.githubUrl}
        />
      {/each}
    </div>

    <svg 
      on:click={() => {
        const projectsSection = document.getElementById('projects');
        if (projectsSection) {
          projectsSection.scrollIntoView({ behavior: 'smooth' });
        }
      }}
      on:keydown={(e) => {
        if (e.key === 'Enter' || e.key === ' ') {
          const projectsSection = document.getElementById('experience');
          if (projectsSection) {
            projectsSection.scrollIntoView({ behavior: 'smooth' });
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
      class="mx-auto cursor-pointer sm:block hover:stroke-primary transition-colors mt-[5vh]"
    >
      <path d="m7 6 5 5 5-5"/>
      <path d="m7 13 5 5 5-5"/>
    </svg>
  </div>
</div>