<script>
  import ThemeSwitch from "$lib/components/Theme/ThemeSwitch.svelte"
  import GithubIcon from "$lib/assets/icons/github.svg.svelte"
</script>

<div class="sticky top-0 z-40 w-full border-slate-900/10 transition-[border-color] duration-500 dark:border-slate-50/[0.06] lg:z-50 lg:border-b">
  <div class="mx-auto max-w-4xl">
    <div class="mx-4 border-b border-slate-900/10 py-4 transition-[border-color] duration-500 dark:border-slate-50/[0.06] lg:mx-0 lg:border-0 lg:px-8">
      <div class="relative flex items-center">
        <a class="mr-3 md:w-auto" href="/">
          <span class="sr-only">renatodamas.com</span>
          <GithubIcon class="h-8 w-auto" />
        </a>
        <div class="relative ml-auto flex items-center">
          <div class="ml-6 flex items-center border-l border-slate-900/10 pl-6 duration-1000 dark:border-slate-50/[0.06]">
            <ThemeSwitch />
            <a
              href="https://github.com/codectl/renatodamas.com"
              class="ml-6 block text-slate-400 hover:text-slate-500 dark:hover:text-slate-300"
            >
              <span class="sr-only">Website on GitHub</span>
              <GithubIcon class="h-5 w-5" fill="currentColor" aria-hidden="true" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
