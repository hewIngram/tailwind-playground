<template>
    <div class="flex flex-col text-xl text-gray-700 bg-white h-screen py-8 px-16">
        <div
            class="flex  items-center text-3xl font-bold py-10 text-gray-900 self-start justify-between w-64"
        >
            <p>Projects</p>
            <div
                style="background-color: #4C51BF"
                class="text-m bg-blue rounded-full h-12 w-12 flex items-center justify-center text-white"
            >
                <FontAwesomeIcon :icon="plusIcon" fixed-width />
            </div>
        </div>
        <div class="flex items-center py-4 justify-between w-64">
            <span class="flex items-center"
                ><FontAwesomeIcon :icon="archiveIcon" fixed-width class="mr-4" />
                <p>All projects</p></span
            >
            <FontAwesomeIcon :icon="chevronIcon" fixed-width />
        </div>
        <div class="flex items-center py-4 justify-between w-64">
            <span class="flex items-center"
                ><FontAwesomeIcon :icon="paperclipIcon" fixed-width class="mr-4" />
                <p>Pinned</p></span
            >
            <FontAwesomeIcon :icon="chevronIcon" fixed-width />
        </div>
        <div class="flex items-center py-4 justify-between w-64">
            <span class="flex items-center"
                ><FontAwesomeIcon :icon="chartIcon" fixed-width class="mr-4" />
                <p>In process</p></span
            >
            <FontAwesomeIcon :icon="chevronIcon" fixed-width />
        </div>
        <div class="flex items-center py-4 justify-between w-64">
            <span class="flex items-center"
                ><FontAwesomeIcon :icon="check" fixed-width class="mr-4" />
                <p>Done</p></span
            >
            <FontAwesomeIcon :icon="chevronIcon" fixed-width />
        </div>
    </div>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import {
    faArchive,
    faPaperclip,
    faChartPie,
    faCheckCircle,
    faChevronRight,
    faPlus,
} from '@fortawesome/free-solid-svg-icons'

export default {
    name: 'Navebar',
    components: {
        FontAwesomeIcon,
    },
    computed: {
        archiveIcon() {
            return faArchive
        },
        paperclipIcon() {
            return faPaperclip
        },
        chartIcon() {
            return faChartPie
        },
        check() {
            return faCheckCircle
        },
        chevronIcon() {
            return faChevronRight
        },
        plusIcon() {
            return faPlus
        },
    },
}
</script>
