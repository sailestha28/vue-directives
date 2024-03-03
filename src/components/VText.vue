<template>
    <section class="flex gap-1 flex-col" id="v-text">
        <h2 class="font-bold text-xl">
            1. v-text:
        </h2>
        <div>
            Update the element's text content.
        </div>
        <div>
            <b>Expects</b>
            : string
        </div>
        <div>
            v-text works by setting the element's textContent property, so it will overwrite any existing content inside the element
        </div>
        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><code><span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">span</span><span style="color:#B392F0;"> v-text</span><span
            style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">msg</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span
            style="color:#85E89D;">span</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- same as --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">span</span><span style="color:#E1E4E8;">&gt;&#123;&#123; msg }}&lt;/</span><span style="color:#85E89D;">span</span><span
    style="color:#E1E4E8;">&gt;</span></span></code></pre>
    </section>
</template>
<script setup lang="ts">

</script>
