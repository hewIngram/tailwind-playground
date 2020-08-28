<template>
    <div class="flex bg-gray-100" >
        <Sidebar />
        <Navbar />
        <main class="flex flex-col w-full">
            <Header />
            <div>
                Router content
            </div>
        </main>
    </div>
</template>

<script>
import Sidebar from '@/components/Sidebar.vue'
import Navbar from '@/components/Navbar.vue'
import Header from '@/components/Header.vue'

export default {
    name: 'Home',
    components: {
        Sidebar,
        Navbar,
        Header,
    },
}
</script>
