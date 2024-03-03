<template>
    <section class="flex gap-1 flex-col" id="v-modal">
        <h2 class="font-bold text-xl">
            10. v-modal:
        </h2>
        <div>
           Create a two-way binding on a form input element or a component.
        </div>
        <div>
            <b>Expects</b>
            : varies based on value of form inputs element or output of components
        </div>
        <div>
            <b>Limited to:</b>
           <ul class="list-disc"><li><code>&lt;input&gt;</code></li><li><code>&lt;select&gt;</code></li><li><code>&lt;textarea&gt;</code></li><li>components</li></ul>
        </div>
        <div>
            <b>Modifiers:</b>
           <ul><li><code>.lazy</code> - listen to <code>change</code> events instead of <code>input</code></li><li><code>.number</code> - cast valid input string to numbers</li><li><code>.trim</code> - trim input</li></ul>
        </div>

        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><code><span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">input</span><span style="color:#B392F0;"> v-model</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">text</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">textarea</span><span style="color:#B392F0;"> v-model</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">message</span><span style="color:#9ECBFF;">"</span><span style="color:#B392F0;"> placeholder</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"add multiple lines"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">textarea</span><span style="color:#E1E4E8;">&gt;</span></span><span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;Selected: {{ selected }}&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">select</span><span style="color:#B392F0;"> v-model</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">selected</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  &lt;</span><span style="color:#85E89D;">option</span><span style="color:#B392F0;"> disabled</span><span style="color:#B392F0;"> value</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">""</span><span style="color:#E1E4E8;">&gt;Please select one&lt;/</span><span style="color:#85E89D;">option</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  &lt;</span><span style="color:#85E89D;">option</span><span style="color:#E1E4E8;">&gt;A&lt;/</span><span style="color:#85E89D;">option</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  &lt;</span><span style="color:#85E89D;">option</span><span style="color:#E1E4E8;">&gt;B&lt;/</span><span style="color:#85E89D;">option</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">  &lt;</span><span style="color:#85E89D;">option</span><span style="color:#E1E4E8;">&gt;C&lt;/</span><span style="color:#85E89D;">option</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;/</span><span style="color:#85E89D;">select</span><span style="color:#E1E4E8;">&gt;</span></span></code>
       </pre>
    </section>
</template>
<script setup lang="ts">


</script>
