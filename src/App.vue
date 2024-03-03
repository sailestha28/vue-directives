<template>
    <div class="max-w-[1280px] mx-auto mt-[2.5%]">
        <div class="flex gap-10">
            <div class="shrink-0 w-40 ">
                <ul class="sticky top-3 w-full space-y-1">
                    <li v-for="(item,i) in menu" :key="i">
                        <a class="text-green-600" :href="`#${item}`">
                            {{ i + 1 }}. {{ item }}
                        </a>

                    </li>
                </ul>
            </div>
            <div class="min-w-0 jb-w-full space-y-10">
                <VText/>
                <VHtml/>
                <VShow/>
                <VIfCom/>
                <VElseCom/>
                <VElseIfCom/>
                <VFor/>
                <VOnComp/>
                <VBind/>
                <VModelComp/>
                <VSlot/>
                <VPre/>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">

    import VBind from "./components/VBind.vue"
    import VElseCom from "./components/VElseCom.vue"
    import VElseIfCom from "./components/VElseIfCom.vue"
    import VFor from "./components/VFor.vue"
    import VHtml from "./components/VHtml.vue"
    import VIfCom from "./components/VIfCom.vue"
    import VModelComp from "./components/VModelComp.vue"
    import VOnComp from "./components/VOnComp.vue"
    import VPre from "./components/VPre.vue"
    import VShow from "./components/VShow.vue"
    import VSlot from "./components/VSlot.vue"
    import VText from "./components/VText.vue"

    const menu = [
        "v-text",
        "v-html",
        "v-show",
        "v-if",
        "v-else",
        "v-else-if",
        "v-for",
        "v-on",
        "v-bind",
        "v-model",
        "v-slot",
        "v-pre",
        "v-once",
        "v-memo",
        "v-cloak",

    ]
</script>
