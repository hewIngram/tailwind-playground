<template>
    <div class="flex flex-col bg-indigo-700 text-white h-screen text-3xl">
        <div
            :class="{
                'py-5': true,
                'px-8': true,
                'opacity-25': isActive('home'),
                'hover:opacity-75': true,
                'cursor-pointer': true,
            }"
        >
            <FontAwesomeIcon :icon="homeIcon" fixed-width />
        </div>
        <div
            :class="{
                'py-5': true,
                'px-8': true,
                'opacity-25': isActive('folder'),
                'hover:opacity-75': true,
                'cursor-pointer': true,
            }"
        >
            <FontAwesomeIcon :icon="folderIcon" fixed-width />
        </div>
        <div
            :class="{
                'py-5': true,
                'px-8': true,
                'opacity-25': isActive('clock'),
                'hover:opacity-75': true,
                'cursor-pointer': true,
            }"
        >
            <FontAwesomeIcon :icon="clockIcon" fixed-width />
        </div>
        <div
            :class="{
                'py-5': true,
                'px-8': true,
                'opacity-25': isActive('documentation'),
                'hover:opacity-75': true,
                'cursor-pointer': true,
            }"
        >
            <FontAwesomeIcon :icon="bookIcon" fixed-width />
        </div>
        <div
            :class="{
                'py-5': true,
                'px-8': true,
                'opacity-25': isActive('settings'),
                'hover:opacity-75': true,
                'cursor-pointer': true,
            }"
        >
            <FontAwesomeIcon :icon="settingsIcon" fixed-width />
        </div>
        <div
            :class="{
                'py-5': true,
                'px-8': true,
                'opacity-25': isActive('settings'),
                'hover:opacity-75': true,
                'cursor-pointer': true,
                'mt-auto': true
            }"
        >
            <FontAwesomeIcon :icon="signOutIcon" fixed-width />
        </div>
    </div>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import {
    faHome,
    faBookOpen,
    faFolder,
    faCog,
    faClock,
    faSignOutAlt,
} from '@fortawesome/free-solid-svg-icons'

export default {
    name: 'Sidebar',
    components: {
        FontAwesomeIcon,
    },
    computed: {
        homeIcon() {
            return faHome
        },
        folderIcon() {
            return faFolder
        },
        bookIcon() {
            return faBookOpen
        },
        settingsIcon() {
            return faCog
        },
        clockIcon() {
            return faClock
        },
        signOutIcon() {
            return faSignOutAlt
        },
    },
    methods: {
        isActive(routeName) {
            return routeName !== 'home'
        },
    },
}
</script>
