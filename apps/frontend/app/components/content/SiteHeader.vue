<template>
    <header class="border-b border-neutral-600">
        <div class="container mx-auto flex items-center justify-between px-4 py-4">
            <a
                href="/"
                class="text-2xl font-bold text-neutral-200 hover:text-neutral-100"
            >
                <span class="text-2xl font-bold">0x7A3F</span>
            </a>

            <div class="group relative">
                <button
                    type="button"
                    class="text-neutral-200 hover:text-neutral-100"
                >
                    Projects ▾
                </button>

                <div class="invisible absolute right-0 top-full z-10 pt-2 group-hover:visible group-focus-within:visible">
                    <div class="flex min-w-48 flex-col rounded-md border border-neutral-600 bg-neutral-900 py-2">
                        <a
                            href="/projects/link-check"
                            class="px-4 py-2 text-sm text-neutral-300 hover:bg-neutral-800 hover:text-neutral-100"
                        >
                            Link Check
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>
