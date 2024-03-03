<template>
    <section class="flex gap-1 flex-col" id="v-cloak">
        <h2 class="font-bold text-xl">
            15. v-cloak:
        </h2>
        <div>
            Used to hide un-compiled template until it is ready.
        </div>
        <div>
            <b>Does not expect expression</b>
        </div>
        <div>
            This directive is only needed in no-build-step setups.

            When using in-DOM templates, there can be a "flash of un-compiled templates": the user may see raw mustache tags until the mounted component replaces them with rendered content.
            <br>
            v-cloak will remain on the element until the associated component instance is mounted. Combined with CSS rules such as [v-cloak] { display: none }, it can be used to hide the raw templates
            until the component is ready.
        </div>
        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><code><span class="line"><span style="color:#E1E4E8;">[</span><span style="color:#B392F0;">v-cloak</span><span style="color:#E1E4E8;">] {</span></span>
<span class="line"><span style="color:#79B8FF;">  display</span><span style="color:#E1E4E8;">: </span><span style="color:#79B8FF;">none</span><span style="color:#E1E4E8;">;</span></span>
<span class="line"><span style="color:#E1E4E8;">}</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-cloak</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">   &#123;&#123; message }}</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span></code></pre>
    </section>
</template>
<script setup lang="ts">


</script>
