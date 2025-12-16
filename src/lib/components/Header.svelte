<script lang="ts">
  import { onMount } from 'svelte';

  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 10;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<header class="fixed top-0 left-0 w-full z-50 transition-all duration-300 {isScrolled ? 'bg-white/90 backdrop-blur-sm py-4 shadow-sm' : 'bg-transparent py-8'}">
  <div class="container mx-auto px-6 md:px-12 flex justify-between items-center">
    <!-- Logo -->
    <a href="/" class="text-black hover:opacity-80 transition-opacity">
      <svg width="32" height="35" viewBox="0 0 97 105" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path opacity="0.5" d="M0.84375 29.5892V75.3785L43.791 45.7896V0L0.84375 29.5892Z" fill="currentColor"/>
        <path opacity="0.5" d="M0.84375 75.3787V29.5891L43.791 59.1783V104.968L0.84375 75.3787Z" fill="currentColor"/>
        <path opacity="0.5" d="M96.8438 29.5891V75.3787L53.8965 45.7895V0L96.8438 29.5891Z" fill="currentColor"/>
        <path opacity="0.5" d="M96.8438 75.3787V29.5891L53.8965 59.1783V104.968L96.8438 75.3787Z" fill="currentColor"/>
      </svg>
    </a>

    <!-- Navigation -->
    <nav class="hidden md:flex items-center space-x-8">
      {#each ['Philosophy', 'Sectors', 'Approach', 'Contact'] as item}
        <a href="#{item.toLowerCase()}" class="text-gray-600 hover:text-black text-sm font-medium transition-colors">
          {item}
        </a>
      {/each}
    </nav>
  </div>
</header>
