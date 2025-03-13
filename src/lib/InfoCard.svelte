<script lang="ts">
  export let title = "";
  export let company = "";
  export let period = "";
  export let description = "";
  export let variant = "left"; // "left" or "right"
  export let skills: string[] = []; // Optional array of skills/technologies
  export let githubUrl: string = ""; // Optional GitHub repository URL
</script>

<div class="card w-full bg-base-100 shadow-xl my-6 rounded-md border border-base-300">
  <div class="card-body p-6">
    <!-- Mobile layout (always title first, then description) -->
    <div class="flex flex-col md:hidden gap-6">
      <!-- Company Info Section (always on top for mobile) -->
      <div>
        <div class="flex items-center gap-2">
          <h2 class="card-title text-xl font-bold">{title}</h2>
          {#if githubUrl}
            <a href={githubUrl} target="_blank" rel="noopener noreferrer" class="hover:text-primary transition-colors" aria-label="GitHub Repository">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-github">
                <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path>
              </svg>
            </a>
          {/if}
        </div>
        <p class="text-lg font-medium text-primary">{company}</p>
        <p class="text-sm opacity-70">{period}</p>
        
        {#if skills.length > 0}
          <div class="mt-3">
            <div class="flex flex-wrap gap-2">
              {#each skills as skill}
                <span class="badge badge-outline">{skill}</span>
              {/each}
            </div>
          </div>
        {/if}
      </div>
      
      <!-- Description Section (always below for mobile) -->
      <div>
        <p class="whitespace-pre-line">{description}</p>
      </div>
    </div>

    <!-- Desktop layout (maintains left/right variants) -->
    <div class="hidden md:flex md:flex-row gap-6">
      {#if variant === "left"}
        <!-- Left variant layout -->
        <!-- Company Info Section -->
        <div class="md:w-1/3">
          <div class="flex items-center gap-2">
            <h2 class="card-title text-xl font-bold">{title}</h2>
            {#if githubUrl}
              <a href={githubUrl} target="_blank" rel="noopener noreferrer" class="hover:text-primary transition-colors" aria-label="GitHub Repository">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-github">
                  <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path>
                </svg>
              </a>
            {/if}
          </div>
          <p class="text-lg font-medium text-primary">{company}</p>
          <p class="text-sm opacity-70">{period}</p>
          
          {#if skills.length > 0}
            <div class="mt-3">
              <div class="flex flex-wrap gap-2">
                {#each skills as skill}
                  <span class="badge badge-outline">{skill}</span>
                {/each}
              </div>
            </div>
          {/if}
        </div>
        
        <!-- Divider for desktop -->
        <div class="md:w-px bg-base-300"></div>
        
        <!-- Description Section -->
        <div class="md:w-2/3">
          <p class="whitespace-pre-line">{description}</p>
        </div>
      {:else}
        <!-- Right variant layout -->
        <!-- Description Section -->
        <div class="md:w-2/3">
          <p class="whitespace-pre-line">{description}</p>
        </div>
        
        <!-- Divider for desktop -->
        <div class="md:w-px bg-base-300"></div>
        
        <!-- Company Info Section -->
        <div class="md:w-1/3">
          <div class="flex items-center gap-2">
            <h2 class="card-title text-xl font-bold">{title}</h2>
            {#if githubUrl}
              <a href={githubUrl} target="_blank" rel="noopener noreferrer" class="hover:text-primary transition-colors" aria-label="GitHub Repository">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-github">
                  <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path>
                </svg>
              </a>
            {/if}
          </div>
          <p class="text-lg font-medium text-primary">{company}</p>
          <p class="text-sm opacity-70">{period}</p>
          
          {#if skills.length > 0}
            <div class="mt-3">
              <div class="flex flex-wrap gap-2">
                {#each skills as skill}
                  <span class="badge badge-outline">{skill}</span>
                {/each}
              </div>
            </div>
          {/if}
        </div>
      {/if}
    </div>
  </div>
</div>
