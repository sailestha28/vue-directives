<template>
    <section class="flex gap-1 flex-col" id="v-for">
        <h2 class="font-bold text-xl">
            7. v-for:
        </h2>
        <div>
           Render the element or template block multiple times based on the source data.
        </div>
        <div>
            <b>Expects</b>
            : Array | Object | number | string | Iterable
        </div>
        <div>
           The directive's value must use the special syntax alias in expression to provide an alias for the current element being iterated on:
        </div>
        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><code><span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-for</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">item </span><span style="color:#F97583;">in</span><span style="color:#E1E4E8;"> items</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  &#123;&#123; item.text }}</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span style="color: white">Alternative</span>
 <span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-for</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">(item, index) </span><span style="color:#F97583;">in</span><span style="color:#E1E4E8;"> items</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-for</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">(value, key) </span><span style="color:#F97583;">in</span><span style="color:#E1E4E8;"> object</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-for</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">(value, name, index) </span><span style="color:#F97583;">in</span><span style="color:#E1E4E8;"> object</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span></code></pre>
    </section>
</template>
<script setup lang="ts">

</script>
