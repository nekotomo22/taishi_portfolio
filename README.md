<!DOCTYPE html>
<html lang="ja">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>泰嗣 -Taishi- | Video & Graphic Portfolio</title>

  <!-- Google Fonts -->
  <link
    href="https://fonts.googleapis.com/css2?family=Montserrat:wght@700;900&family=Noto+Sans+JP:wght@300;500;700&display=swap"
    rel="stylesheet">
  <script src="https://cdn.tailwindcss.com"></script>

  <style>
    :root {
      --bg-color: #050505;
      --accent-color: #ffffff;
      --text-gray: #a0a0a0;
    }

    body {
      background-color: var(--bg-color);
      color: var(--accent-color);
      font-family: 'Noto Sans JP', 'Montserrat', sans-serif;
      overflow-x: hidden;
    }

    .reveal {
      opacity: 0;
      transform: translateY(30px);
      transition: all 1.2s cubic-bezier(0.22, 1, 0.36, 1);
    }

    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }

    .hero-title {
      font-size: clamp(3.5rem, 12vw, 10rem);
      line-height: 0.85;
      letter-spacing: -0.05em;
    }

    ::-webkit-scrollbar {
      width: 6px;
    }

    ::-webkit-scrollbar-track {
      background: #000;
    }

    ::-webkit-scrollbar-thumb {
      background: #333;
      border-radius: 10px;
    }

    .work-card img {
      transition: transform 0.8s cubic-bezier(0.22, 1, 0.36, 1);
    }

    .work-card:hover img {
      transform: scale(1.05);
    }

    .overlay {
      background: linear-gradient(0deg, rgba(0, 0, 0, 0.9) 0%, rgba(0, 0, 0, 0.2) 50%, rgba(0, 0, 0, 0) 100%);
      opacity: 0;
      transition: opacity 0.4s;
    }

    .work-card:hover .overlay {
      opacity: 1;
    }

    .skill-card {
      border-bottom: 1px solid #1a1a1a;
      transition: border-color 0.4s;
    }

    .skill-card:hover {
      border-color: #ffffff;
    }

    .no-scrollbar::-webkit-scrollbar {
      display: none;
    }

    .no-scrollbar {
      -ms-overflow-style: none;
      scrollbar-width: none;
    }

    @keyframes swipe-indicator {
      0%, 100% { transform: translateX(0); }
      50% { transform: translateX(5px); }
    }
    .animate-swipe-indicator {
      animation: swipe-indicator 1.5s ease-in-out infinite;
    }
  </style>
</head>

