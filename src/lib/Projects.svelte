<script>
  import InfoCard from './InfoCard.svelte';
  import Footer from './Footer.svelte';
  
  // Example experience data - you can replace with your actual experience
  const experiences = [
    {
      title: "chris-vanderveen.github.io",
      company: "",
      period: "Feb 2024 - Ongoing",
      description: "Designed and implemented a responsive personal website using modern web technologies including Svelte, TypeScript, and TailwindCSS. Leveraged DaisyUI component library for enhanced UI elements\n\nDeployed and configured continuous integration pipeline through GitHub Pages for seamless updates and version control.",
      skills: ["Svelte", "Javascript/Typescript"],
      variant: "left",
      githubUrl: "https://github.com/chris-vanderveen/chris-vanderveen.github.io"
    },
    {
      title: "Conclave",
      company: "",
      period: "Jan 2024 - Apr 2024",
      description: "Collaborated on a full-featured Android event planning application using Java and Firebase database integration. Implemented secure user authentication system and designed database architecture for event management.\n\nDeveloped core functionality including QR code scanning capabilities, interactive map integration, and differentiated user/admin experiences. Applied software engineering best practices including version control, agile methodologies, and iterative testing throughout the development lifecycle.",
      skills: ["Java", "XML", "Firebase", "Android Studio"],
      variant: "right",
      githubUrl: "https://github.com/CMPUT301W24T08/DroidDesign"
    },
    {
      title: "F1 Telemetry",
      company: "",
      period: "",
      description: "Developed an F1 telemetry application in Rust that captures and processes real-time car data from the F1 video games. Implemented efficient UDP packet deserialization and JSON serialization for multiple telemetry data types including motion, session, and lap data.",
      skills: ["Rust", "JSON", "Serde"],
      variant: "left",
      githubUrl: "https://github.com/chris-vanderveen/F1-Telemetry"
    }
  ];
</script>

<div id="projects" class="bg-gradient-to-b from-base-100 to-base-200 font-inter scroll-mt-16">
  <div class="flex w-full flex-col">
    <div class="divider text-4xl font-regular before:bg-base-content/30 after:bg-base-content/30">Projects</div>
    
    <div class="container mx-auto px-[5vw] pt-[15vh] pb-16">
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
  </div>

  <div class="mt-auto pt-[16vh]">
    <Footer />
  </div>
</div>
