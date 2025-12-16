<script>
  const portfolioImages = [
    {
      name: "REAL ESTATE",
      category: "Infrastructure",
      image: "/generated/image-modern-office-building-with-glass-facade-1765927386130-0.webp", 
      alt: "Modern sustainable office building"
    },
    {
      name: "RENEWABLE ENERGY",
      category: "Clean Infrastructure",
      image: "/generated/image-solar-panel-farm-with-wind-turbines-in-b-1765927389507-1.webp",
      alt: "Solar and wind energy infrastructure"
    },
    {
      name: "REAL ASSETS",
      category: "Global Trade",
      image: "/generated/image-aerial-view-of-industrial-port-with-carg-1765927392560-2.webp",
      alt: "Industrial port infrastructure"
    },
    {
      name: "OPERATING COMPANIES",
      category: "Development",
      image: "/generated/image-modern-residential-development-with-gree-1765927395545-3.webp",
      alt: "Sustainable residential development"
    }
  ];
</script>

<section class="pt-32 pb-16 md:pt-48 md:pb-24 overflow-hidden">
  <div class="container mx-auto px-6 md:px-12 mb-16">
    <h1 class="font-display text-5xl md:text-7xl leading-[1.1] text-gray-900 max-w-4xl">
      Long-duration capital,<br />
      <span class="italic font-normal">fundamentals-led</span> approach.
    </h1>
  </div>

  <div class="pl-6 md:pl-12 overflow-x-auto pb-8 scrollbar-hide">
    <div class="flex space-x-1 min-w-max">
      {#each portfolioImages as item, i}
        <div class="relative group w-[300px] md:w-[400px]">
          <div class="aspect-[3/4] overflow-hidden bg-gray-100 relative">
            <img 
              src={item.image} 
              alt={item.alt}
              class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105"
            />
            {#if i === 0}
              <button class="absolute bottom-4 left-4 w-8 h-8 bg-white rounded-full flex items-center justify-center hover:scale-110 transition-transform" aria-label="Pause">
                <svg width="10" height="12" viewBox="0 0 10 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <rect width="3" height="12" rx="1.5" fill="black"/>
                  <rect x="7" width="3" height="12" rx="1.5" fill="black"/>
                </svg>
              </button>
              <div class="absolute bottom-0 left-0 w-full h-1 bg-gray-200">
                <div class="h-full bg-primary-600 w-1/3"></div>
              </div>
            {/if}
          </div>
          <div class="mt-4 flex items-baseline space-x-2">
            <span class="text-xs font-bold tracking-widest uppercase text-gray-900">{item.name}</span>
            <span class="text-xs font-serif italic text-gray-500">{item.category}</span>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>
