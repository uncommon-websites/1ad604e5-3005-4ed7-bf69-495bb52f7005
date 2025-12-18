<script>
  import { onMount } from 'svelte';

  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 0;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<header class="sticky top-0 z-50 w-full bg-white transition-shadow duration-300" class:shadow-md={isScrolled}>
  <!-- Top Banner -->
  <div class="bg-white border-b border-gray-100 py-2 flex justify-center">
      <a href="#" class="inline-flex items-center gap-3 bg-[#FF8300] text-white text-[10px] font-medium tracking-wide px-4 py-1.5 rounded-full hover:bg-[#E07400] transition-colors">
        <span class="bg-white text-[#FF8300] px-1.5 py-0.5 rounded-[2px] text-[9px] font-bold">NEW</span>
        INTRODUCING LISTEN360 AI
      </a>
  </div>

  <!-- Main Nav -->
  <div class="max-w-[1400px] mx-auto px-6 h-20 flex items-center justify-between">
    <!-- Logo -->
    <a href="/" class="flex items-center gap-3">
      <svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M15.9735 31.7251V26.4703C21.8217 26.4207 26.5214 21.6331 26.4719 15.7791C26.4223 9.92411 21.6403 5.21896 15.793 5.26858C9.98026 5.31823 5.29456 10.0496 5.29456 15.869H2.47932e-05C-0.00745736 11.6554 1.67883 7.61601 4.67916 4.6609C10.9436 -1.55363 21.0398 -1.55363 27.3052 4.6609C33.491 10.7743 33.5546 20.7511 27.4474 26.9441C27.4006 26.9918 27.3529 27.0396 27.3052 27.0864C24.2955 30.0808 20.2159 31.7504 15.9735 31.7251Z" fill="#FF8300"/>
        <path d="M12.8328 31.7228H0V18.9922H5.29362V26.4671H12.8328V31.7228Z" fill="#EB0029"/>
      </svg>
      <span class="text-2xl font-bold tracking-tight text-black">Listen360</span>
    </a>

    <!-- Nav Links -->
    <nav class="hidden lg:flex items-center gap-8 text-[11px] font-medium tracking-widest uppercase text-gray-800">
      <button class="hover:text-gray-500 flex items-center gap-1 cursor-pointer">Solutions <svg width="8" height="8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m6 9 6 6 6-6"/></svg></button>
      <button class="hover:text-gray-500 flex items-center gap-1 cursor-pointer">Industries <svg width="8" height="8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m6 9 6 6 6-6"/></svg></button>
      <button class="hover:text-gray-500 flex items-center gap-1 cursor-pointer">Resources <svg width="8" height="8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m6 9 6 6 6-6"/></svg></button>
      <button class="hover:text-gray-500 flex items-center gap-1 cursor-pointer">Company <svg width="8" height="8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m6 9 6 6 6-6"/></svg></button>
    </nav>

    <!-- Right Actions -->
    <div class="flex items-center gap-6">
      <a href="#" class="text-[11px] font-medium tracking-widest uppercase hover:text-gray-500">Login</a>
      <a href="#" class="text-[11px] font-medium tracking-widest uppercase border border-[#FF8300] text-[#FF8300] px-5 py-3 hover:bg-[#FF8300] hover:text-white transition-colors">Get a Demo</a>
    </div>
  </div>
</header>
