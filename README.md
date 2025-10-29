<!doctype html>
<html lang="id" x-data="{ dark: false, menu: false }" :class="{ 'dark': dark }">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Menu Sederhana</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script defer src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"></script>
</head>
<body class="bg-gray-50 dark:bg-gray-900 text-gray-800 dark:text-gray-100 min-h-screen">
  <nav class="flex justify-between items-center p-4 shadow bg-white dark:bg-gray-800">
    <div class="font-bold text-lg text-indigo-600">MyMenu</div>

    <!-- Menu desktop -->
    <ul class="hidden md:flex space-x-4">
      <li><a href="#" class="hover:text-indigo-600">Beranda</a></li>
      <li><a href="#" class="hover:text-indigo-600">Layanan</a></li>
      <li><a href="#" class="hover:text-indigo-600">Portfolio</a></li>
      <li><a href="#" class="hover:text-indigo-600">Kontak</a></li>
    </ul>

    <!-- Tombol kanan -->
    <div class="flex items-center space-x-2">
      <button @click="dark=!dark" class="px-3 py-1 border rounded-md text-sm">Mode</button>
      <button @click="menu=!menu" class="md:hidden px-3 py-1 border rounded-md text-sm">Menu</button>
    </div>
  </nav>

  <!-- Menu mobile -->
  <div x-show="menu" x-transition class="md:hidden p-4 bg-white dark:bg-gray-800 shadow">
    <a href="#" class="block py-1">Beranda</a>
    <a href="#" class="block py-1">Layanan</a>
    <a href="#" class="block py-1">Portfolio</a>
    <a href="#" class="block py-1">Kontak</a>
  </div>

  <main class="p-6 text-center">
    <h1 class="text-3xl font-bold mb-2">Menu Laravel Sederhana</h1>
    <p class="text-gray-600 dark:text-gray-300">Contoh menu responsif dan mudah disesuaikan.</p>
  </main>
</body>
</html>
