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
      <a href="#" class="inline-flex items-center gap-3 bg-[#FF4438] text-white text-[10px] font-medium tracking-wide px-4 py-1.5 rounded-full hover:bg-[#E03025] transition-colors">
        <span class="bg-white text-[#FF4438] px-1.5 py-0.5 rounded-[2px] text-[9px] font-bold">NEW</span>
        ADOPTION, SCALE & IMPACT REPORT
      </a>
  </div>

  <!-- Main Nav -->
  <div class="max-w-[1400px] mx-auto px-6 h-20 flex items-center justify-between">
    <!-- Logo -->
    <a href="/" class="text-4xl font-serif tracking-tight text-black">
      ABRIDGE
    </a>

    <!-- Nav Links -->
    <nav class="hidden lg:flex items-center gap-8 text-[11px] font-medium tracking-widest uppercase text-gray-800">
      <button class="hover:text-gray-500 flex items-center gap-1 cursor-pointer">Platform <svg width="8" height="8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m6 9 6 6 6-6"/></svg></button>
      <button class="hover:text-gray-500 flex items-center gap-1 cursor-pointer">AI <svg width="8" height="8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m6 9 6 6 6-6"/></svg></button>
      <button class="hover:text-gray-500 flex items-center gap-1 cursor-pointer">Resources <svg width="8" height="8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m6 9 6 6 6-6"/></svg></button>
      <button class="hover:text-gray-500 flex items-center gap-1 cursor-pointer">About <svg width="8" height="8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m6 9 6 6 6-6"/></svg></button>
    </nav>

    <!-- Right Actions -->
    <div class="flex items-center gap-6">
      <a href="#" class="text-[11px] font-medium tracking-widest uppercase hover:text-gray-500">Login</a>
      <a href="#" class="text-[11px] font-medium tracking-widest uppercase border border-[#FF4438] text-[#FF4438] px-5 py-3 hover:bg-[#FF4438] hover:text-white transition-colors">Contact Us</a>
    </div>
  </div>
</header>
