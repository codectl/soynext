<script lang="ts">
  import { onMount } from "svelte"
  import { Icon, Moon, Sun } from "svelte-hero-icons";

  let theme: string

  onMount(() => {
    const systemPreferredTheme = window.matchMedia("(prefers-color-scheme: dark)").matches ? "dark" : "light"
    theme = localStorage.theme ?? systemPreferredTheme
    setTheme(theme)
  })

  const toggleTheme = () => setTheme(theme === "dark" ? "light" : "dark")

  const setTheme = (value: string) => {
    theme = value
    document.body.classList.remove("light", "dark")
    document.body.classList.add(theme)

    localStorage.theme = theme
    if (window.matchMedia(`(prefers-color-scheme: ${localStorage.theme})`).matches)
      localStorage.removeItem("theme")
  }
</script>

<button
  type="button"
  class="text-slate-400 hover:text-slate-500 dark:hover:text-slate-300"
  on:click={() => toggleTheme()}
>
  <span class="sr-only">Theme</span>
  <Icon class="h-6 w-6" src={ theme === "dark" ? Moon : Sun} />
</button>
