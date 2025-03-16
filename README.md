<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chrono Resort - Four Eras in One Destination</title>
<script src="https://cdn.tailwindcss.com"></script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Playfair+Display:wght@400;500;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/remixicon@4.5.0/fonts/remixicon.css" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/echarts/5.5.0/echarts.min.js"></script>
<script>tailwind.config={theme:{extend:{colors:{primary:'#8B5E3C',secondary:'#2A5A4B'},borderRadius:{'none':'0px','sm':'2px',DEFAULT:'4px','md':'8px','lg':'12px','xl':'16px','2xl':'20px','3xl':'24px','full':'9999px','button':'4px'}}}}</script>
<style>
:where([class^="ri-"])::before { content: "\f3c2"; }
.date-input::-webkit-calendar-picker-indicator {
background: transparent;
bottom: 0;
color: transparent;
cursor: pointer;
height: auto;
left: 0;
position: absolute;
right: 0;
top: 0;
width: auto;
}
.custom-scroll::-webkit-scrollbar {
width: 6px;
height: 6px;
}
.custom-scroll::-webkit-scrollbar-track {
background: #f1f1f1;
border-radius: 3px;
}
.custom-scroll::-webkit-scrollbar-thumb {
background: #888;
border-radius: 3px;
}
.custom-scroll::-webkit-scrollbar-thumb:hover {
background: #555;
}
.theme-card::before {
content: '';
position: absolute;
top: 0;
left: 0;
right: 0;
bottom: 0;
background: linear-gradient(to bottom, rgba(0,0,0,0) 50%, rgba(0,0,0,0.7) 100%);
border-radius: 16px;
z-index: 1;
}
@keyframes float {
0% { transform: translateY(0px); }
50% { transform: translateY(-10px); }
100% { transform: translateY(0px); }
}
.float-animation {
animation: float 3s ease-in-out infinite;
}
</style>
</head>
<body class="font-['Inter'] bg-white">
<nav class="fixed top-0 left-0 right-0 bg-white shadow-sm z-50">
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="flex justify-between items-center h-16">
<div class="flex items-center">
<a href="/" class="font-['Pacifico'] text-2xl text-primary">Chrono Resort</a>
<div class="hidden md:flex items-center space-x-8 ml-10">
<a href="#" class="text-gray-700 hover:text-primary">Home</a>
<a href="#" class="text-gray-700 hover:text-primary">Themes</a>
<a href="#" class="text-gray-700 hover:text-primary">Rooms</a>
<a href="#" class="text-gray-700 hover:text-primary">Activities</a>
<a href="#" class="text-gray-700 hover:text-primary">Contact</a>
</div>
</div>
<div class="flex items-center space-x-4">
<div class="relative" id="languageSelector">
<button class="flex items-center space-x-2 text-gray-700 hover:text-primary cursor-pointer">
<i class="ri-global-line text-lg"></i>
<span>EN</span>
<i class="ri-arrow-down-s-line"></i>
</button>
<div class="hidden absolute top-full right-0 mt-2 w-48 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5">
<div class="py-1">
<a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">English</a>
<a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Español</a>
<a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Français</a>
</div>
</div>
</div>
<button class="bg-primary text-white px-6 py-2 !rounded-button hover:bg-opacity-90 transition-all whitespace-nowrap cursor-pointer">
Book Now
</button>
</div>
</div>
</div>
</nav>
<main class="pt-16">
<section class="relative h-[600px] bg-cover bg-center" style="background-image: url('https://public.readdy.ai/ai/img_res/61d6bae9edf7d8274c89b53f730eb30e.jpg')">
<div class="absolute inset-0 bg-black bg-opacity-40"></div>
<div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-full flex items-center">
<div class="max-w-2xl text-white">
<h1 class="text-5xl font-['Playfair_Display'] font-bold mb-6">Four Eras in One Destination</h1>
<p class="text-xl mb-8">Time travel through eras while relaxing.</p>
<button class="bg-primary text-white px-8 py-3 !rounded-button hover:bg-opacity-90 transition-all text-lg whitespace-nowrap cursor-pointer">
Start Your Journey
</button>
</div>
<div class="absolute right-8 top-1/2 -translate-y-1/2 bg-white rounded-lg p-6 shadow-xl w-96">
<h3 class="text-xl font-semibold mb-4">Book Your Stay</h3>
<form id="bookingForm" class="space-y-4">
<div>
<label class="block text-sm font-medium text-gray-700 mb-1">Check-in</label>
<div class="relative">
<input type="date" class="w-full border border-gray-300 rounded-md px-4 py-2 date-input" min="2025-03-16">
<i class="ri-calendar-line absolute right-3 top-1/2 -translate-y-1/2 text-gray-400"></i>
</div>
</div>
<div>
<label class="block text-sm font-medium text-gray-700 mb-1">Check-out</label>
<div class="relative">
<input type="date" class="w-full border border-gray-300 rounded-md px-4 py-2 date-input" min="2025-03-17">
<i class="ri-calendar-line absolute right-3 top-1/2 -translate-y-1/2 text-gray-400"></i>
</div>
</div>
<div>
<label class="block text-sm font-medium text-gray-700 mb-1">Guests</label>
<div class="relative">
<select class="w-full border border-gray-300 rounded-md px-4 py-2 appearance-none pr-8">
<option>1 Guest</option>
<option>2 Guests</option>
<option>3 Guests</option>
<option>4 Guests</option>
</select>
<i class="ri-arrow-down-s-line absolute right-3 top-1/2 -translate-y-1/2 text-gray-400"></i>
</div>
</div>
<div>
<label class="block text-sm font-medium text-gray-700 mb-1">Theme</label>
<div class="relative">
<select class="w-full border border-gray-300 rounded-md px-4 py-2 appearance-none pr-8">
<option>Medieval Era</option>
<option>Green Environment</option>
<option>Modern Era</option>
<option>Advanced Era</option>
</select>
<i class="ri-arrow-down-s-line absolute right-3 top-1/2 -translate-y-1/2 text-gray-400"></i>
</div>
</div>
<button type="submit" class="w-full bg-primary text-white py-3 !rounded-button hover:bg-opacity-90 transition-all whitespace-nowrap cursor-pointer">
Check Availability
</button>
</form>
</div>
</div>
</section>
<section class="py-20 bg-gray-50">
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="text-center mb-16">
<h2 class="text-4xl font-['Playfair_Display'] font-bold mb-4">Our Unique Themes</h2>
<p class="text-gray-600 max-w-2xl mx-auto">Choose your preferred era and immerse yourself in a carefully crafted experience that combines historical authenticity with modern comfort.</p>
</div>
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
<div class="theme-card relative rounded-lg overflow-hidden cursor-pointer group">
<img src="https://public.readdy.ai/ai/img_res/106e45e60fcd161933276907a1e1b9a8.jpg" class="w-full h-96 object-cover transition-transform duration-300 group-hover:scale-110" alt="Medieval Era">
<div class="absolute bottom-0 left-0 right-0 p-6 text-white z-10">
<h3 class="text-xl font-bold mb-2">Medieval Era</h3>
<p class="text-sm mb-4">Step back into the age of knights and castles</p>
<span class="text-sm bg-white bg-opacity-20 px-3 py-1 rounded-full">10 Rooms Available</span>
</div>
</div>
<div class="theme-card relative rounded-lg overflow-hidden cursor-pointer group">
<img src="https://public.readdy.ai/ai/img_res/d1e92a2b9f91e32f2afac02c6796385d.jpg" class="w-full h-96 object-cover transition-transform duration-300 group-hover:scale-110" alt="Green Environment">
<div class="absolute bottom-0 left-0 right-0 p-6 text-white z-10">
<h3 class="text-xl font-bold mb-2">Green Environment</h3>
<p class="text-sm mb-4">Embrace sustainable luxury in harmony with nature</p>
<span class="text-sm bg-white bg-opacity-20 px-3 py-1 rounded-full">10 Rooms Available</span>
</div>
</div>
<div class="theme-card relative rounded-lg overflow-hidden cursor-pointer group">
<img src="https://public.readdy.ai/ai/img_res/87e20d84fa52ab9618074143b8fee933.jpg" class="w-full h-96 object-cover transition-transform duration-300 group-hover:scale-110" alt="Modern Era">
<div class="absolute bottom-0 left-0 right-0 p-6 text-white z-10">
<h3 class="text-xl font-bold mb-2">Modern Era</h3>
<p class="text-sm mb-4">Experience contemporary luxury at its finest</p>
<span class="text-sm bg-white bg-opacity-20 px-3 py-1 rounded-full">10 Rooms Available</span>
</div>
</div>
<div class="theme-card relative rounded-lg overflow-hidden cursor-pointer group">
<img src="https://public.readdy.ai/ai/img_res/f0f8f51a157a29d2c92e62447ab648f1.jpg" class="w-full h-96 object-cover transition-transform duration-300 group-hover:scale-110" alt="Advanced Era">
<div class="absolute bottom-0 left-0 right-0 p-6 text-white z-10">
<h3 class="text-xl font-bold mb-2">Advanced Era</h3>
<p class="text-sm mb-4">Step into the future of hospitality</p>
<span class="text-sm bg-white bg-opacity-20 px-3 py-1 rounded-full">10 Rooms Available</span>
</div>
</div>
</div>
</div>
</section>
<section class="py-20">
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="text-center mb-16">
<h2 class="text-4xl font-['Playfair_Display'] font-bold mb-4">Exclusive Activities</h2>
<p class="text-gray-600 max-w-2xl mx-auto">Discover our curated selection of theme-specific and common activities designed to enhance your stay.</p>
</div>
<div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-16">
<div>
<h3 class="text-2xl font-['Playfair_Display'] font-bold mb-6">Theme-Exclusive Activities</h3>
<div class="space-y-4">
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Knight Training</h4>
<p class="text-gray-600">Learn medieval combat techniques and chivalry</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full">
<i class="ri-sword-line text-primary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Archery Lessons</h4>
<p class="text-gray-600">Master the art of medieval archery</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full">
<i class="ri-arrow-right-line text-primary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Yoga Classes</h4>
<p class="text-gray-600">Connect with nature through mindful movement</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full">
<i class="ri-mental-health-line text-primary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Meditation in Nature</h4>
<p class="text-gray-600">Find peace in our natural surroundings</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full">
<i class="ri-sun-line text-primary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Cocktail Party Lessons</h4>
<p class="text-gray-600">Learn the art of modern mixology</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full">
<i class="ri-goblet-line text-primary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Virtual Reality Tours</h4>
<p class="text-gray-600">Explore immersive digital worlds</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full">
<i class="ri-virtual-reality-line text-primary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Interactive Tech Exhibitions</h4>
<p class="text-gray-600">Experience cutting-edge technology demonstrations</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full">
<i class="ri-robot-line text-primary text-xl"></i>
</div>
</div>
</div>
</div>
</div>
<div>
<h3 class="text-2xl font-['Playfair_Display'] font-bold mb-6">Common Activities</h3>
<div class="space-y-4">
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Spa & Wellness Center</h4>
<p class="text-gray-600">Rejuvenating treatments and relaxation services</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-secondary bg-opacity-10 rounded-full">
<i class="ri-spa-line text-secondary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Gourmet Dining</h4>
<p class="text-gray-600">Multi-cuisine restaurants and themed bars</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-secondary bg-opacity-10 rounded-full">
<i class="ri-restaurant-line text-secondary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Fitness Center</h4>
<p class="text-gray-600">State-of-the-art equipment and personal training</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-secondary bg-opacity-10 rounded-full">
<i class="ri-heart-pulse-line text-secondary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Swimming Pool</h4>
<p class="text-gray-600">Indoor and outdoor pools with lounging areas</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-secondary bg-opacity-10 rounded-full">
<i class="ri-swim-line text-secondary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Robot Construction</h4>
<p class="text-gray-600">Build and program your own robot companion</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-secondary bg-opacity-10 rounded-full">
<i class="ri-robot-2-line text-secondary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Painting Sessions</h4>
<p class="text-gray-600">Express yourself through various painting techniques</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-secondary bg-opacity-10 rounded-full">
<i class="ri-paint-brush-line text-secondary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Gardening Seminars</h4>
<p class="text-gray-600">Learn sustainable gardening practices</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-secondary bg-opacity-10 rounded-full">
<i class="ri-plant-line text-secondary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Storytelling Evenings</h4>
<p class="text-gray-600">Immersive tales from different eras</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-secondary bg-opacity-10 rounded-full">
<i class="ri-book-open-line text-secondary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Medieval Board Games</h4>
<p class="text-gray-600">Classic strategy games from the medieval period</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-secondary bg-opacity-10 rounded-full">
<i class="ri-gamepad-line text-secondary text-xl"></i>
</div>
</div>
</div>
<div class="bg-white rounded-lg shadow-sm p-6 border border-gray-100">
<div class="flex items-center justify-between">
<div>
<h4 class="text-lg font-semibold mb-2">Craft Workshops</h4>
<p class="text-gray-600">Create handmade items using traditional methods</p>
</div>
<div class="w-10 h-10 flex items-center justify-center bg-secondary bg-opacity-10 rounded-full">
<i class="ri-tools-line text-secondary text-xl"></i>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</section>
<section class="py-20">
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="text-center mb-16">
<h2 class="text-4xl font-['Playfair_Display'] font-bold mb-4">Our Rooms & Suites</h2>
<p class="text-gray-600 max-w-2xl mx-auto">Experience luxury accommodations across different eras, each room carefully designed to provide maximum comfort and unique experiences.</p>
</div>
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8 mb-20">
<div class="bg-white rounded-lg overflow-hidden shadow-sm group">
<div class="relative h-64">
<img src="https://public.readdy.ai/ai/img_res/b020d1760a4c8224d35ebffeea91f129.jpg" class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-110" alt="Standard Family Room">
<div class="absolute top-4 right-4 bg-white px-4 py-2 rounded-full shadow-md">
<span class="text-primary font-semibold">120 € / night</span>
</div>
</div>
<div class="p-6">
<h3 class="text-xl font-bold mb-2">Standard Family Room</h3>
<p class="text-gray-600 mb-4">Perfect for families, featuring comfortable twin beds, modern amenities, and a cozy atmosphere.</p>
<ul class="space-y-2 mb-6">
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>Twin Beds</li>
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>32" Smart TV</li>
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>Free Wi-Fi</li>
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>Air Conditioning</li>
</ul>
<button class="w-full bg-primary text-white py-3 !rounded-button hover:bg-opacity-90 transition-all whitespace-nowrap">Book Now</button>
</div>
</div>
<div class="bg-white rounded-lg overflow-hidden shadow-sm group">
<div class="relative h-64">
<img src="https://public.readdy.ai/ai/img_res/3bfc851823cd035e6d1ef9c039ced7f1.jpg" class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-110" alt="Superior Suite">
<div class="absolute top-4 right-4 bg-white px-4 py-2 rounded-full shadow-md">
<span class="text-primary font-semibold">180 € / night</span>
</div>
</div>
<div class="p-6">
<h3 class="text-xl font-bold mb-2">Superior Suite</h3>
<p class="text-gray-600 mb-4">Elevated comfort with a king-size bed, separate sitting area, and premium amenities.</p>
<ul class="space-y-2 mb-6">
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>King-Size Bed</li>
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>Sitting Area</li>
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>Mini Bar</li>
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>Premium Amenities</li>
</ul>
<button class="w-full bg-primary text-white py-3 !rounded-button hover:bg-opacity-90 transition-all whitespace-nowrap">Book Now</button>
</div>
</div>
<div class="bg-white rounded-lg overflow-hidden shadow-sm group">
<div class="relative h-64">
<img src="https://public.readdy.ai/ai/img_res/fe39d8a28f7c8eeac30a1c97105b5cda.jpg" class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-110" alt="Deluxe Family Suite">
<div class="absolute top-4 right-4 bg-white px-4 py-2 rounded-full shadow-md">
<span class="text-primary font-semibold">250 € / night</span>
</div>
</div>
<div class="p-6">
<h3 class="text-xl font-bold mb-2">Deluxe Family Suite</h3>
<p class="text-gray-600 mb-4">Spacious suite with separate living area, two bedrooms, and luxury amenities for the whole family.</p>
<ul class="space-y-2 mb-6">
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>Two Bedrooms</li>
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>Living Room</li>
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>Kitchenette</li>
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>2 Bathrooms</li>
</ul>
<button class="w-full bg-primary text-white py-3 !rounded-button hover:bg-opacity-90 transition-all whitespace-nowrap">Book Now</button>
</div>
</div>
<div class="bg-white rounded-lg overflow-hidden shadow-sm group">
<div class="relative h-64">
<img src="https://public.readdy.ai/ai/img_res/49824a85fd17c779faaccba36c7595b5.jpg" class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-110" alt="Premium Chrono Travel Suite">
<div class="absolute top-4 right-4 bg-white px-4 py-2 rounded-full shadow-md">
<span class="text-primary font-semibold">400 € / night</span>
</div>
</div>
<div class="p-6">
<h3 class="text-xl font-bold mb-2">Premium Chrono Travel Suite</h3>
<p class="text-gray-600 mb-4">Our flagship suite offering an immersive time-travel experience with era-specific decor and cutting-edge amenities.</p>
<ul class="space-y-2 mb-6">
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>Theme Customization</li>
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>Private Terrace</li>
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>Butler Service</li>
<li class="flex items-center text-gray-600"><i class="ri-checkbox-circle-line text-primary mr-2"></i>VIP Amenities</li>
</ul>
<button class="w-full bg-primary text-white py-3 !rounded-button hover:bg-opacity-90 transition-all whitespace-nowrap">Book Now</button>
</div>
</div>
</div>
</div>
</section>
<section class="py-20 bg-gray-50">
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="text-center mb-16">
<h2 class="text-4xl font-['Playfair_Display'] font-bold mb-4">Guest Testimonials</h2>
<p class="text-gray-600 max-w-2xl mx-auto">Read what our guests have to say about their unique experiences at Chrono Resort.</p>
</div>
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
<div class="bg-white rounded-lg p-6 shadow-sm">
<div class="flex items-center mb-4">
<div class="flex text-yellow-400">
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
</div>
<span class="ml-2 text-sm text-gray-600">Medieval Era</span>
</div>
<p class="text-gray-700 mb-4">"An incredible journey back in time! The attention to detail in the Medieval theme was outstanding. The feast and tournament were unforgettable experiences."</p>
<div class="flex items-center">
<img src="https://public.readdy.ai/ai/img_res/295f6a77ff525369ed7b61df6772776c.jpg" class="w-10 h-10 rounded-full object-cover" alt="Guest">
<div class="ml-3">
<h4 class="font-semibold">Michael Richardson</h4>
<p class="text-sm text-gray-600">London, UK</p>
</div>
</div>
</div>
<div class="bg-white rounded-lg p-6 shadow-sm">
<div class="flex items-center mb-4">
<div class="flex text-yellow-400">
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
</div>
<span class="ml-2 text-sm text-gray-600">Green Environment</span>
</div>
<p class="text-gray-700 mb-4">"The perfect blend of luxury and sustainability. The eco-adventures were enlightening, and the organic dining options were exceptional. A truly refreshing experience."</p>
<div class="flex items-center">
<img src="https://public.readdy.ai/ai/img_res/19b98238c2b4cccafb6b48f6aed5b312.jpg" class="w-10 h-10 rounded-full object-cover" alt="Guest">
<div class="ml-3">
<h4 class="font-semibold">Sarah Anderson</h4>
<p class="text-sm text-gray-600">Vancouver, Canada</p>
</div>
</div>
</div>
<div class="bg-white rounded-lg p-6 shadow-sm">
<div class="flex items-center mb-4">
<div class="flex text-yellow-400">
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
<i class="ri-star-fill"></i>
</div>
<span class="ml-2 text-sm text-gray-600">Advanced Era</span>
</div>
<p class="text-gray-700 mb-4">"Mind-blowing technology integration! The VR experiences were out of this world, and the automated room features made our stay incredibly comfortable."</p>
<div class="flex items-center">
<img src="https://public.readdy.ai/ai/img_res/d6b2d4e89c80d3a6e228404b16b218b6.jpg" class="w-10 h-10 rounded-full object-cover" alt="Guest">
<div class="ml-3">
<h4 class="font-semibold">David Chen</h4>
<p class="text-sm text-gray-600">Singapore</p>
</div>
</div>
</div>
</div>
</div>
</section>
<section class="py-20">
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="text-center mb-16">
<h2 class="text-4xl font-['Playfair_Display'] font-bold mb-4">Contact & Location</h2>
<p class="text-gray-600 max-w-2xl mx-auto">Discover our enchanting location in the Black Forest, conveniently situated near the historic spa town of Baden-Baden and Baden Airpark.</p>
</div>
<div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
<div>
<div class="bg-white rounded-lg p-8 shadow-sm">
<h3 class="text-2xl font-['Playfair_Display'] font-bold mb-6">Get in Touch</h3>
<div class="space-y-6">
<div>
<label class="block text-sm font-medium text-gray-700 mb-1">Name</label>
<input type="text" class="w-full border border-gray-300 rounded-md px-4 py-2" placeholder="Your name">
</div>
<div>
<label class="block text-sm font-medium text-gray-700 mb-1">Email</label>
<input type="email" class="w-full border border-gray-300 rounded-md px-4 py-2" placeholder="Your email">
</div>
<div>
<label class="block text-sm font-medium text-gray-700 mb-1">Message</label>
<textarea class="w-full border border-gray-300 rounded-md px-4 py-2 h-32" placeholder="Your message"></textarea>
</div>
<button class="w-full bg-primary text-white py-3 !rounded-button hover:bg-opacity-90 transition-all whitespace-nowrap cursor-pointer">
Send Message
</button>
</div>
<div class="mt-8 space-y-4">
<div class="flex items-center">
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full">
<i class="ri-map-pin-line text-primary"></i>
</div>
<div class="ml-4">
<h4 class="font-semibold">Address</h4>
<p class="text-gray-600">Schwarzwaldhochstraße 150, 77815 Bühl, Germany</p>
<p class="text-gray-600 text-sm">15 min from Baden-Baden | 20 min from Baden Airpark</p>
</div>
</div>
<div class="flex items-center">
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full">
<i class="ri-phone-line text-primary"></i>
</div>
<div class="ml-4">
<h4 class="font-semibold">Phone</h4>
<p class="text-gray-600">+30 210 8202567</p>
</div>
</div>
<div class="flex items-center">
<div class="w-10 h-10 flex items-center justify-center bg-primary bg-opacity-10 rounded-full">
<i class="ri-mail-line text-primary"></i>
</div>
<div class="ml-4">
<h4 class="font-semib old">Email</h4>
<p class="text-gray-600">info@chronoresort.com</p>
</div>
</div>
</div>
</div>
</div>
<div class="h-[600px] rounded-lg overflow-hidden shadow-sm relative">
<img src="https://public.readdy.ai/gen_page/map_placeholder_1280x720.png" alt="Resort Location Map" class="w-full h-full object-cover">
<div class="absolute inset-0 bg-gradient-to-b from-transparent to-black/30"></div>
<div class="absolute bottom-6 left-6 bg-white/90 p-4 rounded-lg shadow-lg">
<h4 class="font-semibold text-primary mb-2">Chrono Resort</h4>
<p class="text-sm text-gray-600">Nestled in Black Forest, just 15 minutes from Baden-Baden</p>
<p class="text-sm text-gray-600">20 minutes from Baden Airpark (FKB)</p>
<p class="text-sm text-gray-600">Schwarzwaldhochstraße 150, 77815 Bühl, Germany</p>
</div>
</div>
</div>
</div>
</section>
</main>
<footer class="bg-gray-900 text-white py-20">
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
<div>
<a href="/" class="font-['Pacifico'] text-2xl text-white mb-4 block">Chrono Resort</a>
<p class="text-gray-400">Experience luxury across different eras in one unique destination.</p>
<div class="flex space-x-4 mt-6">
<a href="#" class="text-gray-400 hover:text-white"><i class="ri-facebook-fill"></i></a>
<a href="#" class="text-gray-400 hover:text-white"><i class="ri-twitter-fill"></i></a>
<a href="#" class="text-gray-400 hover:text-white"><i class="ri-instagram-fill"></i></a>
<a href="#" class="text-gray-400 hover:text-white"><i class="ri-linkedin-fill"></i></a>
</div>
</div>
<div>
<h4 class="text-lg font-semibold mb-4">Quick Links</h4>
<ul class="space-y-2">
<li><a href="#" class="text-gray-400 hover:text-white">About Us</a></li>
<li><a href="#" class="text-gray-400 hover:text-white">Rooms & Suites</a></li>
<li><a href="#" class="text-gray-400 hover:text-white">Dining</a></li>
<li><a href="#" class="text-gray-400 hover:text-white">Spa & Wellness</a></li>
<li><a href="#" class="text-gray-400 hover:text-white">Events</a></li>
</ul>
</div>
<div>
<h4 class="text-lg font-semibold mb-4">Themes</h4>
<ul class="space-y-2">
<li><a href="#" class="text-gray-400 hover:text-white">Medieval Era</a></li>
<li><a href="#" class="text-gray-400 hover:text-white">Green Environment</a></li>
<li><a href="#" class="text-gray-400 hover:text-white">Modern Era</a></li>
<li><a href="#" class="text-gray-400 hover:text-white">Advanced Era</a></li>
</ul>
</div>
<div>
<h4 class="text-lg font-semibold mb-4">Newsletter</h4>
<p class="text-gray-400 mb-4">Subscribe to our newsletter for special offers and updates.</p>
<form class="space-y-4">
<input type="email" class="w-full bg-gray-800 border border-gray-700 rounded-md px-4 py-2 text-white" placeholder="Your email">
<button class="w-full bg-primary text-white py-2 rounded-md hover:bg-opacity-90">Subscribe</button>
</form>
</div>
</div>
<div class="border-t border-gray-800 mt-16 pt-8 text-center">
<p class="text-gray-400">&copy; 2025 Chrono Resort. All rights reserved.</p>
</div>
</div>
</footer>
<div class="fixed bottom-8 right-8 z-50 space-y-4">
<button id="scrollToTop" class="w-12 h-12 bg-primary text-white rounded-full shadow-lg flex items-center justify-center hover:bg-opacity-90 transition-all opacity-0 invisible transition-opacity duration-300">
<i class="ri-arrow-up-line"></i>
</button>
<script>
const scrollToTopButton = document.getElementById('scrollToTop');
window.addEventListener('scroll', () => {
if (window.pageYOffset > 300) {
scrollToTopButton.classList.remove('opacity-0', 'invisible');
} else {
scrollToTopButton.classList.add('opacity-0', 'invisible');
}
});
scrollToTopButton.addEventListener('click', () => {
window.scrollTo({
top: 0,
behavior: 'smooth'
});
});
</script>
<button class="w-12 h-12 bg-green-500 text-white rounded-full shadow-lg flex items-center justify-center hover:bg-opacity-90 transition-all">
<i class="ri-whatsapp-line"></i>
</button>
</div>
</body>
</html>
       
   
