<script setup lang="ts">
defineProps<{
    title: string
    git?: string
    demo?: string
    image?: string
    imageAlt?: string
}>()
</script>

<template>
    <section class="relative isolate overflow-hidden">
        <div
            class="mx-auto max-w-7xl px-4 py-24 sm:py-32"
            :class="{ 'grid items-center gap-12 lg:grid-cols-2': image }"
        >
            <div>
                <p class="mb-4 text-sm font-semibold uppercase tracking-[0.2em] text-neutral-400">
                    Project
                </p>
                <h1 class="text-4xl font-bold tracking-tight sm:text-6xl">
                    {{ title }}
                </h1>
                <div v-if="git || demo" class="mt-8 flex flex-wrap gap-4">
                    <a
                        v-if="demo"
                        :href="demo"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="rounded-md bg-white px-5 py-2.5 text-sm font-semibold text-neutral-900 hover:bg-neutral-200"
                    >
                        Demo
                    </a>
                    <a
                        v-if="git"
                        :href="git"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="rounded-md border border-neutral-600 px-5 py-2.5 text-sm font-semibold hover:border-neutral-400"
                    >
                        Source
                    </a>
                </div>
            </div>
            <img
                v-if="image"
                :src="image"
                :alt="imageAlt ?? title"
                class="w-full rounded-xl border border-neutral-800 object-cover shadow-2xl"
            >
        </div>
    </section>
</template>
