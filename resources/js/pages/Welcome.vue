<script setup lang="ts">
import { Head, Link } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Welcome">
        <link rel="preconnect" href="https://rsms.me/" />
        <link rel="stylesheet" href="https://rsms.me/inter/inter.css" />
    </Head>
    <div class="flex min-h-screen flex-col items-center bg-[#FDFDFC] p-6 text-[#1b1b18] dark:bg-[#0a0a0a] lg:justify-center lg:p-8">
        <header class="not-has-[nav]:hidden mb-6 w-full max-w-[335px] text-sm lg:max-w-4xl">
            <nav class="flex items-center justify-end gap-4">
                <Link
                    v-if="$page.props.auth.user"
                    :href="route('dashboard')"
                    class="inline-block rounded-sm border border-[#19140035] px-5 py-1.5 text-sm leading-normal text-[#1b1b18] hover:border-[#1915014a] dark:border-[#3E3E3A] dark:text-[#EDEDEC] dark:hover:border-[#62605b]"
                >
                    Dashboard
                </Link>
                <template v-else>
                    <Link
                        :href="route('login')"
                        class="inline-block rounded-sm border border-transparent px-5 py-1.5 text-sm leading-normal text-[#1b1b18] hover:border-[#19140035] dark:text-[#EDEDEC] dark:hover:border-[#3E3E3A]"
                    >
                        Log in
                    </Link>
                    <Link
                        :href="route('register')"
                        class="inline-block rounded-sm border border-[#19140035] px-5 py-1.5 text-sm leading-normal text-[#1b1b18] hover:border-[#1915014a] dark:border-[#3E3E3A] dark:text-[#EDEDEC] dark:hover:border-[#62605b]"
                    >
                        Register
                    </Link>
                </template>
            </nav>
        </header>
        <div class="duration-750 starting:opacity-0 flex w-full items-center justify-center opacity-100 transition-opacity lg:grow">
            <div class="max-w-[335px] lg:max-w-4xl w-full">
                <div class="rounded-xl border border-sidebar-border/70 dark:border-sidebar-border p-8 flex flex-col gap-6 bg-white dark:bg-[#121212] shadow-sm">
                    <div class="flex items-center gap-4">
                        <div class="h-12 w-12 rounded-full bg-gradient-to-br from-indigo-500 to-purple-600 flex items-center justify-center text-white font-bold text-xl">SFM</div>
                        <div>
                            <h1 class="text-2xl font-semibold text-white">Welcome to Smart Fish Measurement</h1>
                            <p class="text-gray-600 dark:text-gray-400">Accurately measure and analyze fish with AI-powered tools</p>
                        </div>
                    </div>
                    
                    <p class="text-gray-700 dark:text-gray-300">
                        Smart Fish Measurement is an AI-powered platform that helps you accurately measure, track, and analyze fish species with precision. Our advanced technology eliminates the need for manual measurements and provides detailed analytics for researchers, anglers, and conservation efforts.
                    </p>
                    
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                        <div class="rounded-lg border border-sidebar-border/50 dark:border-sidebar-border/30 p-4">
                            <h3 class="font-medium mb-2">Build Agents</h3>
                            <p class="text-sm text-gray-600 dark:text-gray-400">Create custom agents with our intuitive interface</p>
                        </div>
                        <div class="rounded-lg border border-sidebar-border/50 dark:border-sidebar-border/30 p-4">
                            <h3 class="font-medium mb-2">Deploy Anywhere</h3>
                            <p class="text-sm text-gray-600 dark:text-gray-400">Integrate with your existing systems seamlessly</p>
                        </div>
                    </div>
                    
                    <div class="flex justify-center">
                        <Link
                            :href="route('register')"
                            class="px-6 py-2 bg-gradient-to-r from-indigo-500 to-purple-600 text-white rounded-md hover:opacity-90 transition-opacity"
                        >
                            Get Started
                        </Link>
                    </div>
                </div>
            </div>
        </div>
        <div class="h-14.5 hidden lg:block"></div>
    </div>
</template>
