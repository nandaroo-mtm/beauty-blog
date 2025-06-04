<template>
    <div class="bg-white shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
            
            <!-- Logo -->
            <div class="flex-shrink-0"  @click="onClickMenu">
                <a href="#" class="text-xl font-bold text-blue-600">MyApp</a>
            </div>

            <!-- Navigation -->
            <nav class="hidden md:flex space-x-6">
                <a href="#" class="text-gray-700 hover:text-blue-600">Home</a>
                <a href="#" class="text-gray-700 hover:text-blue-600">Features</a>
                <a href="#" class="text-gray-700 hover:text-blue-600">Pricing</a>
                <a href="#" class="text-gray-700 hover:text-blue-600">Contact</a>
            </nav>

            <!-- Right Side (e.g., Login/Avatar) -->
            <div class="hidden md:flex items-center space-x-4">
                <button class="px-4 py-2 text-sm font-medium text-white bg-blue-600 rounded hover:bg-blue-700">
                Login
                </button>
            </div>

            <!-- Mobile menu button -->
            <div class="md:hidden">
                <button 
                    id="mobile-menu-button" 
                    class="text-gray-700 hover:text-blue-600 focus:outline-none"
                    @click="onClickMenu"
                >
                    <svg class="h-6 w-6" fill="none" stroke="currentColor" stroke-width="2"
                        viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
            </div>

            </div>
        </div>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="md:hidden hidden px-4 pb-4">
            <a href="#" class="block py-2 text-gray-700 hover:text-blue-600">Home</a>
            <a href="#" class="block py-2 text-gray-700 hover:text-blue-600">Features</a>
            <a href="#" class="block py-2 text-gray-700 hover:text-blue-600">Pricing</a>
            <a href="#" class="block py-2 text-gray-700 hover:text-blue-600">Contact</a>
            <button class="w-full mt-2 px-4 py-2 text-sm font-medium text-white bg-blue-600 rounded hover:bg-blue-700">
            Login
            </button>
        </div>

    
    </div>

</template>

<!-- Optional JS to toggle mobile menu -->
<script>
export default {
  setup(props, root) {
    const { emit } = root;

    const onClickMenu = () => {
        console.log('onclickmenu');
    }

    return {
      onClickMenu
    }
  }
}
// const btn = window.document.getElementById('mobile-menu-button');
// const menu = window.document.getElementById('mobile-menu');

// btn.addEventListener('click', () => {
// menu.classList.toggle('hidden');
// });
</script>