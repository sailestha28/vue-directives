<template>
    <section class="flex gap-1 flex-col" id="v-memo">
        <h2 class="font-bold text-xl">
            14. v-memo:
        </h2>
        <div>
            <b>Expects</b>
            : any
        </div>
        <div>
            Memoize a sub-tree of the template. Can be used on both elements and components. The directive expects a fixed-length array of dependency values to compare for the memoization. If every
            value in the array was the same as last render, then updates for the entire sub-tree will be skipped.
        </div>
        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><code><span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-memo</span><span
            style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">[valueA, valueB]</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  ...</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span></code></pre>
        <div>
            When the component re-renders, if both valueA and valueB remain the same, all updates for this
            <div> and its children will be skipped. In fact, even the Virtual DOM VNode creation will also be skipped since the memoized copy of the sub-tree can be reused.
            </div>
        </div>
    </section>
</template>
<script setup lang="ts">


</script>
