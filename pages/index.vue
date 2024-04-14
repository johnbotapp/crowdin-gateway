<template>
  <div class="flex grow flex-col items-center justify-center bg-[#21252B]">
    <div class="container flex flex-col items-center justify-center gap-8 p-4">
      <div class="flex flex-col items-center justify-center gap-2">
        <CrowdinLogo
          class="grayscale invert"
        />
        <h1 class="text-center text-lg text-[#E2E5E9]">Please select a project to contribute!</h1>
      </div>
      <div class="grid grid-cols-1 gap-4 md:grid-cols-2 md:gap-8">
        <a
          v-for="(project, index) in projects"
          :key="index"
          :href="project.link"
          target="_blank"
          class="flex max-w-sm cursor-pointer flex-col rounded-lg border border-solid border-[#FFFFFF2e] bg-[#2C3139] p-6 transition-colors duration-150 ease-in-out hover:bg-[#FFFFFF0d]"
        >
          <h2 class="text-lg !leading-none text-[#E2E5E9]">{{ project.name }}</h2>
          <hr class="mb-2.5 mt-3.5 border-t border-solid border-[#FFFFFF1f]" />
          <p class="text-sm text-[#BDC1C6]">{{ project.description }}</p>
        </a>
      </div>
    </div>
  </div>
</template>

<script setup>
  const projects = [{
    name: "John-Bot",
    description: "John-Bot is an ambitious Discord bot project. Initially available only in French, we're now looking to expand internationally!",
    link: "https://crowdin.com/project/johnbot",
  }, {
    name: "John-Bot Website",
    description: "The website of John-Bot, an ambitious Discord bot project. Initially available only in French, we're now looking to expand internationally!",
    link: "https://crowdin.com/project/johnbot-website",
  }];

</script>
