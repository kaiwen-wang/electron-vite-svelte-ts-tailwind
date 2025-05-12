<script lang="ts">
  import Versions from './components/Versions.svelte'
  import electronLogo from './assets/electron.svg'

  const ipcHandle = (): void => window.electron.ipcRenderer.send('ping')
</script>

<img
  alt="logo"
  class="mb-5 h-32 w-32 transition-[filter] duration-300 hover:drop-shadow-[0_0_1.2em_#6988e6aa]"
  src={electronLogo}
/>
<div class="text-sm leading-4 text-[var(--ev-c-text-2)] font-bold mb-[10px] pt-4">
  Powered by electron-vite
</div>
<div
  class="text-[28px] text-[var(--ev-c-text-1)] font-bold leading-8 text-center mx-[10px] py-4 px-0"
>
  Build an Electron app with
  <span
    class="bg-gradient-to-br from-[#ff3e00] from-35% to-[#647eff] bg-clip-text text-transparent font-bold"
    >Svelte</span
  >,
  <span
    class="bg-gradient-to-br from-[#3178c6] from-45% to-[#f0dc4e] bg-clip-text text-transparent font-bold"
    >TypeScript</span
  >, and
  <span
    class="bg-gradient-to-br from-[#06b6d4] from-40% to-[#a855f7] bg-clip-text text-transparent font-bold"
    >Tailwind CSS</span
  >
</div>
<p class="text-base leading-6 text-[var(--ev-c-text-2)] font-semibold">
  Please try pressing <code
    class="font-semibold px-[5px] py-[3px] rounded-[2px] bg-[var(--color-background-mute)] font-mono text-[85%]"
    >F12</code
  > to open the devTool
</p>
<div class="flex pt-8 m-[-6px] flex-wrap justify-start">
  <div class="flex-shrink-0 p-[6px]">
    <a
      href="https://electron-vite.org/"
      target="_blank"
      rel="noreferrer"
      class="cursor-pointer no-underline inline-block border border-transparent text-center font-semibold whitespace-nowrap rounded-[20px] px-5 py-0 leading-[38px] text-sm border-[var(--ev-button-alt-border)] text-[var(--ev-button-alt-text)] bg-[var(--ev-button-alt-bg)] hover:border-[var(--ev-button-alt-hover-border)] hover:text-[var(--ev-button-alt-hover-text)] hover:bg-[var(--ev-button-alt-hover-bg)]"
      >Documentation</a
    >
  </div>
  <div class="flex-shrink-0 p-[6px]">
    <!-- svelte-ignore a11y-click-events-have-key-events a11y-no-static-element-interactions a11y-missing-attribute-->
    <a
      target="_blank"
      rel="noreferrer"
      on:click={ipcHandle}
      class="cursor-pointer no-underline inline-block border border-transparent text-center font-semibold whitespace-nowrap rounded-[20px] px-5 py-0 leading-[38px] text-sm border-[var(--ev-button-alt-border)] text-[var(--ev-button-alt-text)] bg-[var(--ev-button-alt-bg)] hover:border-[var(--ev-button-alt-hover-border)] hover:text-[var(--ev-button-alt-hover-text)] hover:bg-[var(--ev-button-alt-hover-bg)]"
      >Send IPC</a
    >
  </div>
</div>
<Versions />
