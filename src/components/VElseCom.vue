<template>
    <section class="flex gap-1 flex-col" id="v-else">
        <h2 class="font-bold text-xl">
            5. v-else:
        </h2>
        <div>
           Denote the "else block" for v-if or a v-if / v-else-if chain.
        </div>
        <div>
            <b>Expects</b>
            :  Does not expect expression
        </div>
        <div>
          Can be used on <span><</span>template> to denote a conditional block containing only text or multiple elements.
        </div>
        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><code><span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-if</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">Math.</span><span style="color:#B392F0;">random</span><span style="color:#E1E4E8;">() </span><span style="color:#F97583;">&gt;</span><span style="color:#79B8FF;"> 0.5</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  Now you see me</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-else</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  Now you don't</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span></code></pre>
    </section>
</template>
<script setup lang="ts">


</script>
