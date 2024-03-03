<template>
    <section class="flex gap-1 flex-col" id="v-bind">
        <h2 class="font-bold text-xl">
            9. v-bind:
        </h2>
        <div>
Dynamically bind one or more attributes, or a component prop to an expression.
        </div>
              <div>
            <b>shorthand</b>
            : <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">:</span> or <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">.</span> (when using .prop modifier)
        </div>
        <div>
            <b>Modifiers</b>
            : any (with argument) | Object (without argument)
        </div>   <div>
            <b>Expects</b>
        :
        <br>
        <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">.camel </span>- transform the kebab-case attribute name into camelCase.
        <br> <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">.prop</span> - force a binding to be set as a DOM property. 3.2+
        <br> <span class="inline-block bg-gray-100 px-2 py-1 rounded-full">.attr</span> - force a binding to be set as a DOM attribute.
        </div>

        <div>
          When used to bind the class or style attribute, v-bind supports additional value types such as Array or Objects. See linked guide section below for more details.

When setting a binding on an element, Vue by default checks whether the element has the key defined as a property using an in operator check. If the property is defined, Vue will set the value as a DOM property instead of an attribute. This should work in most cases, but you can override this behavior by explicitly using .prop or .attr modifiers. This is sometimes necessary, especially when working with custom elements.
        </div>
        <pre class="bg-black rounded-lg overflow-hidden px-10 py-5"><code><span class="line"><span style="color:#6A737D;">&lt;!-- bind an attribute --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">img</span><span style="color:#B392F0;"> v-bind</span><span style="color:#E1E4E8;">:</span><span style="color:#B392F0;">src</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">imageSrc</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;"> /&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- dynamic attribute name --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">button</span><span style="color:#B392F0;"> v-bind:</span><span style="color:#E1E4E8;">[</span><span style="color:#B392F0;">key</span><span style="color:#E1E4E8;">]=</span><span style="color:#9ECBFF;">"value"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- shorthand --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">img</span><span style="color:#E1E4E8;"> :</span><span style="color:#B392F0;">src</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">imageSrc</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;"> /&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- same-name shorthand (3.4+), expands to :src="src" --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">img</span><span style="color:#E1E4E8;"> :</span><span style="color:#B392F0;">src</span><span style="color:#E1E4E8;"> /&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- shorthand dynamic attribute name --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;"> :[</span><span style="color:#B392F0;">key</span><span style="color:#E1E4E8;">]=</span><span style="color:#9ECBFF;">"value"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">button</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- with inline string concatenation --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">img</span><span style="color:#E1E4E8;"> :</span><span style="color:#B392F0;">src</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"'/path/to/images/'</span><span style="color:#F97583;"> +</span><span style="color:#E1E4E8;"> fileName</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;"> /&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- class binding --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;"> :</span><span style="color:#B392F0;">class</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">{ red: isRed }</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;"> :</span><span style="color:#B392F0;">class</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">[classA, classB]</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;"> :</span><span style="color:#B392F0;">class</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">[classA, { classB: isB, classC: isC }]</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- style binding --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;"> :</span><span style="color:#B392F0;">style</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">{ fontSize: size </span><span style="color:#F97583;">+</span><span style="color:#9ECBFF;"> 'px'</span><span style="color:#E1E4E8;"> }</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;"> :</span><span style="color:#B392F0;">style</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">[styleObjectA, styleObjectB]</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- binding an object of attributes --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">div</span><span style="color:#B392F0;"> v-bind</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">{ id: someProp, </span><span style="color:#9ECBFF;">'other-attr'</span><span style="color:#E1E4E8;">: otherProp }</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">div</span><span style="color:#E1E4E8;">&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- prop binding. "prop" must be declared in the child component. --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#79B8FF;">MyComponent</span><span style="color:#E1E4E8;"> :</span><span style="color:#B392F0;">prop</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">someThing</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;"> /&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- pass down parent props in common with a child component --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#79B8FF;">MyComponent</span><span style="color:#B392F0;"> v-bind</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">$props</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;"> /&gt;</span></span>
<span class="line"></span>
<span class="line"><span style="color:#6A737D;">&lt;!-- XLink --&gt;</span></span>
<span class="line"><span style="color:#E1E4E8;">&lt;</span><span style="color:#85E89D;">svg</span><span style="color:#E1E4E8;">&gt;&lt;</span><span style="color:#85E89D;">a</span><span style="color:#E1E4E8;"> :</span><span style="color:#B392F0;">xlink</span><span style="color:#E1E4E8;">:</span><span style="color:#B392F0;">special</span><span style="color:#E1E4E8;">=</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">foo</span><span style="color:#9ECBFF;">"</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">a</span><span style="color:#E1E4E8;">&gt;&lt;/</span><span style="color:#85E89D;">svg</span><span style="color:#E1E4E8;">&gt;</span></span></code></pre>
    </section>
</template>
<script setup lang="ts">

</script>
