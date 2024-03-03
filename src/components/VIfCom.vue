<template>
    <section class="flex gap-1 flex-col" id="v-if">
        <h2 class="font-bold text-xl">
            4. v-if:
        </h2>
        <div>
            Conditionally render an element or a template fragment based on the truthy-ness of the expression value.
        </div>
        <div>
            <b>Expects</b>
            : any
        </div>
        <div>
          When a v-if element is toggled, the element and its contained directives / components are destroyed and re-constructed. If the initial condition is falsy, then the inner content won't be rendered at all.

Can be used on <span><</span>template> to denote a conditional block containing only text or multiple elements.

This directive triggers transitions when its condition changes.

When used together, v-if has a higher priority than v-for. We don't recommend using these two directives together on one element — see the list rendering guide for details.
        </div>
        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><code><span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-if</span><span
            style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">if</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span
            style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span></code></pre>
    </section>
</template>
<script setup lang="ts">


</script>
