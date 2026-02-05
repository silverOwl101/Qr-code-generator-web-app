<template>
    <div class="flex items-center justify-center min-h-screen bg-gray-650">
        <UCard class="w-full max-w-md shadow-xl border border-gray-800">
            <template #header>
                <div class="flex items-center justify-between">
                    <span class="text-lg font-semibold text-white/60">QR Code Generator</span>
                </div>
            </template>
            <div class="flex flex-col gap-6 py-4">
                <UInput v-model="qrInput" placeholder="Enter text to generate QR code" size="lg" class="w-full"
                    icon="i-heroicons-pencil-square" autofocus />
                <div class="flex justify-center">
                    <Qrcode :value="qrInput" class="w-48 h-48 rounded-lg border border-gray-200" />
                </div>
            </div>
            <template #footer>
                <div class="text-[10px] text-gray-500 text-center">Powered by Nuxt UI & QRCode</div>
                <div class="text-xs text-gray-500 text-center">Made by John Harold Paluca</div>
            </template>
        </UCard>
    </div>
</template>

<script lang="ts" setup>
const qrInput = ref('')
</script>