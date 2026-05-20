
<!doctype html>
<html lang="id" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jajan Yuk - Es &amp; Cemilan</title>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script src="https://cdn.jsdelivr.net/npm/lucide@0.263.0/dist/umd/lucide.min.js"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&amp;display=swap" rel="stylesheet">
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: { poppins: ['Poppins', 'sans-serif'] },
          colors: {
            sky: { light: '#e0f7fa', mid: '#4dd0e1', dark: '#00acc1' },
            mint: '#a8e6cf',
            pastel: { yellow: '#fff9c4', pink: '#fce4ec' }
          }
        }
      }
    }
  </script>
  <style>
    html, body { height: 100%; margin: 0; }
    * { font-family: 'Poppins', sans-serif; }
    .fade-in { opacity: 0; transform: translateY(30px); transition: opacity 0.7s ease, transform 0.7s ease; }
    .fade-in.visible { opacity: 1; transform: translateY(0); }
    .card-hover { transition: transform 0.3s ease, box-shadow 0.3s ease; }
    .card-hover:hover { transform: translateY(-8px); box-shadow: 0 20px 40px rgba(0,0,0,0.1); }
    .nav-link { position: relative; }
    .nav-link::after { content:''; position:absolute; bottom:-2px; left:0; width:0; height:2px; background:#00acc1; transition: width 0.3s; }
    .nav-link:hover::after { width:100%; }
    .hero-bg { background: linear-gradient(135deg, #e0f7fa 0%, #a8e6cf 50%, #fff9c4 100%); }
    .blob { border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%; animation: morph 8s ease-in-out infinite; }
    @keyframes morph { 0%,100%{ border-radius:30% 70% 70% 30%/30% 30% 70% 70%; } 50%{ border-radius:70% 30% 30% 70%/70% 70% 30% 30%; } }
    @keyframes float { 0%,100%{ transform:translateY(0); } 50%{ transform:translateY(-10px); } }
    .float-anim { animation: float 3s ease-in-out infinite; }
    .menu-badge { background: linear-gradient(135deg, #4dd0e1, #00acc1); }
  </style>
  <style>body { box-sizing: border-box; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full overflow-auto bg-white"><!-- Navbar -->
  <nav id="navbar" class="fixed top-0 left-0 w-full z-50 bg-white/90 backdrop-blur-md shadow-sm transition-all duration-300">
   <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex items-center justify-between h-16"><a href="#beranda" class="flex items-center gap-2"> <span class="text-2xl">🧊</span> <span class="text-xl sm:text-2xl font-extrabold bg-gradient-to-r from-cyan-500 to-teal-400 bg-clip-text text-transparent">Jajan Yuk</span> </a>
    <div class="hidden md:flex items-center gap-6"><a href="#beranda" class="nav-link text-sm font-medium text-gray-700 hover:text-cyan-600">Beranda</a> <a href="#menu" class="nav-link text-sm font-medium text-gray-700 hover:text-cyan-600">Menu</a> <a href="#tentang" class="nav-link text-sm font-medium text-gray-700 hover:text-cyan-600">Tentang</a> <a href="#kontak" class="nav-link text-sm font-medium text-gray-700 hover:text-cyan-600">Kontak</a> <a href="https://wa.me/6283164196704" target="_blank" rel="noopener noreferrer" class="px-4 py-2 bg-gradient-to-r from-cyan-500 to-teal-400 text-white text-sm font-semibold rounded-full hover:shadow-lg transition">Pesan</a>
    </div><button id="mobileMenuBtn" class="md:hidden p-2 rounded-lg hover:bg-gray-100"> <i data-lucide="menu" class="w-6 h-6 text-gray-700"></i> </button>
   </div>
   <div id="mobileMenu" class="hidden md:hidden bg-white border-t px-4 pb-4"><a href="#beranda" class="block py-2 text-gray-700 font-medium">Beranda</a> <a href="#menu" class="block py-2 text-gray-700 font-medium">Menu</a> <a href="#tentang" class="block py-2 text-gray-700 font-medium">Tentang</a> <a href="#kontak" class="block py-2 text-gray-700 font-medium">Kontak</a> <a href="https://wa.me/6283164196704" target="_blank" rel="noopener noreferrer" class="block mt-2 text-center py-2 bg-cyan-500 text-white rounded-full font-semibold">Pesan Sekarang</a>
   </div>
  </nav><!-- Hero Section -->
  <section id="beranda" class="hero-bg pt-24 pb-16 px-4 sm:px-6 lg:px-8 relative overflow-hidden">
   <div class="absolute top-10 right-10 w-32 h-32 bg-yellow-200/50 blob hidden lg:block"></div>
   <div class="absolute bottom-10 left-10 w-24 h-24 bg-cyan-200/50 blob hidden lg:block" style="animation-delay:-4s"></div>
   <div class="max-w-7xl mx-auto flex flex-col lg:flex-row items-center gap-10">
    <div class="flex-1 text-center lg:text-left"><span class="inline-block px-4 py-1 bg-white/70 rounded-full text-sm font-medium text-cyan-700 mb-4">🎉 Buka Setiap Hari</span>
     <h1 id="heroTitle" class="text-3xl sm:text-4xl lg:text-5xl font-black text-gray-800 leading-tight mb-4">Segarnya Nikmat,<br>
      Cemilannya Mantap!</h1>
     <p id="heroSubtitle" class="text-base sm:text-lg text-gray-600 mb-8 max-w-lg mx-auto lg:mx-0">Tempat favorit minuman dan jajanan enak dengan harga ramah di kantong.</p>
     <div class="flex flex-col sm:flex-row gap-3 justify-center lg:justify-start"><a href="#menu" class="px-6 py-3 bg-gradient-to-r from-cyan-500 to-teal-400 text-white font-semibold rounded-full shadow-lg hover:shadow-xl hover:scale-105 transition-all text-center">🍹 Lihat Menu</a> <a href="https://wa.me/6283164196704?text=Halo,%20saya%20mau%20pesan!" target="_blank" rel="noopener noreferrer" class="px-6 py-3 bg-white text-cyan-600 font-semibold rounded-full shadow-md hover:shadow-lg hover:scale-105 transition-all border border-cyan-200 text-center">📱 Pesan Sekarang</a>
     </div>
    </div>
    <div class="flex-1 flex justify-center">
     <div class="relative float-anim">
      <div class="w-64 h-64 sm:w-80 sm:h-80 rounded-full bg-gradient-to-br from-cyan-100 to-mint flex items-center justify-center shadow-2xl"><span class="text-8xl sm:text-9xl">🥤</span>
      </div><span class="absolute top-4 right-4 text-4xl animate-bounce">🍩</span> <span class="absolute bottom-8 left-0 text-3xl" style="animation: float 2.5s ease-in-out infinite; animation-delay:-1s">🧁</span>
     </div>
    </div>
   </div>
  </section><!-- Menu Minuman -->
  <section id="menu" class="py-16 px-4 sm:px-6 lg:px-8 bg-white">
   <div class="max-w-7xl mx-auto">
    <div class="text-center mb-12 fade-in"><span class="inline-block px-4 py-1 menu-badge text-white text-sm font-semibold rounded-full mb-3">🍹 MENU MINUMAN</span>
     <h2 class="text-2xl sm:text-3xl font-bold text-gray-800">Minuman Segar Pilihan</h2>
     <p class="text-gray-500 mt-2">Dingin, manis, dan bikin nagih!</p>
    </div>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6" id="drinkGrid"></div>
   </div>
  </section><!-- Menu Cemilan -->
  <section class="py-16 px-4 sm:px-6 lg:px-8 bg-gradient-to-b from-yellow-50 to-white">
   <div class="max-w-7xl mx-auto">
    <div class="text-center mb-12 fade-in"><span class="inline-block px-4 py-1 bg-yellow-400 text-white text-sm font-semibold rounded-full mb-3">🍟 MENU CEMILAN</span>
     <h2 class="text-2xl sm:text-3xl font-bold text-gray-800">Cemilan Favorit</h2>
     <p class="text-gray-500 mt-2">Gurih, renyah, dan bikin ketagihan!</p>
    </div>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6" id="snackGrid"></div>
   </div>
  </section><!-- Tentang -->
  <section id="tentang" class="py-16 px-4 sm:px-6 lg:px-8 bg-white">
   <div class="max-w-4xl mx-auto text-center fade-in"><span class="text-5xl mb-4 inline-block">🏪</span>
    <h2 class="text-2xl sm:text-3xl font-bold text-gray-800 mb-6">Tentang Kami</h2>
    <p id="aboutText" class="text-gray-600 text-base sm:text-lg leading-relaxed max-w-2xl mx-auto">Jajan Yuk adalah warung minuman dan cemilan yang menyediakan berbagai menu segar dan lezat dengan harga terjangkau. Cocok untuk nongkrong bersama teman dan keluarga.</p>
    <div class="flex flex-wrap justify-center gap-8 mt-10">
     <div class="text-center">
      <span class="text-3xl block mb-1">💰</span><span class="text-sm text-gray-600 font-medium">Harga Ramah</span>
     </div>
     <div class="text-center">
      <span class="text-3xl block mb-1">🧊</span><span class="text-sm text-gray-600 font-medium">Segar Setiap Hari</span>
     </div>
     <div class="text-center">
      <span class="text-3xl block mb-1">👨‍👩‍👧‍👦</span><span class="text-sm text-gray-600 font-medium">Ramah Keluarga</span>
     </div>
     <div class="text-center">
      <span class="text-3xl block mb-1">📦</span><span class="text-sm text-gray-600 font-medium">Terima Pesanan</span>
     </div>
    </div>
   </div>
  </section><!-- Kontak -->
  <section id="kontak" class="py-16 px-4 sm:px-6 lg:px-8 bg-gradient-to-br from-cyan-50 to-mint/30">
   <div class="max-w-4xl mx-auto fade-in">
    <div class="text-center mb-10">
     <h2 class="text-2xl sm:text-3xl font-bold text-gray-800">Hubungi Kami</h2>
     <p class="text-gray-500 mt-2">Menerima pesanan untuk acara dan kebutuhan lainnya.</p>
    </div>
    <div class="grid sm:grid-cols-2 gap-6">
     <div class="bg-white rounded-2xl p-6 shadow-md">
      <div class="flex items-start gap-4">
       <div class="w-12 h-12 bg-cyan-100 rounded-xl flex items-center justify-center shrink-0">
        <i data-lucide="map-pin" class="w-5 h-5 text-cyan-600"></i>
       </div>
       <div>
        <h3 class="font-semibold text-gray-800">Alamat</h3>
        <p id="contactAddress" class="text-gray-500 text-sm mt-1">Desa Nunggal Sari Jalur 12</p>
       </div>
      </div>
     </div>
     <div class="bg-white rounded-2xl p-6 shadow-md">
      <div class="flex items-start gap-4">
       <div class="w-12 h-12 bg-green-100 rounded-xl flex items-center justify-center shrink-0">
        <i data-lucide="phone" class="w-5 h-5 text-green-600"></i>
       </div>
       <div>
        <h3 class="font-semibold text-gray-800">WhatsApp</h3>
        <p id="contactWa" class="text-gray-500 text-sm mt-1">0831-6419-6704</p><a href="https://wa.me/6283164196704" target="_blank" rel="noopener noreferrer" class="inline-block mt-2 text-xs font-semibold text-white bg-green-500 px-3 py-1 rounded-full hover:bg-green-600 transition">Chat Sekarang</a>
       </div>
      </div>
     </div>
    </div>
   </div>
  </section><!-- Footer -->
  <footer class="bg-gray-900 text-white py-10 px-4">
   <div class="max-w-7xl mx-auto text-center"><span class="text-2xl font-bold bg-gradient-to-r from-cyan-400 to-teal-300 bg-clip-text text-transparent">Jajan Yuk</span>
    <p class="text-gray-400 text-sm mt-3">Terima kasih sudah mampir ke Jajan Yuk! 💛</p>
    <div class="flex justify-center gap-4 mt-4"><a href="#" class="w-9 h-9 bg-gray-800 rounded-full flex items-center justify-center hover:bg-cyan-600 transition"><i data-lucide="instagram" class="w-4 h-4"></i></a> <a href="#" class="w-9 h-9 bg-gray-800 rounded-full flex items-center justify-center hover:bg-cyan-600 transition"><i data-lucide="facebook" class="w-4 h-4"></i></a> <a href="https://wa.me/6283164196704" target="_blank" rel="noopener noreferrer" class="w-9 h-9 bg-gray-800 rounded-full flex items-center justify-center hover:bg-green-600 transition"><i data-lucide="phone" class="w-4 h-4"></i></a>
    </div>
    <p class="text-gray-500 text-xs mt-6">© 2024 Jajan Yuk. All rights reserved.</p>
   </div>
  </footer>
  <script>
    // Data
    const drinks = [
      { name: 'Es Teler', price: 'Rp10.000', emoji: '🍨', color: 'from-green-100 to-emerald-50' },
      { name: 'Es Teh Hijau', price: 'Rp5.000', emoji: '🍵', color: 'from-green-50 to-lime-50' },
      { name: 'Es Kecebong', price: 'Rp5.000', emoji: '🧋', color: 'from-amber-50 to-yellow-50' },
      { name: 'Es Kacang Merah', price: 'Rp5.000', emoji: '🫘', color: 'from-red-50 to-pink-50' },
      { name: 'Es Ubi Ungu', price: 'Rp6.000', emoji: '🍠', color: 'from-purple-50 to-violet-50' },
      { name: 'Es Josu', price: 'Rp5.000', emoji: '🥛', color: 'from-blue-50 to-cyan-50' },
      { name: 'Es Kusu', price: 'Rp5.000', emoji: '🍶', color: 'from-orange-50 to-amber-50' },
      { name: 'Es Jeruk Nipis', price: 'Rp5.000', emoji: '🍋', color: 'from-lime-50 to-green-50' },
      { name: 'Es Milkshake', price: 'Rp10.000', emoji: '🥤', color: 'from-pink-50 to-rose-50' },
    ];

    const snacks = [
      { name: 'Risol Sayur', emoji: '🥟', color: 'from-green-50 to-emerald-50' },
      { name: 'Risol Mayo', emoji: '🥙', color: 'from-yellow-50 to-amber-50' },
      { name: 'Risol Ayam', emoji: '🍗', color: 'from-orange-50 to-amber-50' },
      { name: 'Aneka Makanan Tradisional', emoji: '🍱', color: 'from-red-50 to-rose-50' },
      { name: 'Aneka Gorengan', emoji: '🍟', color: 'from-amber-50 to-yellow-50' },
      { name: 'Seblak', emoji: '🌶️', color: 'from-red-100 to-orange-50' },
    ];

    // Render cards
    const drinkGrid = document.getElementById('drinkGrid');
    drinks.forEach(d => {
      drinkGrid.innerHTML += `
        <div class="card-hover fade-in bg-gradient-to-br ${d.color} rounded-2xl p-5 border border-gray-100 shadow-sm">
          <div class="text-5xl mb-3">${d.emoji}</div>
          <h3 class="font-semibold text-gray-800 text-lg">${d.name}</h3>
          <p class="text-cyan-600 font-bold text-lg mt-1">${d.price}</p>
          <a href="https://wa.me/6283164196704?text=Halo,%20saya%20mau%20pesan%20${encodeURIComponent(d.name)}" target="_blank" rel="noopener noreferrer" class="inline-block mt-3 px-4 py-2 bg-gradient-to-r from-cyan-500 to-teal-400 text-white text-sm font-semibold rounded-full hover:shadow-md transition">Pesan</a>
        </div>`;
    });

    const snackGrid = document.getElementById('snackGrid');
    snacks.forEach(s => {
      snackGrid.innerHTML += `
        <div class="card-hover fade-in bg-gradient-to-br ${s.color} rounded-2xl p-5 border border-gray-100 shadow-sm">
          <div class="text-5xl mb-3">${s.emoji}</div>
          <h3 class="font-semibold text-gray-800 text-lg">${s.name}</h3>
          <a href="https://wa.me/6283164196704?text=Halo,%20saya%20mau%20pesan%20${encodeURIComponent(s.name)}" target="_blank" rel="noopener noreferrer" class="inline-block mt-3 px-4 py-2 bg-gradient-to-r from-yellow-400 to-orange-400 text-white text-sm font-semibold rounded-full hover:shadow-md transition">Pesan</a>
        </div>`;
    });

    // Mobile menu
    document.getElementById('mobileMenuBtn').addEventListener('click', () => {
      document.getElementById('mobileMenu').classList.toggle('hidden');
    });
    document.querySelectorAll('#mobileMenu a').forEach(a => a.addEventListener('click', () => document.getElementById('mobileMenu').classList.add('hidden')));

    // Scroll fade-in
    const observer = new IntersectionObserver(entries => {
      entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
    }, { threshold: 0.1 });
    document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

    // Lucide icons
    lucide.createIcons();

    // Element SDK
    const defaultConfig = {
      hero_title: 'Segarnya Nikmat, Cemilannya Mantap!',
      hero_subtitle: 'Tempat favorit minuman dan jajanan enak dengan harga ramah di kantong.',
      about_text: 'Jajan Yuk adalah warung minuman dan cemilan yang menyediakan berbagai menu segar dan lezat dengan harga terjangkau. Cocok untuk nongkrong bersama teman dan keluarga.',
      contact_address: 'Desa Nunggal Sari Jalur 12',
      whatsapp_number: '0831-6419-6704',
      background_color: '#ffffff',
      surface_color: '#e0f7fa',
      text_color: '#1f2937',
      primary_action: '#00acc1',
      secondary_action: '#f59e0b',
      font_family: 'Poppins',
      font_size: 16
    };

    function applyConfig(config) {
      const c = { ...defaultConfig, ...config };
      document.getElementById('heroTitle').innerHTML = c.hero_title.replace(',', ',<br>');
      document.getElementById('heroSubtitle').textContent = c.hero_subtitle;
      document.getElementById('aboutText').textContent = c.about_text;
      document.getElementById('contactAddress').textContent = c.contact_address;
      document.getElementById('contactWa').textContent = c.whatsapp_number;
      document.body.style.fontFamily = `${c.font_family}, Poppins, sans-serif`;
      document.body.style.fontSize = c.font_size + 'px';
    }

    window.elementSdk.init({
      defaultConfig,
      onConfigChange: async (config) => applyConfig(config),
      mapToCapabilities: (config) => ({
        recolorables: [
          { get: () => config.background_color || defaultConfig.background_color, set: v => { config.background_color = v; window.elementSdk.setConfig({ background_color: v }); } },
          { get: () => config.surface_color || defaultConfig.surface_color, set: v => { config.surface_color = v; window.elementSdk.setConfig({ surface_color: v }); } },
          { get: () => config.text_color || defaultConfig.text_color, set: v => { config.text_color = v; window.elementSdk.setConfig({ text_color: v }); } },
          { get: () => config.primary_action || defaultConfig.primary_action, set: v => { config.primary_action = v; window.elementSdk.setConfig({ primary_action: v }); } },
          { get: () => config.secondary_action || defaultConfig.secondary_action, set: v => { config.secondary_action = v; window.elementSdk.setConfig({ secondary_action: v }); } },
        ],
        borderables: [],
        fontEditable: { get: () => config.font_family || defaultConfig.font_family, set: v => { config.font_family = v; window.elementSdk.setConfig({ font_family: v }); } },
        fontSizeable: { get: () => config.font_size || defaultConfig.font_size, set: v => { config.font_size = v; window.elementSdk.setConfig({ font_size: v }); } }
      }),
      mapToEditPanelValues: (config) => new Map([
        ['hero_title', config.hero_title || defaultConfig.hero_title],
        ['hero_subtitle', config.hero_subtitle || defaultConfig.hero_subtitle],
        ['about_text', config.about_text || defaultConfig.about_text],
        ['contact_address', config.contact_address || defaultConfig.contact_address],
        ['whatsapp_number', config.whatsapp_number || defaultConfig.whatsapp_number],
      ])
    });
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9fef0709c3f5e78f',t:'MTc3OTMxODc2MC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
