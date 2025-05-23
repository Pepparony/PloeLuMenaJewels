<script>
    // Mobile menu state
    let isOpen = false;
    
    // Toggle mobile menu
    function toggleMenu() {
      isOpen = !isOpen;
      // Prevent scrolling when menu is open
      if (isOpen) {
        document.body.style.overflow = 'hidden';
      } else {
        document.body.style.overflow = 'auto';
      }
    }
  
    // Close menu on link click
    function handleNavClick() {
      isOpen = false;
      document.body.style.overflow = 'auto';
    }
  
     // Team members data
     const teamMembers = [
      {
        name: "James Mitchell",
        title: "Founder & Master Jeweler",
        bio: "With over 20 years of experience in jewelry crafting, James brings passion and precision to every custom piece he creates.",
        image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=800&h=800&fit=crop"
      },
      {
        name: "Sarah Chen",
        title: "Lead Designer",
        bio: "Sarah's innovative designs blend traditional techniques with modern aesthetics, creating unique pieces that tell your story.",
        image: "https://images.unsplash.com/photo-1494790108377-be9c29b29330?w=800&h=800&fit=crop"
      },
      {
        name: "Maria Rodriguez",
        title: "Gemstone Specialist",
        bio: "Maria's expertise in precious stones ensures each piece features the perfect gems to bring your vision to life.",
        image: "https://images.unsplash.com/photo-1580489944761-15a19d654956?w=800&h=800&fit=crop"
      }
    ];
  
      // Features data
      const features = [
      {
        title: "Custom Design Process",
        description: "Work directly with our master jewelers to bring your dream piece to life. From initial sketches to final polish, we guide you through every step of creating your perfect jewelry.",
        image: "https://images.unsplash.com/photo-1515709980177-7a7d628c09ba?w=800&h=600&fit=crop",
        benefits: [
          "One-on-one design consultations",
          "3D renderings before crafting"
        ],
        imagePosition: "right"
      },
      {
        title: "Ethically Sourced Materials",
        description: "We use only conflict-free diamonds and responsibly sourced precious metals. Every stone comes with certification, ensuring your jewelry is as ethical as it is beautiful.",
        image: "https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?w=800&h=600&fit=crop",
        benefits: [
          "Certified conflict-free diamonds",
          "Recycled precious metals available"
        ],
        imagePosition: "left"
      },
      {
        title: "Lifetime Warranty & Care",
        description: "Your custom jewelry is protected by our comprehensive lifetime warranty. We offer free cleaning, inspection, and maintenance to keep your pieces sparkling for generations.",
        image: "https://images.unsplash.com/photo-1630019852942-f89202989a59?w=800&h=600&fit=crop",
        benefits: [
          "Free annual cleanings",
          "Lifetime craftsmanship warranty"
        ],
        imagePosition: "right"
      }
    ];
  
  // Jewelry collections data
  const collections = [
      {
        category: "Engagement Rings",
        custom: [
          "Completely personalized designs tailored to your love story",
          "Choice of any precious metal and stone combination"
        ],
        readyMade: [
          "Limited selection of pre-designed styles",
          "Fixed sizes and stone options with minimal customization"
        ]
      },
      {
        category: "Wedding Bands",
        custom: [
          "Matching sets designed to complement your engagement ring",
          "Engraving and unique texture options available"
        ],
        readyMade: [
          "Standard band styles in common sizes",
          "Generic designs that may not match your ring perfectly"
        ]
      },
      {
        category: "Anniversary Gifts",
        custom: [
          "Incorporate birthstones and meaningful symbols",
          "Transform heirloom jewelry into modern pieces"
        ],
        readyMade: [
          "Mass-produced designs lacking personal significance",
          "Cannot incorporate sentimental elements"
        ]
      },
      {
        category: "Special Occasions",
        custom: [
          "Design pieces that tell your unique story",
          "Perfect for milestone birthdays, graduations, or achievements"
        ],
        readyMade: [
          "Generic gift options without personal meaning",
          "One-size-fits-all approach to special moments"
        ]
      },
      {
        category: "Customer Satisfaction",
        custom: [
          "100% satisfaction with 5/5 average rating"
        ],
        readyMade: [
          "Mixed reviews with 3.5/5 average rating"
        ],
        hasRating: true,
        customRating: 5,
        readyMadeRating: 3.5
      }
    ];
  </script>
  
  <head>
    <title>Handcrafted Custom Jewelry | Ploe LuMena Jewels</title>
  </head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <section id="yeah">
    
  
  
  <div class="w-screen bg-[#a855f7] text-white flex text-center justify-center items-center absolute p-2 top-0 fixed z-100">
    <p class="text-lg tracking-wide">✨ Holiday Sale - 20% off all custom orders! ✨</p>
  </div>
  
  <nav class="flex w-full justify-between md:justify-between items-center bg-[#faf5ff] px-4 md:px-8 lg:px-16 mt-10 py-6">
    <!-- Logo Section -->
    <div class="px-4">
      <a href="/" class="w-fit h-fit">
        <h1 class="text-2xl font-bold text-[#a855f7]">Ploe LuMena Jewels</h1>
      </a>
    </div>
    
    <!-- Desktop Navigation Links - Hidden on mobile -->
    <div class="hidden md:flex text-lg space-x-6">
      <a class="transition-all duration-200 underline-offset-8 hover:underline text-lg" href="/collections">Collections</a>
      <a class="transition-all duration-200 underline-offset-8 hover:underline text-lg" href="/custom">Custom Design</a>
      <a class="transition-all duration-200 underline-offset-8 hover:underline text-lg" href="/about">Our Story</a>
      <a class="transition-all duration-200 underline-offset-8 hover:underline text-lg" href="/gallery">Gallery</a>
      <a class="transition-all duration-200 underline-offset-8 hover:underline text-lg" href="/contact">Contact</a>
    </div>
    
    <!-- Desktop Phone Number - Hidden on mobile -->
    <div class="hidden md:flex justify-end text-lg items-center space-x-2">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M22 12C22 10.6868 21.7413 9.38647 21.2388 8.1731C20.7362 6.95996 19.9997 5.85742 19.0711 4.92896C18.1425 4.00024 17.0401 3.26367 15.8268 2.76123C14.6136 2.25854 13.3132 2 12 2V4C13.0506 4 14.0909 4.20703 15.0615 4.60889C16.0321 5.01099 16.914 5.60034 17.6569 6.34326C18.3997 7.08594 18.989 7.96802 19.391 8.93848C19.7931 9.90918 20 10.9495 20 12H22Z" fill="currentColor" />
        <path d="M2 10V5C2 4.44775 2.44772 4 3 4H8C8.55228 4 9 4.44775 9 5V9C9 9.55225 8.55228 10 8 10H6C6 14.4182 9.58173 18 14 18V16C14 15.4478 14.4477 15 15 15H19C19.5523 15 20 15.4478 20 16V21C20 21.5522 19.5523 22 19 22H14C7.37259 22 2 16.6274 2 10Z" fill="currentColor" />
        <path d="M17.5433 9.70386C17.8448 10.4319 18 11.2122 18 12H16.2C16.2 11.4485 16.0914 10.9023 15.8803 10.3928C15.6692 9.88306 15.3599 9.42017 14.9698 9.03027C14.5798 8.64014 14.1169 8.33081 13.6073 8.11963C13.0977 7.90869 12.5515 7.80005 12 7.80005V6C12.7879 6 13.5681 6.15527 14.2961 6.45679C15.024 6.7583 15.6855 7.2002 16.2426 7.75732C16.7998 8.31445 17.2418 8.97583 17.5433 9.70386Z" fill="currentColor" />
      </svg>
      <a href="tel:555-0123">Book Consultation</a>
    </div>
    
    <!-- Mobile Menu Button - Only visible on mobile -->
    <button class="md:hidden p-2 rounded-lg hover:bg-gray-100" on:click={toggleMenu}>
      {#if !isOpen}
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
        </svg>
      {:else}
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
        </svg>
      {/if}
    </button>
  </nav>
  
  <!-- Mobile Menu Dropdown - Fixed position, slides down when active -->
  {#if isOpen}
    <div class="fixed inset-x-0 z-40 bg-[#a855f7] md:hidden" style="top: 80px;">
      <div class="flex flex-col px-6 py-8 space-y-6">
        <!-- Mobile Navigation Links -->
        <a href="/collections" class="text-white text-xl font-semibold hover:text-gray-200 transition-colors duration-200" on:click={handleNavClick}>Collections</a>
        <a href="/custom" class="text-white text-xl font-semibold hover:text-gray-200 transition-colors duration-200" on:click={handleNavClick}>Custom Design</a>
        <a href="/about" class="text-white text-xl font-semibold hover:text-gray-200 transition-colors duration-200" on:click={handleNavClick}>Our Story</a>
        <a href="/gallery" class="text-white text-xl font-semibold hover:text-gray-200 transition-colors duration-200" on:click={handleNavClick}>Gallery</a>
        <a href="/contact" class="text-white text-xl font-semibold hover:text-gray-200 transition-colors duration-200" on:click={handleNavClick}>Contact</a>
  
        <!-- Mobile Phone Number -->
        <div class="flex items-center space-x-2 pt-6">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M22 12C22 10.6868 21.7413 9.38647 21.2388 8.1731C20.7362 6.95996 19.9997 5.85742 19.0711 4.92896C18.1425 4.00024 17.0401 3.26367 15.8268 2.76123C14.6136 2.25854 13.3132 2 12 2V4C13.0506 4 14.0909 4.20703 15.0615 4.60889C16.0321 5.01099 16.914 5.60034 17.6569 6.34326C18.3997 7.08594 18.989 7.96802 19.391 8.93848C19.7931 9.90918 20 10.9495 20 12H22Z" fill="white" />
            <path d="M2 10V5C2 4.44775 2.44772 4 3 4H8C8.55228 4 9 4.44775 9 5V9C9 9.55225 8.55228 10 8 10H6C6 14.4182 9.58173 18 14 18V16C14 15.4478 14.4477 15 15 15H19C19.5523 15 20 15.4478 20 16V21C20 21.5522 19.5523 22 19 22H14C7.37259 22 2 16.6274 2 10Z" fill="white" />
            <path d="M17.5433 9.70386C17.8448 10.4319 18 11.2122 18 12H16.2C16.2 11.4485 16.0914 10.9023 15.8803 10.3928C15.6692 9.88306 15.3599 9.42017 14.9698 9.03027C14.5798 8.64014 14.1169 8.33081 13.6073 8.11963C13.0977 7.90869 12.5515 7.80005 12 7.80005V6C12.7879 6 13.5681 6.15527 14.2961 6.45679C15.024 6.7583 15.6855 7.2002 16.2426 7.75732C16.7998 8.31445 17.2418 8.97583 17.5433 9.70386Z" fill="white" />
          </svg>
          <a href="tel:555-0123" class="text-white text-xl" on:click={handleNavClick}>Book Consultation</a>
        </div>
        
        <!-- Mobile CTA Button -->
        <a href="/custom" class="mt-6 rounded-xl w-fit px-8 py-3 bg-white text-[#a855f7] text-bold text-xl flex justify-center items-center transition-all duration-100 hover:bg-gray-100" on:click={handleNavClick}>
          <p class="mr-2">Start Your Design</p>
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M23.0677 11.9929L18.818 7.75739L17.4061 9.17398L19.2415 11.0032L0.932469 11.0012L0.932251 13.0012L19.2369 13.0032L17.4155 14.8308L18.8321 16.2426L23.0677 11.9929Z" fill="currentColor" />
          </svg>
        </a>
      </div>
    </div>
  {/if}
  <section class="flex w-screen justify-center items-center relative bg-grayscale-100 bg-no-repeat bg-cover">
    <div class="relative top-0 w-full h-[425px] sm:h-[400px] md:h-[500px] lg:h-[600px] overflow-hidden">
      <img class="w-full h-full object-cover grayscale-75" src="u9283747978_fill_in_--ar_21_--v_6.1_01ca5601-532f-40b2-b4f2-87d504f189a5_0.png" alt="Custom jewelry showcase">
    </div>
    <div class="flex flex-col w-[90%] sm:w-[80%] md:w-[70%] justify-center items-center text-white font-sans z-20 absolute py-6 sm:py-12 md:py-20 lg:py-35">
      <p class="text-base sm:text-lg uppercase mb-2 sm:mb-4 md:mb-6">Handcrafted with Love</p>
      <h1 class="text-3xl md:text-5xl lg:text-6xl text-center font-bold tracking-wide mb-2 leading-[1.1]">Custom Handmade <br>Jewelry That Tells Your Story</h1>
      <svg class="w-[65%] sm:w-[60%] md:w-[55%] mb-2 sm:mb-4 md:mb-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 300 20">
          <!-- The skinny subtle smile curve for an underline -->
          <path d="M 10,12 Q 150,6 290,12" stroke="#FFFFFF" stroke-width="1.5" fill="none" />
      </svg>
      <a href="/custom" class="mb-3 sm:mb-4 md:mb-5 rounded-xl w-fit px-6 sm:px-10 md:px-15 py-2 sm:py-2.5 md:py-3 bg-[#a855f7] text-bold text-lg sm:text-xl md:text-2xl flex justify-center items-center transition-all duration-100 hover:opacity-90 text-white">
        <p class="mr-2">Design Your Piece</p>
        <svg width="20" height="20" sm:width="22" sm:height="22" md:width="24" md:height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M23.0677 11.9929L18.818 7.75739L17.4061 9.17398L19.2415 11.0032L0.932469 11.0012L0.932251 13.0012L19.2369 13.0032L17.4155 14.8308L18.8321 16.2426L23.0677 11.9929Z" fill="currentColor"/>
        </svg>
      </a>
    </div>
  </section>
  
  <!-- Gallery Preview Section -->
  <section class="w-full flex flex-col justify-evenly items-center py-6 sm:py-8 space-y-6 sm:space-y-8 px-4 sm:px-6">
    <h1 class="text-xl sm:text-2xl text-gray-500">Recent Creations</h1>
    <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-6 w-full gap-6 sm:gap-8 lg:gap-10">
      <div class="flex justify-center items-center">
        <img class="rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300" src="https://images.unsplash.com/photo-1602751584552-8ba73aad10e1?w=400&h=400&fit=crop" alt="Custom ring">
      </div>
      <div class="flex justify-center items-center">
        <img class="rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300" src="https://images.unsplash.com/photo-1535632066927-ab7c9ab60908?w=400&h=400&fit=crop" alt="Necklace">
      </div>
      <div class="hidden md:flex justify-center items-center">
        <img class="rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300" src="https://images.unsplash.com/photo-1611591437281-460bfbe1220a?w=400&h=400&fit=crop" alt="Earrings">
      </div>
      <div class="hidden md:flex justify-center items-center">
        <img class="rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300" src="https://images.unsplash.com/photo-1603561591411-07134e71a2a9?w=400&h=400&fit=crop" alt="Bracelet">
      </div>
      <div class="hidden md:flex justify-center items-center">
        <img class="rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300" src="https://images.unsplash.com/photo-1599643477877-530eb83abc8e?w=400&h=400&fit=crop" alt="Custom pendant">
      </div>
      <div class="hidden md:flex justify-center items-center">
        <img class="rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300" src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?w=400&h=400&fit=crop" alt="Wedding bands">
      </div>
    </div>
  </section>
  
  <section class="w-full flex flex-col py-12 sm:py-16 md:py-20 lg:py-24 space-y-6 sm:space-y-8 md:space-y-10 justify-center items-center px-4 sm:px-6">
    <h1 class="text-4xl sm:text-4xl md:text-5xl lg:text-6xl font-bold text-center leading-[1.1]">Jewelry as unique <br class="hidden sm:block"> as <b class="text-[#a855f7]">you are</b></h1>
    
    <p class="text-base sm:text-lg text-gray-700 text-center leading-[1.5] max-w-4xl">
      Every piece we create is a collaboration between your vision and our craftsmanship. 
      <br class="hidden md:block">From engagement rings to family heirlooms, we bring your dreams to life
      <br class="hidden md:block">with ethically sourced materials and meticulous attention to detail.
    </p>
    
    <div class="flex flex-col md:flex-row justify-center items-center gap-6 md:gap-8 w-full sm:w-[90%] md:w-[85%] lg:w-[78%]">
      <div class="bg-[#faf5ff] rounded-2xl px-6 sm:px-8 md:px-10 py-8 sm:py-10 md:py-12 space-y-4 w-full md:w-1/3 mb-6 md:mb-0">
        <img class="rounded-2xl w-full h-48 object-cover" src="https://images.unsplash.com/photo-1606800052052-a08af7148866?w=600&h=400&fit=crop" alt="Custom design process">
        <h2 class="text-xl sm:text-2xl font-bold text-center">Personalized Design <br> Process</h2>
        <p class="text-base sm:text-lg text-gray-700">Work one-on-one with our designers to create jewelry that perfectly captures your style and story.</p>
      </div>
      
      <div class="bg-[#faf5ff] rounded-2xl px-6 sm:px-8 md:px-10 py-8 sm:py-10 md:py-12 space-y-4 w-full md:w-1/3">
        <img class="rounded-2xl w-full h-48 object-cover" src="https://images.unsplash.com/photo-1617038260897-41a1f14a8ca0?w=600&h=400&fit=crop" alt="Master craftsmanship">
        <h2 class="text-xl sm:text-2xl font-bold text-center">Master <br> Craftsmanship</h2>
        <p class="text-base sm:text-lg text-gray-700">Our skilled artisans use traditional techniques combined with modern technology to create flawless pieces.</p>
      </div>
      
      <div class="bg-[#faf5ff] rounded-2xl px-6 sm:px-8 md:px-10 py-8 sm:py-10 md:py-12 space-y-4 w-full md:w-1/3">
        <img class="rounded-2xl w-full h-48 object-cover" src="https://images.unsplash.com/photo-1515562141207-7a88fb7ce338?w=600&h=400&fit=crop" alt="Lifetime warranty">
        <h2 class="text-xl sm:text-2xl font-bold text-center">Lifetime <br> Guarantee</h2>
        <p class="text-base sm:text-lg text-gray-700">Every piece comes with our lifetime warranty and free annual maintenance to keep it perfect forever.</p>
      </div>
    </div>
    
    <a href="/custom" class="mt-4 sm:mt-6 mb-3 sm:mb-5 rounded-xl w-fit px-8 sm:px-10 md:px-15 py-2 sm:py-3 bg-[#a855f7] text-bold text-xl sm:text-2xl flex justify-center items-center transition-all duration-100 hover:opacity-90 text-white shadow-lg">
      <p class="mr-2">Start Your Custom Design</p>
      <svg width="20" height="20" sm:width="22" sm:height="22" md:width="24" md:height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M23.0677 11.9929L18.818 7.75739L17.4061 9.17398L19.2415 11.0032L0.932469 11.0012L0.932251 13.0012L19.2369 13.0032L17.4155 14.8308L18.8321 16.2426L23.0677 11.9929Z" fill="currentColor"/>
      </svg>
    </a>
    
    <p class="text-lg sm:text-xl text-gray-700 text-center">
      Free consultation and 3D design preview 
      <br class="hidden sm:block"> before we begin crafting your piece.
    </p>
  </section>
  
  <!-- Promise Results Section -->
  <section class="w-screen flex justify-center items-center px-4 sm:px-6 py-8 sm:py-12">
    <div class="flex flex-col bg-[#e9d5ff] w-full sm:w-[90%] md:w-4/5 justify-evenly items-center py-8 sm:py-12 md:py-16 rounded-2xl">
      <div class="flex flex-col md:flex-row w-[90%] md:w-[85%] justify-center md:justify-evenly items-center px-4 sm:px-8 md:px-16 lg:px-36 space-y-6 md:space-y-0 md:space-x-4">
        <div class="w-40 md:w-auto">
          <svg class="w-full md:w-40" viewBox="0 0 100 100" fill="#a855f7">
            <path d="M50 20 L60 40 L80 40 L65 55 L70 75 L50 60 L30 75 L35 55 L20 40 L40 40 Z"/>
          </svg>
        </div>
        <div class="flex flex-col space-y-4 sm:space-y-6 text-center md:text-left">
          <h1 class="text-3xl md:text-4xl font-bold">100% Satisfaction Guaranteed!</h1>
          <p class="text-lg md:text-xl">If you're not completely in love with your custom piece, we'll redesign it until it's perfect.</p>
        </div>
      </div>
    </div>
  </section>
  <section class="w-screen flex flex-col justify-center items-center py-12 md:py-16 space-y-8 md:space-y-12">
    <h1 class="text-center font-bold text-4xl sm:text-5xl md:text-6xl leading-tight md:leading-[1.1] tracking-wide px-4">
      Why Choose <b class="text-[#a855f7]">Custom</b> <br class="hidden sm:block" /> Over Mass-Produced
    </h1>
    
    <p class="text-center text-gray-700 text-lg sm:text-xl mb-8 md:mb-12 px-4">Experience the difference of truly personalized jewelry:</p>
  
    <div class="flex flex-col space-y-12 md:space-y-16 w-[90%] md:w-[85%] lg:w-[75%]">
      {#each features as feature, i}
        <!-- Feature Row -->
        <div class="flex flex-col {i % 2 !== 0 ? 'md:flex-row-reverse' : 'md:flex-row'} items-center justify-between gap-8 md:gap-0">
          <!-- Text Content -->
          <div class="flex flex-col space-y-4 w-full md:w-1/2 {i % 2 !== 0 ? 'md:pl-10' : 'md:pr-10'}">
            <h2 class="text-2xl sm:text-3xl font-bold tracking-wide">{feature.title}</h2>
            <p class="text-lg sm:text-xl text-gray-700">{feature.description}</p>
            
            <!-- Benefits -->
            <div class="flex flex-col space-y-3 pt-4">
              {#each feature.benefits as benefit}
                <div class="flex space-x-3 items-center">
                  <div class="w-8 h-8 rounded-full bg-[#a855f7] flex items-center justify-center flex-shrink-0">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" viewBox="0 0 20 20" fill="currentColor">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                    </svg>
                  </div>
                  <p class="text-gray-700 text-base sm:text-lg">{benefit}</p>
                </div>
              {/each}
            </div>
          </div>
          
          <!-- Image -->
          <div class="w-full md:w-1/2 flex justify-center">
            <img class="rounded-2xl shadow-lg w-full md:h-80 object-cover" src={feature.image} alt={feature.title}>
          </div>
        </div>
      {/each}
    </div>
  
    <a href="/custom" class="mt-8 md:mt-16 rounded-xl w-fit px-8 sm:px-15 py-2 sm:py-3 bg-[#a855f7] text-bold text-xl sm:text-2xl flex justify-center items-center transition-all duration-100 hover:opacity-90 text-white shadow-lg"> 
      <p class="mr-2">Book Your Free Consultation</p>
      <svg
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        >
        <path
        d="M23.0677 11.9929L18.818 7.75739L17.4061 9.17398L19.2415 11.0032L0.932469 11.0012L0.932251 13.0012L19.2369 13.0032L17.4155 14.8308L18.8321 16.2426L23.0677 11.9929Z"
        fill="currentColor"
        />
      </svg>
    </a>
  </section>
  
  <section class="w-screen flex flex-col justify-center items-center py-12 md:py-20 bg-gray-50">
    <h1 class="text-center font-bold text-4xl sm:text-5xl md:text-6xl leading-tight md:leading-[1.1] tracking-wide mb-2 px-4">
      Why Choose <b class="text-[#a855f7]">Custom</b> <br/> Over Mass-Produced
    </h1>
    
    <svg class="w-[40%] sm:w-[30%] md:w-[20%] mb-4 sm:mb-8" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 300 20">
      <!-- The skinny subtle smile curve for an underline -->
      <path d="M 10,12 Q 150,6 290,12" stroke="#171717" stroke-width="1.5" fill="none" />
    </svg>
    
    <p class="text-center text-lg sm:text-xl text-gray-700 mb-8 md:mb-16 max-w-3xl px-4">
      See how our custom jewelry service creates meaningful pieces that last a lifetime, compared to generic store-bought options.
    </p>
    
    <!-- Mobile View (Accordion style) -->
    <div class="w-[90%] md:hidden flex flex-col space-y-4">
      <!-- Company Header (Mobile) -->
      <div class="flex w-full gap-2">
        <div class="w-1/2">
          <div class="bg-[#a855f7] rounded-t-xl w-full py-4 flex justify-center">
            <h2 class="text-white text-xl font-bold">Custom</h2>
          </div>
          <div class="bg-white p-4 rounded-b-xl shadow-md w-full flex justify-center items-center">
            <h3 class="text-xl font-bold text-gray-800">James's</h3>
          </div>
        </div>
        <div class="w-1/2">
          <div class="bg-gray-700 rounded-t-xl w-full py-4 flex justify-center">
            <h2 class="text-white text-xl font-bold">Mass</h2>
          </div>
          <div class="bg-white p-4 rounded-b-xl shadow-md w-full flex justify-center items-center">
            <h3 class="text-xl font-bold text-gray-800">Produced</h3>
          </div>
        </div>
      </div>
  
      <!-- Accordion Categories (Mobile) -->
      {#each collections as row, i}
        <details class="bg-white rounded-xl shadow-sm overflow-hidden">
          <summary class="bg-gray-100 p-4 font-bold text-gray-800 text-lg cursor-pointer">
            {row.category}
          </summary>
          <div class="p-4 flex flex-col space-y-6">
            <div class="border-b pb-4">
              <h4 class="font-semibold text-lg mb-3">Custom by James's</h4>
              {#each row.custom as point}
                <div class="flex items-start mb-3">
                  <div class="w-6 h-6 rounded-full bg-[#a855f7] flex items-center justify-center flex-shrink-0 mt-1">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-white" viewBox="0 0 20 20" fill="currentColor">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                    </svg>
                  </div>
                  <p class="text-gray-700 ml-3 text-base">{point}</p>
                </div>
              {/each}
              
              {#if row.hasRating}
                <div class="flex justify-center mt-4">
                  <div class="flex text-yellow-500">
                    {#each Array(5) as _, j}
                      <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    {/each}
                  </div>
                </div>
              {/if}
            </div>
  
            <div>
              <h4 class="font-semibold text-lg mb-3">Mass-Produced</h4>
              {#each row.readyMade as point}
                <div class="flex items-start mb-3">
                  <div class="w-6 h-6 rounded-full bg-red-100 flex items-center justify-center flex-shrink-0 mt-1">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-red-500" viewBox="0 0 20 20" fill="currentColor">
                      <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd" />
                    </svg>
                  </div>
                  <p class="text-gray-700 ml-3 text-base">{point}</p>
                </div>
              {/each}
              
              {#if row.hasRating}
                <div class="flex justify-center mt-4">
                  <div class="flex text-yellow-500">
                    {#each Array(3) as _, j}
                      <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    {/each}
                    {#each Array(2) as _, j}
                      <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-gray-300" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    {/each}
                  </div>
                </div>
              {/if}
            </div>
          </div>
        </details>
      {/each}
    </div>
    
    <!-- Desktop View (Table style) -->
    <div class="hidden md:block w-[90%] lg:w-4/5 flex flex-col">
      <!-- Table Header -->
      <div class="flex w-full mb-8">
        <div class="w-1/3"></div>
        <div class="w-1/3 flex flex-col items-center">
          <div class="bg-[#a855f7] rounded-t-xl w-full py-6 flex justify-center">
            <h2 class="text-white text-3xl font-bold">Custom Design</h2>
          </div>
          <div class="bg-white p-6 rounded-b-xl shadow-md w-full flex justify-center items-center">
            <h3 class="text-2xl font-bold text-gray-800">Ploe LuMena Jewels</h3>
          </div>
        </div>
        <div class="w-1/3 flex flex-col items-center">
          <div class="bg-gray-700 rounded-t-xl w-full py-6 flex justify-center">
            <h2 class="text-white text-3xl font-bold">Mass-Produced</h2>
          </div>
          <div class="bg-white p-6 rounded-b-xl shadow-md w-full flex justify-center items-center">
            <h3 class="text-2xl font-bold text-gray-800">Store-Bought</h3>
          </div>
        </div>
      </div>
      
      <!-- Comparison Rows -->
      <div class="flex flex-col space-y-8">
        {#each collections as row}
          <div class="flex w-full bg-white rounded-xl shadow-sm overflow-hidden">
            <div class="w-1/3 bg-gray-100 p-6 flex items-center">
              <h3 class="text-xl font-bold text-gray-800">{row.category}</h3>
            </div>
            <div class="w-1/3 p-6 border-r border-gray-200">
              {#each row.custom as point, i}
                <div class="flex items-start {i !== 0 ? 'mt-3' : ''}">
                  <div class="w-8 h-8 rounded-full bg-[#a855f7] flex items-center justify-center flex-shrink-0 mt-1">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white" viewBox="0 0 20 20" fill="currentColor">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                    </svg>
                  </div>
                  <p class="text-gray-700 ml-3">{point}</p>
                </div>
              {/each}
              
              {#if row.hasRating}
                <div class="flex justify-center mt-6">
                  <div class="flex text-yellow-500">
                    {#each Array(5) as _, i}
                      <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    {/each}
                  </div>
                </div>
              {/if}
            </div>
            <div class="w-1/3 p-6">
              {#each row.readyMade as point, i}
                <div class="flex items-start {i !== 0 ? 'mt-3' : ''}">
                  <div class="w-8 h-8 rounded-full bg-red-100 flex items-center justify-center flex-shrink-0 mt-1">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-red-500" viewBox="0 0 20 20" fill="currentColor">
                      <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd" />
                    </svg>
                  </div>
                  <p class="text-gray-700 ml-3">{point}</p>
                </div>
              {/each}
              
              {#if row.hasRating}
                <div class="flex justify-center mt-6">
                  <div class="flex text-yellow-500">
                    {#each Array(3) as _, i}
                      <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    {/each}
                    {#each Array(2) as _, i}
                      <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10 text-gray-300" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    {/each}
                  </div>
                </div>
              {/if}
            </div>
          </div>
        {/each}
      </div>
    </div>
  </section>
  
  <!-- Our Process Section -->
  <section class="flex flex-col w-screen justify-center items-center py-12 sm:py-16 md:py-20 px-4 sm:px-6">
    <h1 class="text-center text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-bold leading-[1.1] tracking-wide">Your Dream Piece in <b class="text-[#a855f7]">4 Simple Steps</b></h1>
    
    <svg class="w-[40%] sm:w-[30%] md:w-[20%] mb-4 sm:mb-6 md:mb-8" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 300 20">
      <!-- The skinny subtle smile curve for an underline -->
      <path d="M 10,12 Q 150,6 290,12" stroke="#171717" stroke-width="1.5" fill="none" />
    </svg>
    
    <p class="text-center mb-4 sm:mb-6 md:mb-8 text-base sm:text-lg">
      From initial consultation to the moment you wear your custom piece, 
      <br class="hidden md:block"> we make the process seamless and enjoyable.
    </p>
    
    <img class="w-full sm:w-[85%] md:w-[75%] rounded-2xl mb-4 sm:mb-6 md:mb-8 h-auto md:h-95" src="https://images.unsplash.com/photo-1506630448388-4e683c67ddb0?w=1200&h=600&fit=crop" alt="Jewelry crafting process">
    
    <div class="grid grid-cols-1 sm:grid-cols-2 w-full sm:w-[85%] md:w-[75%] gap-4 mb-4 sm:mb-6 md:mb-8">
      <div class="bg-[#faf5ff] rounded-xl p-4 sm:p-6 space-y-4 sm:space-y-6 md:space-y-8">
        <h1 class="text-2xl sm:text-3xl font-bold tracking-wide">1. Free Consultation</h1>
        <ol class="decoration space-y-4 sm:space-y-6 md:space-y-8">
          <li class="text-gray-700 text-base sm:text-lg"> 
            <b class="font-bold text-gray-700 text-lg sm:text-xl">- Share Your Vision:</b> 
            Meet with our designers to discuss your ideas, style preferences, and budget for your perfect piece.
          </li>
          <li class="text-gray-700 text-base sm:text-lg"> 
            <b class="font-bold text-gray-700 text-lg sm:text-xl">- Expert Guidance:</b> 
            Receive professional advice on stone selection, metal choices, and design possibilities.
          </li>
          <li class="text-gray-700 text-base sm:text-lg"> 
            <b class="font-bold text-gray-700 text-lg sm:text-xl">- Initial Sketches:</b> 
            Leave with preliminary design concepts and a clear quote for your custom jewelry.
          </li>
        </ol>
      </div>
      
      <div class="bg-[#faf5ff] rounded-xl p-4 sm:p-6 space-y-4 sm:space-y-6 md:space-y-8">
        <h1 class="text-2xl sm:text-3xl font-bold tracking-wide">2. Design & Approval</h1>
        <ol class="decoration space-y-4 sm:space-y-6 md:space-y-8">
          <li class="text-gray-700 text-base sm:text-lg"> 
            <b class="font-bold text-gray-700 text-lg sm:text-xl">- 3D Rendering:</b> 
            See your design come to life with detailed computer renderings before production begins.
          </li>
          <li class="text-gray-700 text-base sm:text-lg"> 
            <b class="font-bold text-gray-700 text-lg sm:text-xl">- Unlimited Revisions:</b> 
            Make as many changes as needed until the design is exactly what you envisioned.
          </li>
          <li class="text-gray-700 text-base sm:text-lg"> 
            <b class="font-bold text-gray-700 text-lg sm:text-xl">- Stone Selection:</b> 
            Choose from our ethically sourced diamonds and gemstones with expert guidance.
          </li>
        </ol>
      </div>
      
      <div class="bg-[#faf5ff] rounded-xl p-4 sm:p-6 space-y-4 sm:space-y-6 md:space-y-8">
        <h1 class="text-2xl sm:text-3xl font-bold tracking-wide">3. Expert Crafting</h1>
        <ol class="decoration space-y-4 sm:space-y-6 md:space-y-8">
          <li class="text-gray-700 text-base sm:text-lg"> 
            <b class="font-bold text-gray-700 text-lg sm:text-xl">- Master Artisans:</b> 
            Your piece is handcrafted by our experienced jewelers using time-honored techniques.
          </li>
          <li class="text-gray-700 text-base sm:text-lg"> 
            <b class="font-bold text-gray-700 text-lg sm:text-xl">- Quality Control:</b> 
            Every piece undergoes rigorous inspection to ensure it meets our exacting standards.
          </li>
          <li class="text-gray-700 text-base sm:text-lg"> 
            <b class="font-bold text-gray-700 text-lg sm:text-xl">- Progress Updates:</b> 
            Receive photos and updates throughout the creation process.
          </li>
          <div class="flex flex-wrap gap-1 items-center mt-4">
            <img class="rounded-full w-10 h-10 sm:w-12 sm:h-12 border border-[#a855f7] border-2" src="https://images.unsplash.com/photo-1560707303-4e980ce876ad?w=100&h=100&fit=crop" alt="">
            <img class="rounded-full w-10 h-10 sm:w-12 sm:h-12 border border-[#a855f7] border-2" src="https://images.unsplash.com/photo-1506634572416-48cdfe530110?w=100&h=100&fit=crop" alt="">
            <img class="rounded-full w-10 h-10 sm:w-12 sm:h-12 border border-[#a855f7] border-2" src="https://images.unsplash.com/photo-1543295553-3e0b0aa39e65?w=100&h=100&fit=crop" alt="">
            <img class="rounded-full w-10 h-10 sm:w-12 sm:h-12 border border-[#a855f7] border-2" src="https://images.unsplash.com/photo-1625948515291-69613efd103f?w=100&h=100&fit=crop" alt="">
            <p class="text-[#a855f7] ml-2 sm:ml-6 text-xl sm:text-2xl md:text-3xl">Our artisans at work!</p>
          </div>
        </ol>
      </div>
      
      <div class="bg-[#faf5ff] rounded-xl p-4 sm:p-6 space-y-4 sm:space-y-6 md:space-y-8">
        <h1 class="text-2xl sm:text-3xl font-bold tracking-wide text-center">4. The Perfect Reveal</h1>
        <h2 class="text-[#a855f7] text-center text-5xl sm:text-7xl md:text-9xl">✨</h2>
        <p class="text-gray-700 text-base sm:text-lg text-center">Experience the joy of seeing your custom piece for the first time in our private viewing room. We'll ensure perfect fit and complete satisfaction before you take your treasure home.</p>
      </div>
    </div>
  </section>
   <!-- Testimonials Section -->
  <section class="flex flex-col w-screen justify-center items-center space-y-8 sm:space-y-10 md:space-y-12 py-10 sm:py-12 md:py-16 bg-gray-50 px-4 sm:px-6">
    <h1 class="font-bold text-3xl sm:text-4xl md:text-5xl lg:text-6xl text-center tracking-wide leading-[1.1] text-gray-900">
      Love Stories From <b class="text-[#a855f7]">Our Clients</b>
    </h1>
    
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 grid-rows-auto w-full sm:w-[90%] lg:w-[75%] gap-4 sm:gap-6 overflow-hidden">
      <!-- Image 1 -->
      <div class="hidden md:block relative group overflow-hidden h-60 sm:h-72 md:h-80 rounded-xl">
        <img class="rounded-xl w-full h-full object-cover transition-transform duration-300 group-hover:scale-105" 
             src="https://images.unsplash.com/photo-1617038220319-276d3cfab638?w=600&h=400&fit=crop" alt="Custom engagement ring">
      </div>
      
      <!-- Image 2 -->
      <div class="hidden md:block relative group overflow-hidden h-60 sm:h-72 md:h-80 rounded-xl">
        <img class="rounded-xl w-full h-full object-cover transition-transform duration-300 group-hover:scale-105" 
             src="https://images.unsplash.com/photo-1602173574767-37ac01994b2a?w=600&h=400&fit=crop" alt="Wedding bands">
      </div>
      
      <!-- Image 3 -->
      <div class="hidden md:block relative group overflow-hidden h-60 sm:h-72 md:h-80 rounded-xl">
        <img class="rounded-xl w-full h-full object-cover transition-transform duration-300 group-hover:scale-105" 
             src="https://images.unsplash.com/photo-1598560917505-59a3ad559071?w=600&h=400&fit=crop" alt="Custom necklace">
      </div>
      
      <!-- Review Card 1 -->
      <div class="flex flex-col p-4 sm:p-6 md:p-7 rounded-xl border border-gray-300 hover:border-gray-500 shadow-sm hover:shadow-md transition-all duration-300 h-fit space-y-3 sm:space-y-5 bg-white">
        <div class="flex justify-between h-fit">
          <div class="flex space-x-3 sm:space-x-4 text-gray-700 text-base sm:text-lg md:text-xl items-center">
            <img class="rounded-full w-10 h-10 sm:w-12 sm:h-12 object-cover shadow" src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?w=100&h=100&fit=crop" alt="">
            <div class="flex flex-col">
              <p class="font-medium">Emily R.</p>
              <p class="text-gray-500 text-sm sm:text-base">Engagement Ring</p>
            </div>
          </div>
          <div class="flex flex-col items-end">
            <div class="flex text-yellow-500">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
            </div>
            <p class="text-gray-500 text-sm sm:text-base">Jan 2025</p>
          </div>
        </div>
        <h1 class="font-bold text-gray-800 text-lg sm:text-xl">Beyond My Dreams!</h1>
        <p class="text-gray-700 text-base sm:text-lg md:text-xl">"James created the most stunning ring. He understood exactly what I envisioned and made it even better!"</p>
      </div>
      
      <!-- Review Card 2 -->
      <div class="flex flex-col p-4 sm:p-6 md:p-7 rounded-xl border border-gray-300 hover:border-gray-500 shadow-sm hover:shadow-md transition-all duration-300 h-fit space-y-3 sm:space-y-5 bg-white">
        <div class="flex justify-between h-fit">
          <div class="flex space-x-3 sm:space-x-4 text-gray-700 text-base sm:text-lg md:text-xl items-center">
            <img class="rounded-full w-10 h-10 sm:w-12 sm:h-12 object-cover shadow" src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=100&h=100&fit=crop" alt="">
            <div class="flex flex-col">
              <p class="font-medium">Michael & Anna</p>
              <p class="text-gray-500 text-sm sm:text-base">Wedding Bands</p>
            </div>
          </div>
          <div class="flex flex-col items-end">
            <div class="flex text-yellow-500">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
            </div>
            <p class="text-gray-500 text-sm sm:text-base">Dec 2024</p>
          </div>
        </div>
        <h1 class="font-bold text-gray-800 text-lg sm:text-xl">Perfect Matching Set</h1>
        <p class="text-gray-700 text-base sm:text-lg md:text-xl">"Our wedding bands perfectly complement my engagement ring. The attention to detail is incredible!"</p>
      </div>
      
      <!-- Review Card 3 -->
      <div class="flex flex-col p-4 sm:p-6 md:p-7 rounded-xl border border-gray-300 hover:border-gray-500 shadow-sm hover:shadow-md transition-all duration-300 h-fit space-y-3 sm:space-y-5 bg-white">
        <div class="flex justify-between h-fit">
          <div class="flex space-x-3 sm:space-x-4 text-gray-700 text-base sm:text-lg md:text-xl items-center">
            <img class="rounded-full w-10 h-10 sm:w-12 sm:h-12 object-cover shadow" src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?w=100&h=100&fit=crop" alt="">
            <div class="flex flex-col">
              <p class="font-medium">Sarah L.</p>
              <p class="text-gray-500 text-sm sm:text-base">Anniversary Gift</p>
            </div>
          </div>
          <div class="flex flex-col items-end">
            <div class="flex text-yellow-500">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 sm:h-5 sm:w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
            </div>
            <p class="text-gray-500 text-sm sm:text-base">Nov 2024</p>
          </div>
        </div>
        <h1 class="font-bold text-gray-800 text-lg sm:text-xl">Heirloom Transformed</h1>
        <p class="text-gray-700 text-base sm:text-lg md:text-xl">"They transformed my grandmother's diamonds into a modern necklace that I wear every day. So meaningful!"</p>
      </div>
    </div>
  </section>
  
  <section class="flex flex-col w-screen justify-center items-center space-y-8 py-16 bg-gray-50">
    <h1 class="text-4xl sm:text-5xl md:text-6xl font-bold text-center leading-tight sm:leading-[1.1]">
      Meet Our Master <br class="hidden sm:block" /> Jewelers
    </h1>
    <p class="text-lg sm:text-xl text-center text-gray-700 px-4 sm:px-0">The talented artisans who bring your dreams to life</p>
    
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 grid-rows-1 w-[90%] lg:w-[75%] gap-4 sm:gap-6 overflow-hidden">
      {#each teamMembers as member, i}
        <!-- Team Member Card -->
        <div class="relative group overflow-hidden h-96 sm:h-110 md:h-130 rounded-xl">
          <img 
            class="w-full h-full object-cover transition-all duration-300 brightness-60 md:brightness-100 md:group-hover:scale-105 md:group-hover:brightness-50" 
            src={member.image} 
            alt={member.name}
          />
          <!-- Overlay content that appears on hover -->
          <div class="absolute inset-0 flex flex-col md:items-center justify-end md:justify-center opacity-100 md:opacity-0 md:group-hover:opacity-100 transition-opacity duration-300 px-4 sm:px-6 text-left md:text-center py-4 md:py-0">
            <h3 class="text-white text-xl sm:text-2xl font-bold mb-1 sm:mb-2">{member.name}</h3>
            <p class="text-white text-base sm:text-lg font-medium mb-2 sm:mb-4">{member.title}</p>
            <p class="text-white text-sm sm:text-base">{member.bio}</p>
          </div>
        </div>
      {/each}
    </div>
  </section>
  <div class="w-full flex flex-col items-center mt-16 space-y-6">
              <h2 class="text-3xl font-bold text-center">Still Have Questions?</h2>
              <p class="text-xl text-gray-700 text-center max-w-3xl">Our team is ready to answer any questions you might have about implementing LineGo's parking solutions at your property.</p>
              <a href="/contact" class="rounded-xl w-fit px-20 py-3 bg-[#a855f7] text-bold text-2xl md:text-3xl flex justify-center items-center transition-all duration-100 hover:opacity-90 text-white shadow shadow-[#a855f7]">
                <p class="mr-2">Contact Us Today</p>
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M23.0677 11.9929L18.818 7.75739L17.4061 9.17398L19.2415 11.0032L0.932469 11.0012L0.932251 13.0012L19.2369 13.0032L17.4155 14.8308L18.8321 16.2426L23.0677 11.9929Z" fill="currentColor"/>
                </svg>
              </a>
            </div>
            <footer class="w-screen bg-[#a855f7] text-white mt-24">
            <!-- Top Section with Columns -->
            <div class="w-full max-w-7xl mx-auto px-4 sm:px-6 py-12 sm:py-16 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8 sm:gap-12">
              <!-- Column 1: About -->
              <div class="flex flex-col space-y-6">
                <img src="heard.svg" alt="LineGo Parking" class="h-10 sm:h-24 mb-2 max-w-[200px]">
                <p class="text-white text-opacity-90 text-base sm:text-lg">LineGo is revolutionizing parking enforcement with our non-predatory, resident-first approach. We're committed to creating fair parking environments for properties that care.</p>
                <div class="flex space-x-4">
                  <a href="https://facebook.com" class="text-white hover:text-white hover:opacity-80 transition-opacity">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                      <path d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z"/>
                    </svg>
                  </a>
                  <a href="https://twitter.com" class="text-white hover:text-white hover:opacity-80 transition-opacity">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                      <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/>
                    </svg>
                  </a>
                  <a href="https://instagram.com" class="text-white hover:text-white hover:opacity-80 transition-opacity">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                      <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                    </svg>
                  </a>
                  <a href="https://linkedin.com" class="text-white hover:text-white hover:opacity-80 transition-opacity">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                      <path d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z"/>
                    </svg>
                  </a>
                </div>
              </div>
          
              <!-- Column 2: Quick Links -->
              <div class="flex flex-col space-y-4">
                <h3 class="text-lg sm:text-xl font-bold mb-2">Quick Links</h3>
                <a href="/" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">Home</a>
                <a href="/about" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">About Us</a>
                <a href="/services" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">Our Services</a>
                <a href="/testimonials" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">Testimonials</a>
                <a href="/blog" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">Blog</a>
                <a href="/careers" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">Careers</a>
                <a href="/contact" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">Contact Us</a>
              </div>
          
              <!-- Column 3: Services -->
              <div class="flex flex-col space-y-4">
                <h3 class="text-lg sm:text-xl font-bold mb-2">Our Services</h3>
                <a href="/services/enforcement" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">Parking Enforcement</a>
                <a href="/services/permits" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">Digital Permits</a>
                <a href="/services/technology" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">Parking Technology</a>
                <a href="/services/signage" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">Signage Solutions</a>
                <a href="/services/consulting" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">Parking Consulting</a>
                <a href="/services/towing" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-base sm:text-lg">Towing Services</a>
              </div>
          
              <!-- Column 4: Contact -->
              <div class="flex flex-col space-y-4">
                <h3 class="text-lg sm:text-xl font-bold mb-2">Contact Us</h3>
                <p class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-2 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                  </svg>
                  <span class="text-white text-opacity-90 text-base sm:text-lg">5804 Fairchase Ave.<br>Charlotte, NC 28269</span>
                </p>
                <p class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-2 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                  </svg>
                  <span class="text-white text-opacity-90 text-base sm:text-lg">(704) 309-6194</span>
                </p>
                <p class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-2 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                  </svg>
                  <span class="text-white text-opacity-90 text-base sm:text-lg">James@ploe.com</span>
                </p>
                <div class="pt-4">
                  <h4 class="text-base sm:text-lg font-semibold mb-3">Operating Hours</h4>
                  <p class="text-white text-opacity-90 text-base sm:text-lg">Monday - Friday: 8:00 AM - 8:00 PM</p>
                  <p class="text-white text-opacity-90 text-base sm:text-lg">24/7 Customer Support Available</p>
                </div>
              </div>
            </div>
          
            <!-- Bottom Section with Copyright -->
            <div class="w-full bg-[#a855f7] py-6">
              <div class="max-w-7xl mx-auto px-4 sm:px-6 flex flex-col md:flex-row justify-between items-center">
                <p class="text-white text-opacity-90 text-center md:text-left mb-4 md:mb-0 text-sm sm:text-base">© 2025 LineGo Parking. All rights reserved.</p>
                <div class="flex flex-wrap justify-center gap-4 sm:gap-6">
                  <a href="/privacy" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-sm sm:text-base">Privacy Policy</a>
                  <a href="/terms" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-sm sm:text-base">Terms of Service</a>
                  <a href="/sitemap" class="text-white text-opacity-90 hover:text-opacity-100 transition-opacity text-sm sm:text-base">Sitemap</a>
                </div>
              </div>
            </div>
          </footer>
  </section>