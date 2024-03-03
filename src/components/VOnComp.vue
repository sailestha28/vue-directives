<template>
    <section class="flex gap-1 flex-col" id="v-on">
        <h2 class="font-bold text-xl">
            8. v-on:
        </h2>
        <div>
            Attach an event listener to the element.
        </div>
        <div>
            <b>Shorthand</b>
            : @
        </div>
        <div>
            <b>Expects</b>
            : Function | Inline Statement | Object (without argument)
        </div>
        <div>
            <b>Modifiers</b>
            :
            <br>
            <span class="inline-block bg-gray-100 px-2 py-1 rounded-full"> .stop </span>
            - call event.stopPropagation().
            <br>
            <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">     .prevent</span>
            - call event.preventDefault().
            <br>
             <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">    .capture</span>- add event listener in capture mode.
            <br>
                 <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">   .self</span> - only trigger handler if event was dispatched from this element.
            <br>
                 <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">    .{keyAlias}</span> - only trigger handler on certain keys.
            <br>
                 <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">   .once </span>- trigger handler at most once.
            <br>
                 <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">   .left </span>- only trigger handler for left button mouse events.
            <br>
                 <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">   .right</span> - only trigger handler for right button mouse events.
            <br>
                 <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">   .middle </span>- only trigger handler for middle button mouse events.
            <br>
                 <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">   .passive</span> - attaches a DOM event with { passive: true }.
        </div>
        <div>
            v-show works by setting the display CSS property via inline styles, and will try to respect the initial display value when the element is visible. It also triggers transitions when its
            condition changes.
        </div>
        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><code><span class="line"><span style="color:#6A737D;">&lt;!-- method handler --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">button</span><span style="color:#B392F0;"> v-on</span><span style="color:#E1E4E8;">:</span><span style="color:#B392F0;">click</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">doThis</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- dynamic event --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">button</span><span style="color:#B392F0;"> v-on:</span><span style="color:#E1E4E8;">[</span><span style="color:#B392F0;">event</span><span style="color:#E1E4E8;">]=</span><span style="color:#9ECBFF;">"doThis"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- inline statement --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">button</span><span style="color:#B392F0;"> v-on</span><span style="color:#E1E4E8;">:</span><span style="color:#B392F0;">click</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#B392F0;">doThat</span><span style="color:#E1E4E8;">(</span><span style="color:#9ECBFF;">'hello'</span><span style="color:#E1E4E8;">, $event)</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- shorthand --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;"> @</span><span style="color:#B392F0;">click</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">doThis</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- shorthand dynamic event --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;"> @[</span><span style="color:#B392F0;">event</span><span style="color:#E1E4E8;">]=</span><span style="color:#9ECBFF;">"doThis"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- stop propagation --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;"> @</span><span style="color:#B392F0;">click</span><span style="color:#E1E4E8;">.</span><span style="color:#B392F0;">stop</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">doThis</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- prevent default --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;"> @</span><span style="color:#B392F0;">click</span><span style="color:#E1E4E8;">.</span><span style="color:#B392F0;">prevent</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">doThis</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- prevent default without expression --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">form</span><span style="color:#E1E4E8;"> @</span><span style="color:#B392F0;">submit</span><span style="color:#E1E4E8;">.</span><span style="color:#B392F0;">prevent</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">form</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- chain modifiers --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;"> @</span><span style="color:#B392F0;">click</span><span style="color:#E1E4E8;">.stop.</span><span style="color:#B392F0;">prevent</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">doThis</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- key modifier using keyAlias --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">input</span><span style="color:#E1E4E8;"> @</span><span style="color:#B392F0;">keyup</span><span style="color:#E1E4E8;">.</span><span style="color:#B392F0;">enter</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">onEnter</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;"> /&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- the click event will be triggered at most once --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">button</span><span style="color:#B392F0;"> v-on</span><span style="color:#E1E4E8;">:</span><span style="color:#B392F0;">click</span><span style="color:#E1E4E8;">.</span><span style="color:#B392F0;">once</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">doThis</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- object syntax --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">button</span><span style="color:#B392F0;"> v-on</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">{ mousedown: doThis, mouseup: doThat }</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;">&gt;</span></span></code>
 <code>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#79B8FF;">MyComponent</span><span style="color:#E1E4E8;"> @</span><span style="color:#B392F0;">my-event</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">handleThis</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;"> /&gt;</span></span>
<span class="line"></span><span class="line"><span style="color:#6A737D;">&lt;!-- inline statement --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#79B8FF;">MyComponent</span><span style="color:#E1E4E8;"> @</span><span style="color:#B392F0;">my-event</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#B392F0;">handleThis</span><span style="color:#E1E4E8;">(</span><span style="color:#79B8FF;">123</span><span style="color:#E1E4E8;">, $event)</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;"> /&gt;</span></span></code></pre>
    </section>
</template>
<script setup lang="ts">


</script>
