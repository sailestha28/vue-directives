<template>
    <section class="flex gap-1 flex-col" id="v-pre">
        <h2 class="font-bold text-xl">
            12. v-pre:
        </h2>
        <div>
          Skip compilation for this element and all its children.
        </div>
        <div>
            <b>Does not expect expression</b>

        </div>
        <div>
           Inside the element with v-pre, all Vue template syntax will be preserved and rendered as-is. The most common use case of this is displaying raw mustache tags.
        </div>
        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><code><span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">span</span><span style="color:#B392F0;"> v-pre</span><span style="color:#E1E4E8;">&gt;&#123;&#123; </span><span style="color:#79B8FF;">this</span><span style="color:#E1E4E8;"> will not be compiled }}&lt;/</span><span style="color:#85E89D;">span</span><span style="color:#E1E4E8;">&gt;</span></span></code></pre>
    </section>
</template>
<script setup lang="ts">


</script>
