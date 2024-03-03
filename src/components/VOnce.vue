<template>
    <section class="flex gap-1 flex-col" id="v-once">
        <h2 class="font-bold text-xl">
            13. v-once:
        </h2>
        <div>
        Render the element and component once only, and skip future updates.
        </div>
        <div>
            <b>Does not expect expression</b>
        </div>
        <div>
           On subsequent re-renders, the element/component and all its children will be treated as static content and skipped. This can be used to optimize update performance.
        </div>
        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><<code><span class="line"><span style="color:#6A737D;">&lt;!-- single element --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">span</span><span style="color:#B392F0;"> v-once</span><span style="color:#E1E4E8;">&gt;This will never change: {{msg}}&lt;/</span><span style="color:#85E89D;">span</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- the element have children --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-once</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  &lt;</span><span style="color:#85E89D;">h1</span><span style="color:#E1E4E8;">&gt;comment&lt;/</span><span style="color:#85E89D;">h1</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  &lt;</span><span style="color:#85E89D;">p</span><span style="color:#E1E4E8;">&gt;&#123;&#123;msg}}&lt;/</span><span style="color:#85E89D;">p</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- component --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#79B8FF;">MyComponent</span><span style="color:#B392F0;"> v-once</span><span style="color:#E1E4E8;"> :</span><span style="color:#B392F0;">comment</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">msg</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#79B8FF;">MyComponent</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- `v-for` directive --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">ul</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  &lt;</span><span style="color:#85E89D;">li</span><span style="color:#B392F0;"> v-for</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">i </span><span style="color:#F97583;">in</span><span style="color:#E1E4E8;"> list</span><span style="color:#9ECBFF;">"</span><span style="color:#B392F0;"> v-once</span><span style="color:#E1E4E8;">&gt;{{i}}&lt;/</span><span style="color:#85E89D;">li</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;/</span><span style="color:#85E89D;">ul</span><span style="color:#E1E4E8;">&gt;</span></span></code></pre>
    </section>
</template>
<script setup lang="ts">


</script>