<body>

  <!-- Navigation -->
  <nav class="fixed top-0 w-full z-50 px-8 py-6 flex justify-between items-center mix-blend-difference">
    <div class="text-xl font-black tracking-tighter uppercase text-white">Taishi</div>
    <div class="space-x-8 text-xs uppercase tracking-widest hidden md:flex font-bold text-white">
      <a href="#work" class="hover:text-gray-400 transition">Work</a>
      <a href="#service" class="hover:text-gray-400 transition">Service</a>
    </div>
  </nav>

  <!-- Hero Section -->
  <header class="h-[80vh] flex flex-col justify-center px-8 md:px-20 border-b border-zinc-900">
    <h1 class="hero-title font-black uppercase reveal">Video &<br>Graphic</h1>
    <p class="mt-8 text-zinc-500 tracking-[0.3em] uppercase text-sm font-bold reveal">Production Portfolio 2026</p>
  </header>

  <!-- Work -->
  <section id="work" class="py-32 px-8 md:px-20 bg-zinc-950">
    <div class="flex justify-between items-end mb-20 reveal">
      <div>
        <h2 class="text-xs tracking-[0.5em] text-zinc-500 uppercase mb-4 font-bold">Portfolio</h2>
        <h3 class="text-5xl font-black tracking-tighter">SELECTED WORKS</h3>
      </div>
      <p class="text-zinc-500 text-sm hidden md:block uppercase tracking-widest italic">
        Web Design, TV Graphics & Video Production
      </p>
    </div>

    <!-- Webサイト制作 セクション -->
    <div class="mb-24">
      <div class="flex justify-between items-end mb-8 reveal">
        <h4 class="text-2xl font-bold border-l-4 border-white pl-4 tracking-wider">Webサイト制作</h4>
        <div class="md:hidden flex items-center gap-2 px-3 py-1 rounded-full bg-white/5 border border-white/10 backdrop-blur-md">
          <span class="text-[9px] tracking-[0.2em] text-zinc-300 font-bold uppercase ml-1">Swipe</span>
          <svg class="w-3 h-3 text-white animate-swipe-indicator" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
          </svg>
        </div>
      </div>

      <div class="flex md:grid md:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8 overflow-x-auto snap-x snap-mandatory no-scrollbar pb-8 -mx-8 px-8 md:mx-0 md:px-0">
        <!-- Work Card 1 -->
        <a href="https://nekotomo22.github.io/rikitokuakira_officialsite/" target="_blank" rel="noopener noreferrer"
          class="work-card block relative aspect-video overflow-hidden bg-zinc-900 reveal group flex-none w-[80vw] md:w-auto snap-center">
          <img src="./img/website001.jpeg" alt="力徳明 オフィシャルサイト" class="w-full h-full object-cover"
            onerror="this.src='https://placehold.co/800x450/1a1a1a/ffffff?text=Actor+Official+Site'">
          <div class="overlay absolute inset-0 flex flex-col justify-end p-8">
            <span class="text-xs uppercase tracking-[0.2em] mb-2 text-zinc-400">Web Site</span>
            <h3 class="text-xl font-bold">力徳明 オフィシャルサイト</h3>
          </div>
        </a>

        <!-- Work Card 2 -->
        <a href="https://nekotomo22.github.io/asoorganiccafe/" target="_blank" rel="noopener noreferrer"
          class="work-card block relative aspect-video overflow-hidden bg-zinc-900 reveal group flex-none w-[80vw] md:w-auto snap-center">
          <img src="./img/website002.jpeg" alt="ASO ORGANIC CAFE" class="w-full h-full object-cover"
            onerror="this.src='https://placehold.co/800x450/1a1a1a/ffffff?text=Cafe+Web+Site'">
          <div class="overlay absolute inset-0 flex flex-col justify-end p-8">
            <span class="text-xs uppercase tracking-[0.2em] mb-2 text-zinc-400">Web Site</span>
            <h3 class="text-xl font-bold">ASO ORGANIC CAFE</h3>
          </div>
        </a>
      </div>
    </div>

    <!-- グラフィックデザイン セクション -->
    <div class="mb-24">
      <div class="flex justify-between items-end mb-8 reveal">
        <h4 class="text-2xl font-bold border-l-4 border-white pl-4 tracking-wider">グラフィックデザイン</h4>
        <div class="md:hidden flex items-center gap-2 px-3 py-1 rounded-full bg-white/5 border border-white/10 backdrop-blur-md">
          <span class="text-[9px] tracking-[0.2em] text-zinc-300 font-bold uppercase ml-1">Swipe</span>
          <svg class="w-3 h-3 text-white animate-swipe-indicator" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
          </svg>
        </div>
      </div>

      <div class="flex md:grid md:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8 overflow-x-auto snap-x snap-mandatory no-scrollbar pb-8 -mx-8 px-8 md:mx-0 md:px-0">
        <!-- Graphic Card 1 -->
        <div class="work-card relative aspect-video overflow-hidden bg-zinc-900 reveal group flex-none w-[80vw] md:w-auto snap-center">
          <img src="./img/graphic001.jpeg" alt="エンタメ特集ビジュアル" class="w-full h-full object-cover"
            onerror="this.src='https://placehold.co/800x450/1a1a1a/ffffff?text=Work+01'">
          <div class="overlay absolute inset-0 flex flex-col justify-end p-8">
            <span class="text-xs uppercase tracking-[0.2em] mb-2 text-zinc-400">TV Graphic</span>
            <h3 class="text-xl font-bold">エンタメ特集ビジュアル</h3>
          </div>
        </div>
        <!-- Graphic Card 2 -->
        <div class="work-card relative aspect-video overflow-hidden bg-zinc-900 reveal group flex-none w-[80vw] md:w-auto snap-center">
          <img src="./img/graphic002.jpeg" alt="エンタメ特集ビジュアル" class="w-full h-full object-cover"
            onerror="this.src='https://placehold.co/800x450/1a1a1a/ffffff?text=Work+02'">
          <div class="overlay absolute inset-0 flex flex-col justify-end p-8">
            <span class="text-xs uppercase tracking-[0.2em] mb-2 text-zinc-400">TV Graphic</span>
            <h3 class="text-xl font-bold">エンタメ特集ビジュアル</h3>
          </div>
        </div>
        <!-- Graphic Card 3 -->
        <div class="work-card relative aspect-video overflow-hidden bg-zinc-900 reveal group flex-none w-[80vw] md:w-auto snap-center">
          <img src="./img/graphic003.jpeg" alt="データ解説・報道グラフ" class="w-full h-full object-cover"
            onerror="this.src='https://placehold.co/800x450/1a1a1a/ffffff?text=Work+03'">
          <div class="overlay absolute inset-0 flex flex-col justify-end p-8">
            <span class="text-xs uppercase tracking-[0.2em] mb-2 text-zinc-400">Information</span>
            <h3 class="text-xl font-bold">データ解説・報道グラフ</h3>
          </div>
        </div>
        <!-- Graphic Card 4 -->
        <div class="work-card relative aspect-video overflow-hidden bg-zinc-900 reveal group flex-none w-[80vw] md:w-auto snap-center">
          <img src="./img/graphic004.jpeg" alt="エンタメ特集ビジュアル" class="w-full h-full object-cover"
            onerror="this.src='https://placehold.co/800x450/1a1a1a/ffffff?text=Work+04'">
          <div class="overlay absolute inset-0 flex flex-col justify-end p-8">
            <span class="text-xs uppercase tracking-[0.2em] mb-2 text-zinc-400">News</span>
            <h3 class="text-xl font-bold">エンタメ特集ビジュアル</h3>
          </div>
        </div>
        <!-- Graphic Card 5 -->
        <div class="work-card relative aspect-video overflow-hidden bg-zinc-900 reveal group flex-none w-[80vw] md:w-auto snap-center">
          <img src="./img/graphic005.jpeg" alt="スポーツグラフィック" class="w-full h-full object-cover"
            onerror="this.src='https://placehold.co/800x450/1a1a1a/ffffff?text=Work+05'">
          <div class="overlay absolute inset-0 flex flex-col justify-end p-8">
            <span class="text-xs uppercase tracking-[0.2em] mb-2 text-zinc-400">Sports</span>
            <h3 class="text-xl font-bold">スポーツグラフィック</h3>
          </div>
        </div>
        <!-- Graphic Card 6 -->
        <div class="work-card relative aspect-video overflow-hidden bg-zinc-900 reveal group flex-none w-[80vw] md:w-auto snap-center">
          <img src="./img/graphic006.jpeg" alt="エンタメ特集ビジュアル" class="w-full h-full object-cover"
            onerror="this.src='https://placehold.co/800x450/1a1a1a/ffffff?text=Work+06'">
          <div class="overlay absolute inset-0 flex flex-col justify-end p-8">
            <span class="text-xs uppercase tracking-[0.2em] mb-2 text-zinc-400">Entertainment</span>
            <h3 class="text-xl font-bold">エンタメ特集ビジュアル</h3>
          </div>
        </div>
      </div>
    </div>

    <!-- 動画制作 セクション -->
    <div>
      <div class="flex justify-between items-end mb-8 reveal">
        <h4 class="text-2xl font-bold border-l-4 border-white pl-4 tracking-wider">動画制作</h4>
      </div>
      <div class="flex md:grid md:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8 overflow-x-auto snap-x snap-mandatory no-scrollbar pb-8 -mx-8 px-8 md:mx-0 md:px-0">
        <div class="relative aspect-video overflow-hidden bg-zinc-900 reveal flex-none w-[80vw] md:w-auto snap-center shadow-lg">
          <iframe class="w-full h-full absolute inset-0"
            src="https://www.youtube.com/embed/BE1S05eVIYU?si=qK-iiBn6_9GyEjIz" title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            referrerpolicy="strict-origin-when-cross-origin" allowfullscreen>
          </iframe>
        </div>
      </div>
    </div>
  </section>

  <!-- Service & Skills -->
  <section id="service" class="py-32 px-8 md:px-20 bg-zinc-950/50">
    <div class="max-w-6xl mx-auto">
      <div class="mb-20 reveal">
        <h2 class="text-xs tracking-[0.5em] text-zinc-500 uppercase mb-4 font-bold">Expertise</h2>
        <h3 class="text-5xl font-black tracking-tighter">SERVICE</h3>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-12 gap-y-2">
        <div class="skill-card py-6 flex items-center justify-between reveal">
          <span class="text-zinc-600 text-[10px] font-bold mr-4 italic">01</span>
          <span class="text-lg font-bold tracking-tight flex-1">動画編集</span>
        </div>
        <div class="skill-card py-6 flex items-center justify-between reveal">
          <span class="text-zinc-600 text-[10px] font-bold mr-4 italic">02</span>
          <span class="text-lg font-bold tracking-tight flex-1">アー写撮影</span>
        </div>
        <div class="skill-card py-6 flex items-center justify-between reveal">
          <span class="text-zinc-600 text-[10px] font-bold mr-4 italic">03</span>
          <span class="text-lg font-bold tracking-tight flex-1">MV撮影</span>
        </div>
        <div class="skill-card py-6 flex items-center justify-between reveal">
          <span class="text-zinc-600 text-[10px] font-bold mr-4 italic">04</span>
          <span class="text-lg font-bold tracking-tight flex-1">PR動画制作</span>
        </div>
        <div class="skill-card py-6 flex items-center justify-between reveal">
          <span class="text-zinc-600 text-[10px] font-bold mr-4 italic">05</span>
          <span class="text-lg font-bold tracking-tight flex-1">AIツール活用</span>
        </div>
        <div class="skill-card py-6 flex items-center justify-between reveal">
          <span class="text-zinc-600 text-[10px] font-bold mr-4 italic">06</span>
          <span class="text-lg font-bold tracking-tight flex-1">WEBサイト制作</span>
        </div>
        <div class="skill-card py-6 flex items-center justify-between reveal">
          <span class="text-zinc-600 text-[10px] font-bold mr-4 italic">07</span>
          <span class="text-lg font-bold tracking-tight flex-1">企画・提案</span>
        </div>
        <div class="skill-card py-6 flex items-center justify-between reveal">
          <span class="text-zinc-600 text-[10px] font-bold mr-4 italic">08</span>
          <span class="text-lg font-bold tracking-tight flex-1">フライヤー制作</span>
        </div>
        <div class="skill-card py-6 flex items-center justify-between reveal">
          <span class="text-zinc-600 text-[10px] font-bold mr-4 italic">09</span>
          <span class="text-lg font-bold tracking-tight flex-1">ショートドラマ制作</span>
        </div>
      </div>

      <!-- Tools -->
      <div class="mt-32 reveal">
        <h2 class="text-xs tracking-[0.5em] text-zinc-500 uppercase mb-8 font-bold">Tools</h2>
        <div class="flex flex-wrap gap-x-12 gap-y-6 text-2xl md:text-5xl font-black tracking-tighter opacity-80 italic">
          <span>Photoshop</span>
          <span>Illustrator</span>
          <span>Premiere Pro</span>
          <span>DaVinci Resolve</span>
          <span>CapCut</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer (Simplified) -->
  <footer class="py-20 px-8 md:px-20 border-t border-zinc-900 text-center">
    <p class="text-zinc-700 text-[10px] tracking-[0.5em] uppercase font-bold">
      &copy; 2026 TAISHI. ALL RIGHTS RESERVED.
    </p>
  </footer>

  <script>
    function reveal() {
      document.querySelectorAll(".reveal").forEach(el => {
        const top = el.getBoundingClientRect().top;
        if (top < window.innerHeight - 100) {
          el.classList.add("active");
        }
      });
    }
    window.addEventListener("scroll", reveal);
    window.addEventListener("load", reveal);
    setTimeout(reveal, 500);
  </script>

</body>

</html>
