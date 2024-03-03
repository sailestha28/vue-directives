<template>
    <section class="flex gap-1 flex-col" id="v-show">
        <h2 class="font-bold text-xl">
            3. v-show:
        </h2>
        <div>
            Toggle the element's visibility based on the truthy-ness of the expression value.
        </div>
        <div>
            <b>Expects</b>
            : any
        </div>
        <div>
            v-show works by setting the display CSS property via inline styles, and will try to respect the initial display value when the element is visible. It also triggers transitions when its
            condition changes.
        </div>
        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><code><span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-html</span><span
            style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">html</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span
            style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span></code></pre>
    </section>
</template>
<script setup lang="ts">


</script>
