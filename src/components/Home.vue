<template>
    <div class="min-h-screen bg-slate-950 text-white">

        <!-- NAVBAR -->
        <header class="fixed inset-x-0 top-0 z-50 border-b border-white/10 bg-slate-950/80 backdrop-blur-xl">
            <nav class="mx-auto flex max-w-7xl items-center justify-between px-6 py-5 lg:px-8">

                <!-- Logo -->
                <a href="#home" class="text-2xl font-bold">
                    K<span class="text-cyan-400">.....</span>
                </a>

                <!-- Desktop Navigation -->
                <div class="hidden items-center gap-8 md:flex">
                    <a href="#home" class="text-sm text-slate-300 transition hover:text-cyan-400">
                        Home
                    </a>

                    <a href="#about" class="text-sm text-slate-300 transition hover:text-cyan-400">
                        About
                    </a>

                    <a href="#services" class="text-sm text-slate-300 transition hover:text-cyan-400">
                        Services
                    </a>

                    <a href="#projects" class="text-sm text-slate-300 transition hover:text-cyan-400">
                        Projects
                    </a>

                    <a href="#contact"
                        class="rounded-full bg-cyan-400 px-5 py-2 text-sm font-semibold text-slate-950 transition hover:bg-cyan-300">
                        Contact Me
                    </a>
                </div>

                <!-- Mobile Menu Button -->
                <button @click="mobileMenuOpen = !mobileMenuOpen"
                    class="flex h-10 w-10 items-center justify-center rounded-lg border border-white/10 text-slate-300 transition hover:border-cyan-400/40 hover:text-cyan-400 md:hidden"
                    aria-label="Toggle menu">
                    <!-- Hamburger -->
                    <svg v-if="!mobileMenuOpen" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                        stroke-width="2" stroke="currentColor" class="h-6 w-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
                    </svg>

                    <!-- Close -->
                    <svg v-else xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2"
                        stroke="currentColor" class="h-6 w-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                </button>

            </nav>

            <!-- Mobile Navigation -->
            <div v-if="mobileMenuOpen"
                class="border-t border-white/10 bg-slate-950/95 px-6 py-5 backdrop-blur-xl md:hidden">
                <div class="flex flex-col gap-2">

                    <a href="#home" @click="mobileMenuOpen = false"
                        class="rounded-lg px-4 py-3 text-sm text-slate-300 transition hover:bg-white/5 hover:text-cyan-400">
                        Home
                    </a>

                    <a href="#about" @click="mobileMenuOpen = false"
                        class="rounded-lg px-4 py-3 text-sm text-slate-300 transition hover:bg-white/5 hover:text-cyan-400">
                        About
                    </a>

                    <a href="#services" @click="mobileMenuOpen = false"
                        class="rounded-lg px-4 py-3 text-sm text-slate-300 transition hover:bg-white/5 hover:text-cyan-400">
                        Services
                    </a>

                    <a href="#projects" @click="mobileMenuOpen = false"
                        class="rounded-lg px-4 py-3 text-sm text-slate-300 transition hover:bg-white/5 hover:text-cyan-400">
                        Projects
                    </a>

                    <a href="#contact" @click="mobileMenuOpen = false"
                        class="mt-2 rounded-full bg-cyan-400 px-5 py-3 text-center text-sm font-semibold text-slate-950 transition hover:bg-cyan-300">
                        Contact Me
                    </a>

                </div>
            </div>
        </header>

        <!-- HERO -->
        <section id="home" class="relative flex min-h-screen items-center overflow-hidden">

            <div class="absolute -left-40 top-20 h-96 w-96 rounded-full bg-cyan-500/10 blur-3xl"></div>
            <div class="absolute -right-40 bottom-0 h-96 w-96 rounded-full bg-blue-600/10 blur-3xl"></div>

            <div class="relative mx-auto grid max-w-7xl items-center gap-16 px-6 pt-28 lg:grid-cols-2 lg:px-8">

                <!-- INTRO -->
                <div>

                    <p class="mb-5 text-sm font-medium uppercase tracking-[0.3em] text-cyan-400">
                        Web Developer
                    </p>

                    <h1 class="text-5xl font-bold leading-tight tracking-tight sm:text-6xl lg:text-7xl">
                        I build
                        <span class="block bg-gradient-to-r from-cyan-300 to-blue-500 bg-clip-text text-transparent">
                            modern websites.
                        </span>
                    </h1>

                    <p class="mt-7 max-w-xl text-lg leading-8 text-slate-400">
                        I'm Kaveesha, a Laravel developer focused on building modern
                        web applications, responsive websites and powerful digital
                        experiences using Laravel, Vue.js, WordPress and SEO.
                    </p>

                    <div class="mt-9 flex flex-wrap gap-4">

                        <a href="#projects"
                            class="rounded-full bg-cyan-400 px-7 py-3 font-semibold text-slate-950 transition hover:bg-cyan-300">
                            View My Work
                        </a>

                        <a href="#contact"
                            class="rounded-full border border-white/15 px-7 py-3 font-semibold transition hover:border-cyan-400 hover:text-cyan-300">
                            Let's Work Together
                        </a>

                    </div>

                    <!-- Skills -->
                    <div class="mt-10 flex flex-wrap gap-3">

                        <span v-for="skill in skills" :key="skill"
                            class="rounded-full border border-white/10 bg-white/5 px-4 py-2 text-xs text-slate-400">
                            {{ skill }}
                        </span>

                    </div>

                </div>


                <!-- CODE CARD -->
                <div class="relative">

                    <div
                        class="mx-auto max-w-md rounded-3xl border border-white/10 bg-white/[0.03] p-6 shadow-2xl backdrop-blur-xl">

                        <div class="mb-7 flex items-center gap-2">

                            <span class="h-3 w-3 rounded-full bg-red-400/70"></span>
                            <span class="h-3 w-3 rounded-full bg-yellow-400/70"></span>
                            <span class="h-3 w-3 rounded-full bg-green-400/70"></span>

                            <span class="ml-auto text-xs text-slate-600">
                                developer.php
                            </span>

                        </div>

                        <div class="space-y-3 font-mono text-sm leading-7">

                            <p>
                                <span class="text-purple-400">class</span>
                                <span class="text-cyan-300"> Developer</span>
                            </p>

                            <p class="pl-5 text-white">{</p>

                            <p class="pl-10">
                                <span class="text-slate-500">$role</span>
                                <span class="text-white"> = </span>
                                <span class="text-green-300">
                                    "Laravel Developer"
                                </span>;
                            </p>

                            <p class="pl-10">
                                <span class="text-slate-500">$frontend</span>
                                <span class="text-white"> = </span>
                                <span class="text-green-300">
                                    "Vue.js"
                                </span>;
                            </p>

                            <p class="pl-10">
                                <span class="text-slate-500">$cms</span>
                                <span class="text-white"> = </span>
                                <span class="text-green-300">
                                    "WordPress"
                                </span>;
                            </p>

                            <p class="pl-10">
                                <span class="text-slate-500">$seo</span>
                                <span class="text-white"> = </span>
                                <span class="text-green-300">
                                    true
                                </span>;
                            </p>

                            <p class="pl-10">
                                <span class="text-slate-500">$passion</span>
                                <span class="text-white"> = </span>
                                <span class="text-green-300">
                                    "Building"
                                </span>;
                            </p>

                            <p class="pl-5 text-white">}</p>

                        </div>

                    </div>

                </div>

            </div>

        </section>


        <!-- ABOUT -->
        <section id="about" class="border-t border-white/5 py-28">

            <div class="mx-auto max-w-7xl px-6 lg:px-8">

                <p class="text-sm font-medium uppercase tracking-[0.3em] text-cyan-400">
                    About Me
                </p>

                <div class="mt-6 grid gap-12 lg:grid-cols-2">

                    <h2 class="text-4xl font-bold leading-tight sm:text-5xl">
                        Developer focused on
                        <span class="text-cyan-400">
                            building real solutions.
                        </span>
                    </h2>

                    <div class="space-y-5 leading-8 text-slate-400">

                        <p>
                            I'm a Laravel developer who enjoys creating reliable,
                            scalable and user-friendly web applications.
                        </p>

                        <p>
                            My main stack includes Laravel and Vue.js, while I also
                            work with WordPress and SEO to help businesses build
                            and grow their online presence.
                        </p>

                        <p>
                            I focus on clean development, responsive interfaces,
                            performance and practical solutions to real-world problems.
                        </p>

                    </div>

                </div>

            </div>

        </section>
        <!-- CV SECTION -->
        <section id="cv" class="border-t border-white/5 py-24">
            <div class="mx-auto max-w-5xl px-6 lg:px-8">

                <div class="relative overflow-hidden rounded-3xl border border-cyan-400/20 bg-white/[0.03] p-8 sm:p-12">

                    <!-- Glow -->
                    <div
                        class="pointer-events-none absolute -right-20 -top-20 h-60 w-60 rounded-full bg-cyan-400/10 blur-3xl">
                    </div>

                    <div
                        class="pointer-events-none absolute -bottom-20 -left-20 h-60 w-60 rounded-full bg-blue-500/10 blur-3xl">
                    </div>

                    <div class="relative flex flex-col items-center justify-between gap-8 md:flex-row">

                        <!-- Text -->
                        <div class="text-center md:text-left">

                            <p class="text-sm font-medium uppercase tracking-[0.3em] text-cyan-400">
                                My Resume
                            </p>

                            <h2 class="mt-4 text-3xl font-bold text-white sm:text-4xl">
                                Want to know more about me?
                            </h2>

                            <p class="mt-4 max-w-xl leading-7 text-slate-400">
                                Download my CV to learn more about my skills, experience,
                                projects and professional background.
                            </p>

                        </div>


                        <!-- Download Button -->
                        <a href="/Kaveesha-Godigamuwa-CV.pdf" download
                            class="group inline-flex shrink-0 items-center gap-3 rounded-full bg-cyan-400 px-7 py-3.5 font-semibold text-slate-950 transition duration-300 hover:-translate-y-1 hover:bg-cyan-300 hover:shadow-lg hover:shadow-cyan-400/20">

                            <!-- Download Icon -->
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2"
                                stroke="currentColor" class="h-5 w-5 transition group-hover:translate-y-0.5">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M3 16.5v2.25A2.25 2.25 0 005.25 21h13.5A2.25 2.25 0 0021 18.75V16.5M16.5 12L12 16.5m0 0L7.5 12m4.5 4.5V3" />
                            </svg>

                            Download CV

                        </a>

                    </div>

                </div>

            </div>
        </section>

        <!-- SERVICES -->
        <section id="services" class="border-t border-white/5 py-28">

            <div class="mx-auto max-w-7xl px-6 lg:px-8">

                <p class="text-sm font-medium uppercase tracking-[0.3em] text-cyan-400">
                    What I Do
                </p>

                <h2 class="mt-4 text-4xl font-bold sm:text-5xl">
                    My Services
                </h2>

                <div class="mt-12 grid gap-6 md:grid-cols-2 lg:grid-cols-4">

                    <div v-for="service in services" :key="service.title"
                        class="rounded-3xl border border-white/10 bg-white/[0.03] p-7 transition duration-300 hover:-translate-y-2 hover:border-cyan-400/30">

                        <div class="text-3xl">
                            {{ service.icon }}
                        </div>

                        <h3 class="mt-6 text-xl font-semibold">
                            {{ service.title }}
                        </h3>

                        <p class="mt-4 text-sm leading-7 text-slate-400">
                            {{ service.description }}
                        </p>

                    </div>

                </div>

            </div>

        </section>


        <!-- PROJECTS -->
        <section id="projects" class="border-t border-white/5 py-28">

            <div class="mx-auto max-w-7xl px-6 lg:px-8">

                <p class="text-sm font-medium uppercase tracking-[0.3em] text-cyan-400">
                    Portfolio
                </p>

                <h2 class="mt-4 text-4xl font-bold sm:text-5xl">
                    Recent Projects
                </h2>

                <p class="mt-5 max-w-2xl text-slate-400">
                    A selection of websites and applications I've worked on.
                </p>


                <!-- PROJECT CARDS -->
                <div class="mt-12 grid gap-8 lg:grid-cols-2">

                    <article v-for="project in projects" :key="project.title"
                        class="group overflow-hidden rounded-3xl border border-white/10 bg-white/[0.03] transition duration-300 hover:-translate-y-2 hover:border-cyan-400/30">

                        <!-- REAL WEBSITE SCREENSHOT -->
                        <div class="relative aspect-video overflow-hidden bg-slate-900">

                            <img :src="project.image" :alt="project.title"
                                class="h-full w-full object-cover object-top transition duration-500 group-hover:scale-105" />

                            <!-- Overlay -->
                            <div
                                class="absolute inset-0 flex items-center justify-center bg-slate-950/0 transition duration-300 group-hover:bg-slate-950/60">

                                <a v-if="project.url" :href="project.url" target="_blank"
                                    class="scale-75 rounded-full bg-white px-6 py-3 text-sm font-semibold text-slate-950 opacity-0 transition group-hover:scale-100 group-hover:opacity-100">
                                    Visit Website →
                                </a>

                            </div>

                        </div>


                        <!-- PROJECT CONTENT -->
                        <div class="p-7">

                            <div class="flex items-start justify-between gap-4">

                                <div>
                                    <h3 class="text-2xl font-semibold">
                                        {{ project.title }}
                                    </h3>

                                    <p class="mt-3 text-sm leading-7 text-slate-400">
                                        {{ project.description }}
                                    </p>
                                </div>

                            </div>


                            <div class="mt-6 flex flex-wrap gap-2">

                                <span v-for="tech in project.technologies" :key="tech"
                                    class="rounded-full bg-white/5 px-3 py-1 text-xs text-slate-400">
                                    {{ tech }}
                                </span>

                            </div>

                        </div>

                    </article>

                </div>

            </div>

        </section>


        <!-- CONTACT -->

        <section id="contact" class="border-t border-white/5 py-28">

            <div class="mx-auto max-w-5xl px-6 lg:px-8">

                <!-- Heading -->
                <div class="text-center">

                    <p class="text-sm font-medium uppercase tracking-[0.3em] text-cyan-400">
                        Contact
                    </p>

                    <h2 class="mt-5 text-4xl font-bold sm:text-6xl">
                        Have a project in mind?
                    </h2>

                    <p class="mx-auto mt-6 max-w-2xl leading-8 text-slate-400">
                        Let's discuss your idea and build something useful,
                        modern and effective.
                    </p>

                </div>


                <!-- Contact Details -->
                <div class="mt-12 grid gap-5 sm:grid-cols-2">

                    <!-- Email -->
                    <a href="mailto:kaveeshagodigamuwa6@gmail.com"
                        class="group rounded-2xl border border-white/10 bg-white/[0.03] p-6 transition duration-300 hover:-translate-y-1 hover:border-cyan-400/30 hover:bg-white/[0.05]">

                        <div class="flex items-center gap-5">

                            <div
                                class="flex h-12 w-12 shrink-0 items-center justify-center rounded-xl bg-cyan-400/10 text-xl text-cyan-400">
                                ✉
                            </div>

                            <div class="text-left">
                                <p class="text-xs uppercase tracking-wider text-slate-500">
                                    Email
                                </p>

                                <p
                                    class="mt-1 break-all font-medium text-slate-200 transition group-hover:text-cyan-300">
                                    kaveeshagodigamuwa6@gmail.com
                                </p>
                            </div>

                        </div>

                    </a>


                    <!-- Phone -->
                    <a href="tel:0758935658"
                        class="group rounded-2xl border border-white/10 bg-white/[0.03] p-6 transition duration-300 hover:-translate-y-1 hover:border-cyan-400/30 hover:bg-white/[0.05]">

                        <div class="flex items-center gap-5">

                            <div
                                class="flex h-12 w-12 shrink-0 items-center justify-center rounded-xl bg-cyan-400/10 text-xl text-cyan-400">
                                ☎
                            </div>

                            <div class="text-left">
                                <p class="text-xs uppercase tracking-wider text-slate-500">
                                    Phone
                                </p>

                                <p class="mt-1 font-medium text-slate-200 transition group-hover:text-cyan-300">
                                    075 893 5658
                                </p>
                            </div>

                        </div>

                    </a>

                </div>


                <!-- CTA -->
                <div class="mt-10 text-center">

                    <a href="mailto:kaveeshagodigamuwa6@gmail.com"
                        class="inline-flex items-center gap-2 rounded-full bg-cyan-400 px-8 py-3 font-semibold text-slate-950 transition hover:bg-cyan-300">
                        Get In Touch
                        <span>→</span>
                    </a>

                </div>

            </div>

        </section>




        <!-- FOOTER -->
        <footer class="border-t border-white/5 py-8">

            <div
                class="mx-auto flex max-w-7xl flex-col justify-between gap-4 px-6 text-sm text-slate-500 sm:flex-row lg:px-8">

                <p>
                    © {{ new Date().getFullYear() }} Kaveesha.
                    All rights reserved.
                </p>

                <p>
                    Laravel · Vue.js · WordPress · SEO
                </p>

            </div>

        </footer>

    </div>
