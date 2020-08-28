<template>
    <div class="flex justify-between px-16 py-8 items-center">
        <div>
            <div
                class="border border-gray-400 bg-gray-200 rounded-full px-8 py-3 focus-within:border-teal-500 focus-within:border-4"
            >
                <FontAwesomeIcon :icon="searchIcon" fixed-width class="text-gray-400" />
                <input class="bg-gray-200 ml-4 outline-none w-64" placeholder="Search" />
            </div>
        </div>
        <div class="flex items-center text-xl">
            <FontAwesomeIcon :icon="calendarIcon" fixed-width class="mr-6" />
            <p>10 May - 23 June</p>
        </div>
        <div class="flex items-center text-xl">
            <FontAwesomeIcon :icon="bellIcon" fixed-width class="mr-4" />
            <img
                class="rounded-full w-16 mr-6"
                src="https://avatars3.githubusercontent.com/u/499550?s=460&u=de41ec9325e8a92e281b96a1514a0fd1cd81ad4a&v=4"
            />
            <p>John Alby</p>
            <FontAwesomeIcon :icon="chevronIcon" fixed-width class="ml-4" />
        </div>
    </div>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faSearch, faUser, faChevronDown, faBell, faCalendar } from '@fortawesome/free-solid-svg-icons'

export default {
    name: 'Header',
    components: {
        FontAwesomeIcon,
    },
    computed: {
        searchIcon() {
            return faSearch
        },
        userIcon() {
            return faUser
        },
        chevronIcon() {
            return faChevronDown
        },
        bellIcon() {
            return faBell
        },
        calendarIcon() {
            return faCalendar
        }
    },
}
</script>
