<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Avioturs Travel Service | Travel Agency</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    body { font-family: 'Plus Jakarta Sans', sans-serif; }
    .card-hidden { display: none !important; }
  </style>
</head>
<body class="bg-slate-50 text-slate-800">

  <nav class="sticky top-0 z-50 bg-white/90 backdrop-blur-md border-b border-slate-100 shadow-sm">
    <div class="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between">
      <div class="flex items-center gap-2">
        <span class="text-2xl font-extrabold tracking-tight text-blue-900" data-key="brand_name">AVIOTURS</span>
        <span class="text-xs font-semibold px-2 py-0.5 bg-blue-100 text-blue-700 rounded-full" data-key="badge">TRAVEL</span>
      </div>
      
      <div class="hidden md:flex items-center gap-8 font-medium text-slate-600">
        <a href="#destinations" class="hover:text-blue-600 transition" data-key="nav_dest">Destinations</a>
        <a href="#services" class="hover:text-blue-600 transition" data-key="nav_serv">Services</a>
        <a href="#about" class="hover:text-blue-600 transition" data-key="nav_about">About Us</a>
        <a href="#contact" class="hover:text-blue-600 transition" data-key="nav_contact">Contact</a>
      </div>

      <div class="flex items-center gap-3">
        <select id="langSelect" class="bg-slate-100 border border-slate-300 rounded-full px-3 py-1.5 text-xs font-bold text-slate-700 focus:outline-none focus:ring-2 focus:ring-blue-500 cursor-pointer">
          <option value="en">🌐 EN</option>
          <option value="mk">🌐 MK</option>
          <option value="sq">🌐 SQ</option>
          <option value="de">🌐 DE</option>
        </select>

        <a href="tel:+38923137000" class="bg-blue-600 hover:bg-blue-700 text-white font-semibold px-4 py-2 text-sm md:px-5 md:py-2.5 rounded-full transition shadow-md shadow-blue-500/20" data-key="nav_btn">
          Book a Flight
        </a>
      </div>
    </div>
  </nav>

  <header class="relative bg-slate-900 text-white min-h-[480px] flex items-center">
    <div class="absolute inset-0 overflow-hidden">
      <img src="https://images.unsplash.com/photo-1488085061387-422e29b40080?q=80&w=1920&auto=format&fit=crop" class="w-full h-full object-cover opacity-30" alt="Travel background">
      <div class="absolute inset-0 bg-gradient-to-r from-slate-950/90 via-slate-950/50 to-transparent"></div>
    </div>

    <div class="relative max-w-7xl mx-auto px-6 py-16 w-full">
      <div class="max-w-2xl space-y-4">
        <span class="inline-block px-3 py-1 bg-white/10 backdrop-blur-md border border-white/20 text-xs font-semibold text-blue-200 rounded-full" data-key="hero_badge">
          Established 1986 • IATA Certified
        </span>
        <h1 class="text-4xl sm:text-6xl font-extrabold tracking-tight leading-tight" data-key="hero_title">
          Explore The World.
        </h1>
        <p class="text-lg text-slate-300" data-key="hero_sub">
          Over 20+ international destinations, flight reservations, and custom holiday arrangements.
        </p>
      </div>
    </div>
  </header>

  <section id="destinations" class="py-16 max-w-7xl mx-auto px-6">
    
    <div class="flex flex-col md:flex-row md:items-end justify-between gap-6 mb-10">
      <div>
        <h2 class="text-3xl font-bold tracking-tight" data-key="grid_title">Featured Destinations</h2>
        <p class="text-slate-500 mt-1" data-key="grid_sub">Browse our selection of travel arrangements worldwide.</p>
      </div>

      <div class="w-full md:w-80">
        <input type="text" id="searchInput" placeholder="Search destination..." class="w-full bg-white border border-slate-200 rounded-xl px-4 py-2.5 text-sm font-medium focus:outline-blue-500 shadow-sm">
      </div>
    </div>

    <div class="flex items-center gap-2 overflow-x-auto pb-4 mb-8 border-b border-slate-200">
      <button class="filter-btn active bg-blue-600 text-white px-5 py-2 rounded-full text-sm font-bold transition shadow-sm" data-category="all" data-key="tab_all">All Offers</button>
      <button class="filter-btn bg-white text-slate-600 border border-slate-200 hover:bg-slate-100 px-5 py-2 rounded-full text-sm font-medium transition" data-category="beach" data-key="tab_beach">Beach & Coast</button>
      <button class="filter-btn bg-white text-slate-600 border border-slate-200 hover:bg-slate-100 px-5 py-2 rounded-full text-sm font-medium transition" data-category="winter" data-key="tab_winter">Winter Ski</button>
      <button class="filter-btn bg-white text-slate-600 border border-slate-200 hover:bg-slate-100 px-5 py-2 rounded-full text-sm font-medium transition" data-category="cities" data-key="tab_cities">City Tours</button>
      <button class="filter-btn bg-white text-slate-600 border border-slate-200 hover:bg-slate-100 px-5 py-2 rounded-full text-sm font-medium transition" data-category="exotic" data-key="tab_exotic">Exotic</button>
    </div>

    <div id="destGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">

      <div class="dest-card group bg-white rounded-2xl overflow-hidden shadow-sm hover:shadow-xl transition-all border border-slate-100" data-category="beach" data-name="greece">
        <div class="relative h-48 overflow-hidden">
          <img src="https://images.unsplash.com/photo-1533105079780-92b9be482077?q=80&w=600&auto=format&fit=crop" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" alt="Greece">
          <span class="absolute top-3 right-3 bg-white/90 backdrop-blur-md px-2.5 py-0.5 text-xs font-bold rounded-full text-slate-800" data-key="tag_beach">Beach</span>
        </div>
        <div class="p-5">
          <h3 class="text-lg font-bold mb-1" data-key="c1_title">Greece Beach Resorts</h3>
          <p class="text-slate-500 text-xs mb-3" data-key="c1_desc">Halkidiki, Islands & Beachfront Hotels.</p>
          <span class="text-blue-600 font-bold text-xs" data-key="c_more">View Details →</span>
        </div>
      </div>

      <div class="dest-card group bg-white rounded-2xl overflow-hidden shadow-sm hover:shadow-xl transition-all border border-slate-100" data-category="cities" data-name="italy rome milan">
        <div class="relative h-48 overflow-hidden">
          <img src="https://images.unsplash.com/photo-1516483638261-f4dbaf036963?q=80&w=600&auto=format&fit=crop" class="w-full h-full object-cover group-hover:scale-105 transition duration-500" alt="Italy">
          <span class="absolute top-3 right-3 bg-white/90 backdrop-blur-md px-2.5 py-0.5 text-xs font-bold rounded-full text-slate-800" data-key="tag_cities">City Break</span>
        </div>
        <div class="p-5">
          <h3 class="tex