</template>


<script setup>
import { ref } from 'vue'
const mobileMenuOpen = ref(false)

import nativaImage from '../assets/nativa.png'
import lndImage from '../assets/lnd.png'
import grafix from '../assets/grafix.png'
import harusakilanka from '../assets/harusakilanka.png'
import dmac from '../assets/dmac.png'
import tranq from '../assets/tranq.png'
import telegram from '../assets/telegram.png'

const skills = [
    "Laravel",
    "Vue.js",
    "PHP",
    "WordPress",
    "SEO",
    "MySQL"
]


const services = [
    {
        icon: "⌘",
        title: "Laravel Development",
        description:
            "Custom web applications, APIs, dashboards and backend systems built with Laravel."
    },
    {
        icon: "◈",
        title: "Vue.js Development",
        description:
            "Modern, responsive and interactive interfaces using Vue.js."
    },
    {
        icon: "W",
        title: "WordPress",
        description:
            "Professional business websites, customizations and WordPress solutions."
    },
    {
        icon: "↗",
        title: "SEO",
        description:
            "Technical SEO, content optimization and website improvements to increase visibility."
    }
]


const projects = [
    {
        title: "Nativa Staffing",
        description:
            "A workforce management platform with dashboards, worker management and automated communication features.",
        image: nativaImage,
        url: "https://nativastaffing.com/",
        technologies: [
            "Laravel",
            "MySQL"
        ]
    },

    {
        title: "LND Graphics",
        description: "A professional graphic design and printing company website showcasing creative design services, branding, and printing solutions.",
        image: lndImage,
        url: "https://lndgraphics.com/",
        technologies: [
            "Wordpress"
        ]
    },

    {
        title: "HarusakiLanka",
        description:
            "A responsive business website built with WordPress and optimized for search engines.",
        image: harusakilanka,
        url: "https://harusakilanka.com/",
        technologies: [
            "WordPress",
            "SEO",
            "CSS"
        ]
    },

    {
        title: "Grafix",
        description: "A professional graphic design and printing company website showcasing creative design services, branding, and printing solutions.",
        image: grafix,
        url: "https://grafixadz.com/",
        technologies: [
            "WordPress",
            "Responsive Design"
        ]
    },

    {
        title: "D-MAC Fashion",
        description:
            "A responsive business website built with WordPress and optimized for search engines.",
        image: dmac,
        url: "https://dmacfashion.com/",
        technologies: [
            "WordPress",
        ]
    },

    {
        title: "Telegram E-SHOP",
        description:
            "A digital e-commerce platform focused on online selling and cryptocurrency transfers, providing customers with a convenient way to purchase products and manage digital payments.",
        image: telegram,
        url: "#",
        technologies: [
            "PHP",
            "WooCommerce",
            "Cryptocurrency"
        ]
    },
    {
        title: "Tranquil Tots",
        description:
            "A professional sleep consultancy website designed to help families improve their children's sleep through personalized guidance, expert resources and tailored sleep solutions.",
        image: tranq,
        url: "#",
        technologies: [
            "Laravel",
            "MySQL"
        ]
    },
]

</script>
