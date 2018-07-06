---


---

<h1 id="html">1. Html</h1>
<h2 id="кавычки-в-html">1.1 Кавычки в <code>html</code></h2>
<p>В <code>html</code> всегда использовать двойные кавычки(<code>"</code>)</p>
<p><strong>Мотивация:</strong> Код становиться более однородным и лучше воспринимаеться визуально.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token comment">&lt;!-- wrong --&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">'</span>class-name<span class="token punctuation">'</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>

<span class="token comment">&lt;!-- right --&gt;</span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>class-name<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<h2 id="порядок-атрибутов">Порядок атрибутов</h2>
<p>Сортирока атрибутов по важности. Первый - обязательно <code>class</code>.  Последними идут атрибуты, которые исползуются для <code>js</code>.</p>
<p><strong>Мотивация:</strong> Позволяет визуально отделить верстку елемента, от остальных его функции.</p>
<pre><code>1. class
2. id
3. type, value, href ...
4. data
</code></pre>
<pre class=" language-html"><code class="prism  language-html">// wrong
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>email<span class="token punctuation">"</span></span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>list list--highlited<span class="token punctuation">"</span></span> <span class="token attr-name">data-role</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>email-input<span class="token punctuation">"</span></span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>email<span class="token punctuation">"</span></span> <span class="token punctuation">/&gt;</span></span>
// right
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>list list--highlited<span class="token punctuation">"</span></span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>email<span class="token punctuation">"</span></span>  <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>email<span class="token punctuation">"</span></span> <span class="token attr-name">data-role</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>email-input<span class="token punctuation">"</span></span> <span class="token punctuation">/&gt;</span></span>
</code></pre>
<h2 id="перенос-атрибутов-на-новую-строчку">Перенос атрибутов на новую строчку</h2>
<p>Когда строка с тегом из-за большого числа аттрибутов, становиться слишком длинной, стоит переносить атрибуты на новую строчку. Первый всегда остается на одной строчке с тегом, остальные выравниваются по нему слева. Стоит придерживаться однородности, если, хотя бы один аттрибут перенесен - все остальные тоже быть с новой строчки. Закрывающая скобочка тега, толжна быть обязательно с новой строчки и выровняна по открывающей.</p>
<p><strong>Мотивация:</strong> Ускаряет визуальны поиск нужного атрибута, плюс помогает избежать горизонтального скрола в редакторе.</p>
<pre class=" language-html"><code class="prism  language-html">// wrong 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span>
    <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>wrong-div<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>text<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>

// right
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>wrong-div<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>text<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
// or 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>wrong-div<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
    text
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
// wrong
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>email<span class="token punctuation">"</span></span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>list list--highlited<span class="token punctuation">"</span></span> 
    <span class="token attr-name">data-role</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>email-input<span class="token punctuation">"</span></span> <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>email<span class="token punctuation">"</span></span> <span class="token punctuation">/&gt;</span></span>
// right
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>list list--highlited<span class="token punctuation">"</span></span> 
       <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>email<span class="token punctuation">"</span></span>  
       <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>email<span class="token punctuation">"</span></span> 
       <span class="token attr-name">data-role</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>email-input<span class="token punctuation">"</span></span>
<span class="token punctuation">/&gt;</span></span>
// wrong 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>wrong-div<span class="token punctuation">"</span></span> 
     <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>div<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
     text
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
// right 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>wrong-div<span class="token punctuation">"</span></span> 
     <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>div<span class="token punctuation">"</span></span>
<span class="token punctuation">&gt;</span></span>
    text
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<h1 id="styles">2. Styles</h1>
<h2 id="кавычки">Кавычки</h2>
<p>Всегда испольновать одинарные кавычки (<code>'</code>)</p>
<p><strong>Мотивация:</strong> Код становиться более однородным и лучше воспринимаеться визуально.</p>
<pre class=" language-scss"><code class="prism  language-scss"><span class="token comment">/* wrong */</span>
<span class="token selector">.block </span><span class="token punctuation">{</span>
	 <span class="token property">background</span><span class="token punctuation">:</span> <span class="token url">url</span><span class="token punctuation">(</span><span class="token string">"/now-banner.png"</span><span class="token punctuation">)</span> no-repeat<span class="token punctuation">;</span> 
	 <span class="token selector"><span class="token parent important">&amp;</span>:before </span><span class="token punctuation">{</span>
		<span class="token property">content</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>

<span class="token comment">/* right */</span>
<span class="token selector">.block </span><span class="token punctuation">{</span>
	 <span class="token property">background</span><span class="token punctuation">:</span> <span class="token url">url</span><span class="token punctuation">(</span><span class="token string">'/now-banner.png'</span><span class="token punctuation">)</span> no-repeat<span class="token punctuation">;</span> 
	 
	 <span class="token selector"><span class="token parent important">&amp;</span>:before </span><span class="token punctuation">{</span>
		<span class="token property">content</span><span class="token punctuation">:</span> <span class="token string">''</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="пробелы">Пробелы</h2>
<p>Обязательные пробелы после селектора, свойства и запятых в значениях свойств. Отделять блоки свойств и сложенные слекторы одной пустой строчкой.</p>
<p><strong>Мотивация:</strong> Код становиться однородным и лучше воспринимаеться визуально.</p>
<pre class=" language-scss"><code class="prism  language-scss"><span class="token comment">/* wrong */</span>
<span class="token selector">.main-logo-block </span><span class="token punctuation">{</span>  
  <span class="token property">float</span><span class="token punctuation">:</span> left<span class="token punctuation">;</span>   
  <span class="token selector">a </span><span class="token punctuation">{</span>  
	<span class="token property">display</span><span class="token punctuation">:</span>block<span class="token punctuation">;</span>  
  <span class="token punctuation">}</span>  
  <span class="token selector">span</span><span class="token punctuation">{</span>  
    <span class="token property">display</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span>  
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
<span class="token comment">/* right */</span>
<span class="token selector">.main-logo-block </span><span class="token punctuation">{</span>  
  <span class="token property">float</span><span class="token punctuation">:</span> left<span class="token punctuation">;</span>   
  
  <span class="token selector">a </span><span class="token punctuation">{</span>  
	<span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span>  
  <span class="token punctuation">}</span> 
   
  <span class="token selector">span </span><span class="token punctuation">{</span>  
    <span class="token property">display</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span>  
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="задание-цвета">Задание цвета</h2>
<p>Успользовать только полные версии для <code>hex</code> варианта и только в нижнем регистре, не использовать строковые аналоги.</p>
<p><strong>Мотивация:</strong> Улучшает читаемость кода</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector"><span class="token class">.block</span> </span><span class="token punctuation">{</span>
	<span class="token comment">/* wrong */</span>
	<span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#FFF</span><span class="token punctuation">;</span>
	<span class="token property">color</span><span class="token punctuation">:</span> white<span class="token punctuation">;</span>
	<span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#FFFFFF</span><span class="token punctuation">;</span>
	<span class="token comment">/* right */</span>
	<span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#ffffff</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="указание-единицы-измерения">Указание единицы измерения</h2>
<p>Если для слектора указываеться свойство в котором несколько значений (например <code>margin: 0px 5px</code>), то оябзательно указывать единицу измерения для <code>0</code>.</p>
<p><strong>Мотивация:</strong> Значение лучше вопринимается визуально, плюс меньше движений нужно для изменения нуля на другое число.</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token comment">/* wrong */</span>
<span class="token selector"><span class="token class">.block</span> </span><span class="token punctuation">{</span>
	<span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span> <span class="token number">5</span>px<span class="token punctuation">;</span>
	<span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>rem <span class="token number">0</span> <span class="token number">5</span>rem<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token comment">/* right */</span>
<span class="token selector"><span class="token class">.block</span> </span><span class="token punctuation">{</span>
	<span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span>px <span class="token number">5</span>px<span class="token punctuation">;</span>
	<span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>rem <span class="token number">0</span>rem <span class="token number">5</span>rem<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="сортировка-свойств">Сортировка свойств</h2>
<ol>
<li>*-top</li>
<li>*-right</li>
<li>*-bottom</li>
<li>*-left</li>
</ol>
<p><strong>Мотивация:</strong> Ускоряет визуальный поиск нужного свойства</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token comment">/* right */</span>
<span class="token selector"><span class="token class">.block</span> </span><span class="token punctuation">{</span>
	<span class="token property">top</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span>
	<span class="token property">right</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span>
	<span class="token property">bottom</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span>
	<span class="token property">left</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span>
	
    <span class="token property">margin-top</span><span class="token punctuation">:</span> <span class="token number">10</span>px<span class="token punctuation">;</span>
    <span class="token property">margin-left</span><span class="token punctuation">:</span> <span class="token number">20</span>px<span class="token punctuation">;</span>

	<span class="token property">border-right</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#c0c0c0</span><span class="token punctuation">;</span>
	<span class="token property">border-bottom</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#c0c0c0</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="обязательные-кавычки-в-url">Обязательные кавычки в <code>url</code></h2>
<pre class=" language-css"><code class="prism  language-css"><span class="token comment">/* wrong */</span>
<span class="token property">background</span><span class="token punctuation">:</span> <span class="token url">url(/now-banner.png)</span> no-repeat<span class="token punctuation">;</span>
<span class="token property">background</span><span class="token punctuation">:</span> <span class="token url">url("/now-banner.png")</span> no-repeat<span class="token punctuation">;</span>
<span class="token comment">/* right */</span>
<span class="token property">background</span><span class="token punctuation">:</span> <span class="token url">url('/now-banner.png')</span> no-repeat<span class="token punctuation">;</span>
</code></pre>
<h2 id="стилизация-тегов">Стилизация тегов</h2>
<p>Стараться не стилизировать вложенные в классы теги. Исключением может быть стилизирование <code>img</code> внутри контейнера или задание стилей для текстов из, которые приходят из бекенда</p>
<p><strong>Мотивация:</strong> Разметка может меняться и добавления тега может привести к не ожидаемому применению стилей к нему.</p>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>form<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
	<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>form__password-input<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>form</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<pre class=" language-scss"><code class="prism  language-scss"><span class="token comment">/* wrong */</span>
<span class="token selector">.form </span><span class="token punctuation">{</span>
	<span class="token selector">input </span><span class="token punctuation">{</span>
		<span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#c0c0c0</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
<span class="token comment">/* right */</span>
<span class="token selector">.form </span><span class="token punctuation">{</span>
	<span class="token selector"><span class="token parent important">&amp;</span>__password-input </span><span class="token punctuation">{</span>
		<span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#c0c0c0</span><span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
<span class="token comment">/* right */</span>
<span class="token selector">.tournament__image </span><span class="token punctuation">{</span>
	<span class="token selector">img </span><span class="token punctuation">{</span>
		<span class="token property">display</span><span class="token punctuation">:</span> block<span class="token punctuation">;</span>
		<span class="token property">amrgin</span><span class="token punctuation">:</span> <span class="token number">0</span>px auto<span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="bem">BEM</h2>
<h3 id="названия-классов">Названия классов</h3>
<p>Слова в названиях классов отделяются одинарным дефисом <code>-</code> и пишутся в нижнем регистре.</p>
<pre class=" language-css"><code class="prism  language-css">    <span class="token selector"><span class="token class">.class</span> </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    <span class="token selector"><span class="token class">.three-words-class</span></span><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<h3 id="block">Block</h3>
<p>В общем случае, блок не должен содержать внешних отступов и позиционирования (<code>margin</code>, <code>top</code> …).</p>
<pre class=" language-css"><code class="prism  language-css">    <span class="token selector"><span class="token class">.block</span> </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    <span class="token selector"><span class="token class">.three-words-block</span> </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>Блок отделяется от элемента двумя подчеркиваниями <code>__</code></p>
<h3 id="element">Element</h3>
<pre class=" language-css"><code class="prism  language-css">    <span class="token selector"><span class="token class">.block__element</span> </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    <span class="token selector"><span class="token class">.block__another-element</span> </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    <span class="token selector"><span class="token class">.long-block__long-element</span> </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>Модификатор отделяется двойным дефисом <code>--</code></p>
<h3 id="modifier">Modifier</h3>
<pre class=" language-css"><code class="prism  language-css">    <span class="token selector"><span class="token class">.block--modifier</span> </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    <span class="token selector"><span class="token class">.block--is-visible</span> </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    <span class="token selector"><span class="token class">.block__element--modifier</span> </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<pre class=" language-html"><code class="prism  language-html"><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>form</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>promocode promocode--activated<span class="token punctuation">"</span></span> 
	  <span class="token attr-name">action</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>/promocode<span class="token punctuation">"</span></span> 
	  <span class="token attr-name">method</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>POST<span class="token punctuation">"</span></span>
<span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>promocode__inner<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>input</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>promocode__input<span class="token punctuation">"</span></span> <span class="token attr-name">value</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span><span class="token punctuation">"</span></span> <span class="token punctuation">/&gt;</span></span>
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">class</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>promocode__btn promocode__btn--disabled<span class="token punctuation">"</span></span>
                <span class="token attr-name">type</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>submit<span class="token punctuation">"</span></span>
        <span class="token punctuation">&gt;</span></span>
            Submit
        <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>div</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<h2 id="состояние">Состояние</h2>
<p>Для псевдоклассов, которые определяю состояние блока(<code>:hover</code>) желательно делать модификатор, с теми же свойствами.</p>
<p><strong>Мотивация:</strong> Дает возможность отобразить блок в нужном состоянии, не использую инспектор, просто добавив соответствующий модификатор</p>
<pre class=" language-scss"><code class="prism  language-scss">
<span class="token selector">.block </span><span class="token punctuation">{</span>
	<span class="token property">text-decoration</span><span class="token punctuation">:</span> none<span class="token punctuation">;</span>
	
	<span class="token selector"><span class="token parent important">&amp;</span>:hover,
	<span class="token parent important">&amp;</span>--is-hover </span><span class="token punctuation">{</span>
		<span class="token property">text-decoration</span><span class="token punctuation">:</span> underline<span class="token punctuation">;</span>
	<span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="properties-groups">Properties groups</h2>
<p>Свойства, необходимо бить на группы, разделенные одной пустой строкой, и придерживаться порядка:</p>
<pre><code>1. display block
2. box-size block
3. position block
4. background block
5. font block
</code></pre>
<p><strong>Мотивация</strong>: чаще всего, при изменении элемента, нужно модифицировать одни и те же свойства(<code>margin</code>, <code>top</code>, <code>color</code>). Разбитие их на группы и сортировка, позволяет быстрее найти нужное свойство глазами.</p>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector"><span class="token class">.block</span> </span><span class="token punctuation">{</span>
    <span class="token comment">/* display block */</span>
    <span class="token property">display</span><span class="token punctuation">:</span> flex<span class="token punctuation">;</span>
    <span class="token property">flex-direction</span><span class="token punctuation">:</span> column<span class="token punctuation">;</span>
    
    <span class="token comment">/* box-size block */</span>
    <span class="token property">box-sizing</span><span class="token punctuation">:</span> content-box<span class="token punctuation">;</span>
    <span class="token property">width</span><span class="token punctuation">:</span> <span class="token number">100</span>px<span class="token punctuation">;</span>
    <span class="token property">margin</span><span class="token punctuation">:</span> <span class="token number">0</span>px<span class="token punctuation">;</span>
    <span class="token property">padding</span><span class="token punctuation">:</span> <span class="token number">10</span>px <span class="token number">12</span>px<span class="token punctuation">;</span>
    <span class="token property">border</span><span class="token punctuation">:</span> <span class="token number">1</span>px solid <span class="token hexcode">#f4f4f4</span><span class="token punctuation">;</span>
    
    <span class="token comment">/* position block */</span>
    <span class="token property">position</span><span class="token punctuation">:</span> absolute<span class="token punctuation">;</span>
    <span class="token property">top</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span>
    <span class="token property">right</span><span class="token punctuation">:</span> <span class="token number">5</span>px<span class="token punctuation">;</span>
    <span class="token property">bottom</span><span class="token punctuation">:</span> <span class="token number">7</span>px<span class="token punctuation">;</span>
    <span class="token property">left</span><span class="token punctuation">:</span> <span class="token number">0</span>px<span class="token punctuation">;</span>
    
    <span class="token comment">/* background block */</span>
    <span class="token property">background-color</span><span class="token punctuation">:</span> <span class="token hexcode">#c0c0c0</span><span class="token punctuation">;</span>
    
    <span class="token comment">/* font block */</span>
    <span class="token property">color</span><span class="token punctuation">:</span> <span class="token hexcode">#ffffff</span><span class="token punctuation">;</span>
    <span class="token property">font-size</span><span class="token punctuation">:</span> <span class="token number">12</span>px<span class="token punctuation">;</span>
    
    <span class="token comment">/* others.... */</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="сортировка-внутри-блока">Сортировка внутри блока</h2>
<p>Описание переменных и вложенных классов лучше разбивать на группы, отделять пустой строкой и сортировать по следующему принципу:</p>
<ol>
<li>Variable block - переменные, которые используются внутри блока</li>
<li>Block styles - стили, которые применяются к текущему блоку</li>
<li>Pseudo elements - стили для псевдоэлементов блока</li>
<li>Inner classes block - вложенные в блок селекторы</li>
<li>Elements block - элементы (BEM)</li>
<li>State blocks - селекторы, которые влияют на состояние блока</li>
<li>Modifiers block - модификаторы (BEM)</li>
</ol>
<p><strong>Мотивация:</strong> Ускоряет визуальный поиск блоков по классу.</p>
<pre class=" language-scss"><code class="prism  language-scss"><span class="token selector">.block </span><span class="token punctuation">{</span>
    <span class="token comment">/* variable block */</span>
    <span class="token property"><span class="token variable">$width</span></span><span class="token punctuation">:</span> <span class="token number">500</span>px<span class="token punctuation">;</span>
    
    <span class="token comment">/* block styles */</span>
    <span class="token property">width</span><span class="token punctuation">:</span> <span class="token variable">$width</span><span class="token punctuation">;</span>
    <span class="token comment">/* ... */</span>
    
    <span class="token comment">/* pseudo elements */</span>
    <span class="token selector"><span class="token parent important">&amp;</span>:before,
    <span class="token parent important">&amp;</span>:after </span><span class="token punctuation">{</span>
   
    <span class="token punctuation">}</span>
    
    <span class="token comment">/* inner classes block */</span>
    <span class="token selector">.inner-class1 </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    <span class="token selector">.inner-class2 </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    
    <span class="token comment">/* elements block */</span>
    <span class="token selector"><span class="token parent important">&amp;</span>__element1 </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    <span class="token selector"><span class="token parent important">&amp;</span>__element2 </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    
    <span class="token comment">/* state blocks */</span>
    <span class="token selector"><span class="token parent important">&amp;</span>:hover </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    <span class="token selector"><span class="token parent important">&amp;</span>:visted </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    
    <span class="token comment">/* modifiers block */</span>
    <span class="token selector"><span class="token parent important">&amp;</span>--block-modifier </span><span class="token punctuation">{</span>
    
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="разбитие-имен-в-названии-классов">Разбитие имен в названии классов</h2>
<p><strong>Мотивация:</strong> Уменьшает вложенность в классах, не создает пустых, не используемых <code>namespace-ов</code>. Упрощает поиск классов в исходном коде, т.к. запись <code>block-name__element-name</code> однозначно говорит, что в исходниках будут объявлены строки <code>block-name</code> и <code>__element-name</code>(в противном случае, эти строки могли бы быть разбиты на состовляющие <code>element</code>, <code>name</code> и т.д.) и их можно найти даже обычным поиском. Пример:</p>
<pre class=" language-scss"><code class="prism  language-scss">    <span class="token selector">.block </span><span class="token punctuation">{</span>
        <span class="token selector"><span class="token parent important">&amp;</span>-name </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
</code></pre>
<p>Объявлен <code>block</code>, но не было присвоено никаких стилей и использование его без <code>block-name</code> безсмысленено.</p>
<pre class=" language-scss"><code class="prism  language-scss"> <span class="token comment">// wrong</span>
 <span class="token selector">.long-block </span><span class="token punctuation">{</span>
    <span class="token selector"><span class="token parent important">&amp;</span>-name </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
 <span class="token punctuation">}</span>
 <span class="token selector">.long </span><span class="token punctuation">{</span>
    <span class="token selector"><span class="token parent important">&amp;</span>-block-name </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
 <span class="token punctuation">}</span>
 <span class="token comment">// right</span>
 <span class="token selector">.long-block-name </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<pre class=" language-scss"><code class="prism  language-scss"><span class="token comment">// wrong</span>
<span class="token selector">.block__long</span><span class="token punctuation">{</span>
    <span class="token selector">.element-name </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
<span class="token punctuation">}</span>
<span class="token selector">.block__long-element</span><span class="token punctuation">{</span>
    <span class="token selector"><span class="token parent important">&amp;</span>-name </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
<span class="token punctuation">}</span>
<span class="token comment">// right</span>
<span class="token selector">.block</span><span class="token punctuation">{</span>
    <span class="token selector"><span class="token parent important">&amp;</span>__long-element-name </span><span class="token punctuation">{</span><span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h1 id="javascript">3. JavaScript</h1>
<h2 id="spaces">Spaces</h2>
<pre class=" language-javascript"><code class="prism  language-javascript">    <span class="token comment">//wrong </span>
    <span class="token keyword">function</span> <span class="token function">run</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">{</span> <span class="token operator">...</span>
    <span class="token comment">// right </span>
    <span class="token keyword">function</span> <span class="token function">run</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token operator">...</span>
    
    <span class="token comment">//wrong </span>
    <span class="token keyword">function</span> <span class="token function">run</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token operator">...</span>
    <span class="token comment">// right </span>
    <span class="token keyword">function</span> <span class="token function">run</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token operator">...</span>
    
    <span class="token comment">//wrong</span>
    <span class="token keyword">function</span> <span class="token function">run</span><span class="token punctuation">(</span>when<span class="token punctuation">,</span>where<span class="token punctuation">,</span> how<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token operator">...</span>
    <span class="token comment">// right</span>
    <span class="token keyword">function</span> <span class="token function">run</span><span class="token punctuation">(</span>when<span class="token punctuation">,</span> where<span class="token punctuation">,</span> how<span class="token punctuation">)</span> <span class="token punctuation">{</span> <span class="token operator">...</span>
</code></pre>
<h2 id="variables">Variables</h2>
<pre class=" language-javascript"><code class="prism  language-javascript">    <span class="token comment">// wrong</span>
    <span class="token keyword">var</span> a<span class="token punctuation">,</span> b<span class="token punctuation">,</span>c <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">;</span>
    <span class="token comment">// right</span>
    <span class="token keyword">var</span> a<span class="token punctuation">;</span>
    <span class="token keyword">var</span> b<span class="token punctuation">;</span>
    <span class="token keyword">var</span> c <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">;</span>
</code></pre>
<h2 id="if-condition">If condition</h2>
<pre class=" language-javascript"><code class="prism  language-javascript">    <span class="token comment">// wrong</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>someConditionA <span class="token operator">===</span> <span class="token number">1</span> <span class="token operator">&amp;&amp;</span> someConditionB <span class="token operator">===</span> CONST_VALUE <span class="token operator">&amp;&amp;</span> someConditionC <span class="token operator">===</span> <span class="token string">'super string'</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token comment">// right</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>someConditionA <span class="token operator">===</span> <span class="token number">1</span> 
        <span class="token operator">&amp;&amp;</span> someConditionB <span class="token operator">===</span> CONST_VALUE 
        <span class="token operator">&amp;&amp;</span> someConditionC <span class="token operator">===</span> <span class="token string">'super string'</span>
    <span class="token punctuation">)</span> <span class="token punctuation">{</span>
</code></pre>
<h2 id="section"></h2>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// wrong</span>
<span class="token keyword">let</span> string <span class="token operator">=</span> <span class="token string">"adsasd"</span> <span class="token operator">+</span> <span class="token string">'222'</span><span class="token punctuation">;</span>
<span class="token comment">// right</span>
<span class="token keyword">let</span> string <span class="token operator">=</span> <span class="token string">'adsasd'</span> <span class="token operator">+</span> <span class="token string">'222'</span><span class="token punctuation">;</span>
</code></pre>
<h2 id="new-line-before-return">New line before <code>return</code></h2>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// wrong</span>
<span class="token keyword">function</span> <span class="token function">plus</span><span class="token punctuation">(</span>a<span class="token punctuation">,</span> b<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">let</span> c <span class="token operator">=</span> a <span class="token operator">+</span> b<span class="token punctuation">;</span>
    <span class="token keyword">let</span> d <span class="token operator">=</span> a <span class="token operator">/</span> c <span class="token operator">+</span> b <span class="token operator">/</span> c<span class="token punctuation">;</span>
    <span class="token keyword">return</span> d<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<span class="token comment">// right</span>
<span class="token keyword">function</span> <span class="token function">plus</span><span class="token punctuation">(</span>a<span class="token punctuation">,</span> b<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">let</span> c <span class="token operator">=</span> a <span class="token operator">+</span> b<span class="token punctuation">;</span>
    <span class="token keyword">let</span> d <span class="token operator">=</span> a <span class="token operator">/</span> c <span class="token operator">+</span> b <span class="token operator">/</span> c<span class="token punctuation">;</span>
    
    <span class="token keyword">return</span> d<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<h2 id="early-exit-function">Early exit function</h2>
<pre class=" language-javascript"><code class="prism  language-javascript"><span class="token comment">// wrong</span>
<span class="token keyword">function</span> <span class="token function">someFunction</span><span class="token punctuation">(</span>cond1<span class="token punctuation">,</span> name<span class="token punctuation">,</span> value<span class="token punctuation">,</span> perms<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">let</span> retval <span class="token operator">=</span> SUCCESS<span class="token punctuation">;</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>someCondition<span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token keyword">if</span> <span class="token punctuation">(</span>name <span class="token operator">!==</span> <span class="token keyword">null</span> <span class="token operator">&amp;&amp;</span> name <span class="token operator">!==</span> <span class="token string">''</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
            <span class="token keyword">if</span> <span class="token punctuation">(</span>value <span class="token operator">!==</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
                <span class="token keyword">if</span> <span class="token punctuation">(</span>perms<span class="token punctuation">.</span><span class="token function">allow</span><span class="token punctuation">(</span>name<span class="token punctuation">)</span> <span class="token punctuation">{</span>
                    <span class="token comment">// Do Something</span>
                <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                    reval <span class="token operator">=</span> PERM_DENY<span class="token punctuation">;</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
                retval <span class="token operator">=</span> BAD_VALUE<span class="token punctuation">;</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
            retval <span class="token operator">=</span> BAD_NAME<span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">}</span> <span class="token keyword">else</span> <span class="token punctuation">{</span>
        retval <span class="token operator">=</span> BAD_COND<span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
    
    <span class="token keyword">return</span> retval<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token comment">// right</span>
<span class="token keyword">public</span> <span class="token function">SomeFunction</span><span class="token punctuation">(</span>cond1<span class="token punctuation">,</span> name<span class="token punctuation">,</span> value<span class="token punctuation">,</span> perms<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>someCondition<span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token keyword">return</span> BAD_COND<span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>name <span class="token operator">===</span> <span class="token keyword">null</span> <span class="token operator">||</span> name <span class="token operator">===</span> <span class="token string">''</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token keyword">return</span> BAD_NAME<span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span>value <span class="token operator">==</span> <span class="token number">0</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token keyword">return</span> BAD_VALUE<span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token operator">!</span>perms<span class="token punctuation">.</span><span class="token function">allow</span><span class="token punctuation">(</span>name<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
        <span class="token keyword">return</span> PERM_DENY<span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
    
    <span class="token keyword">return</span> SUCCESS<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

</code></pre>

