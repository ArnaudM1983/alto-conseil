<template>
    <section id="contact">
    <div class="container px-6 py-12 mx-auto">
        <div class="lg:flex lg:items-center lg:-mx-6">
            <div class="lg:w-1/2 lg:mx-6">
                <h2 class="text-3xl mb-10 md:text-6xl font-semibold text-white sm:text-3xl text-left">
            Contactez-nous
        </h2>

                <div class="mt-6 space-y-8 md:mt-8">
                    <p class="flex items-start -mx-2">
                        <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6 mx-2 text-blue-500 dark:text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                        </svg>

                        <span class="mx-2 text-gray-700 truncate w-72 dark:text-gray-400 text-left">+33601010101</span>
                    </p>

                    <p class="flex items-start -mx-2">
                        <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6 mx-2 text-blue-500 dark:text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                        </svg>

                        <span class="mx-2 text-gray-700 truncate w-72 dark:text-gray-400 text-left">rayolhorizon@example.com</span>
                    </p>
                </div>
            </div>

            <div class="mt-8 lg:w-1/2 lg:mx-6">
                <div
                    class="w-full px-8 py-10 mx-auto overflow-hidden  rounded-lg shadow-2xl lg:max-w-xl shadow-gray-300/50 dark:shadow-black/50">
                    <p class="text-lg font-medium text-white text-left">Besoin d’aide ou d’infos ? Écrivez-nous</p>

                    <form class="mt-6">
                        <div class="flex-1">
                            <label class="block mb-2 text-sm text-gray-600 dark:text-gray-200 text-left">Votre Nom</label>
                            <input type="text" class="w-full px-6 py-2 text-lg font-light text-white border border-gray-400 bg-transparent rounded-none placeholder-gray-300 focus:outline-none focus:ring-0 focus:border-white transition"
                            />
                        </div>

                        <div class="flex-1 mt-6">
                            <label class="block mb-2 text-sm text-gray-600 dark:text-gray-200 text-left">Adresse Email</label>
                            <input type="email" class="w-full px-6 py-2 text-lg font-light text-white border border-gray-400 bg-transparent rounded-none placeholder-gray-300 focus:outline-none focus:ring-0 focus:border-white transition"
                            />
                        </div>

                        <div class="w-full mt-6">
                            <label class="block mb-2 text-sm text-gray-600 dark:text-gray-200 text-left">Votre Message</label>
                            <textarea class="w-full px-6 py-2 text-lg font-light text-white border border-gray-400 bg-transparent rounded-none placeholder-gray-300 focus:outline-none focus:ring-0 focus:border-white transition"
                            ></textarea>
                        </div>

                        <button class="w-full text-white border border-white mt-8 px-6 py-2 text-lg font-light cursor-pointer bg-transparent rounded-none hover:bg-white hover:text-black transition">
                            Soumettre le formulaire
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </div>
</section>
</template>