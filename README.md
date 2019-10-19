<h1>#Getting started</h1>
<p>This is simple switch component, to make you UI simplest. Don't think about it, just use it.</p>

<img src="switch.png"/>

`npm i @pbartkowicz/vueswitch`

or

`yarn add @pbartkowicz/vueswitch`

<h1>#Usage</h1>
<p>Import module</p>

<pre>
<code>
import switcher from '@pbartkowicz/vueswitch'
</code>
</pre>

<p>Register</p>
<pre>
<code>
components:{
    switcher,
},
</code>
</pre>

<p>Use</p>
<pre>
<code>
&lt;switcher v-model="yourVariable"/&gt;
</code>
</pre>

<p>Switcher component operate on Boolean so input and output will be true/false. And that's it!</p>