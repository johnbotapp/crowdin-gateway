<template>
  <div class="flex flex-grow items-center flex-col justify-center bg-[#21252B]">
    <div class="container flex gap-8 items-center flex-col justify-center">
      <div class="flex flex-col gap-2 items-center justify-center">
        <CrowdinLogo
          class="grayscale invert"
        />
        <h1 class="text-[#E2E5E9] text-lg">Please select a project to contribute!</h1>
      </div>
      <div class="grid gap-4 grid-cols-2">
        <a
          v-for="(project, index) in projects"
          :key="index"
          :href="project.link"
          target="_blank"
          class="flex cursor-pointer flex-col max-w-sm bg-[#2C3139] p-6 rounded-lg mt-4 border border-solid border-[#FFFFFF2e] hover:bg-[#FFFFFF0d] transition-colors duration-150 ease-in-out"
        >
          <h2 class="text-lg text-[#E2E5E9] !leading-none">{{ project.name }}</h2>
          <hr class="border-t border-solid border-[#FFFFFF1f] mt-3.5 mb-2.5" />
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
