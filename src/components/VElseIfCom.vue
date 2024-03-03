<template>
    <section class="flex gap-1 flex-col" id="v-else-if">
        <h2 class="font-bold text-xl">
            6. v-else-if:
        </h2>
        <div>
         Denote the "else if block" for v-if. Can be chained.
        </div>
        <div>
            <b>Expects</b>
            :  any
        </div>
        <div>
          Restriction: previous sibling element must have v-if or v-else-if.
            <br>
            Can be used on <span><</span>template> to denote a conditional block containing only text or multiple elements.
        </div>
        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><code><span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-if</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">type </span><span style="color:#F97583;">===</span><span style="color:#9ECBFF;"> 'A'"</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  A</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-else-if</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">type </span><span style="color:#F97583;">===</span><span style="color:#9ECBFF;"> 'B'"</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  B</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-else-if</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">type </span><span style="color:#F97583;">===</span><span style="color:#9ECBFF;"> 'C'"</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  C</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-else</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  Not A/B/C</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span></code></pre>
    </section>
</template>
<script setup lang="ts">


</script>
