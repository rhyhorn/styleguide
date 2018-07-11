
# 1. Html
## Кавычки в ``html``

В ``html`` всегда использовать двойные кавычки(``"``)

**Мотивация:** Код становиться более однородным и лучше воспринимаеться визуально.

```html 
<!-- wrong -->
<div class='class-name'></div>

<!-- right -->
<div class="class-name"></div>
```

##  Порядок атрибутов

Сортирока атрибутов по важности. Первый - обязательно ``class``.  Последними идут атрибуты, которые исползуются для ``js``.

**Мотивация:** Позволяет визуально отделить верстку елемента, от остальных его функции.

    1. class
    2. id
    3. type, value, href ...
    4. data

```html
// wrong
<input id="email" class="list list--highlited" data-role="email-input" type="email" />
// right
<input class="list list--highlited" id="email"  type="email" data-role="email-input" />
```

## Перенос атрибутов на новую строчку 

Когда строка с тегом из-за большого числа аттрибутов, становиться слишком длинной, стоит переносить атрибуты на новую строчку. Первый всегда остается на одной строчке с тегом, остальные выравниваются по нему слева. Стоит придерживаться однородности, если, хотя бы один аттрибут перенесен - все остальные тоже быть с новой строчки. Закрывающая скобочка тега, толжна быть обязательно с новой строчки и выровняна по открывающей.

**Мотивация:** Ускаряет визуальны поиск нужного атрибута, плюс помогает избежать горизонтального скрола в редакторе.

```html
// wrong 
<div
    class="wrong-div">text</div>

// right
<div class="wrong-div">text</div>
// or 
<div class="wrong-div">
    text
</div>
// wrong
<input id="email" class="list list--highlited" 
    data-role="email-input" type="email" />
// right
<input class="list list--highlited" 
       id="email"  
       type="email" 
       data-role="email-input"
/>
// wrong 
<div class="wrong-div" 
     id="div">
     text
</div>
// right 
<div class="wrong-div" 
     id="div"
>
    text
</div>
```

# 2. Styles

## Кавычки

Всегда испольновать одинарные кавычки (``'``)

**Мотивация:** Код становиться более однородным и лучше воспринимаеться визуально.

```scss
/* wrong */
.block {
	 background: url("/now-banner.png") no-repeat; 
	 &:before {
		content: "";
	}
}

/* right */
.block {
	 background: url('/now-banner.png') no-repeat; 
	 
	 &:before {
		content: '';
	}
}
```

## Пробелы

Обязательные пробелы после селектора, свойства и запятых в значениях свойств. Отделять блоки свойств и сложенные слекторы одной пустой строчкой.

**Мотивация:** Код становиться однородным и лучше воспринимаеться визуально.

```scss
/* wrong */
.main-logo-block {  
  float: left;   
  a {  
	display:block;  
  }  
  span{  
    display: none;  
  }
}
/* right */
.main-logo-block {  
  float: left;   
  
  a {  
	display: block;  
  } 
   
  span {  
    display: none;  
  }
}
```
## Задание цвета

Успользовать только полные версии для ``hex`` варианта и только в нижнем регистре, не использовать строковые аналоги.

**Мотивация:** Улучшает читаемость кода

```css
.block {
	/* wrong */
	color: #FFF;
	color: white;
	color: #FFFFFF;
	/* right */
	color: #ffffff;
}
```

## Указание единицы измерения

Если для слектора указываеться свойство в котором несколько значений (например ``margin: 0px 5px``), то оябзательно указывать единицу измерения для ``0``.

**Мотивация:** Значение лучше вопринимается визуально, плюс меньше движений нужно для изменения нуля на другое число.

```css
/* wrong */
.block {
	margin: 0 5px;
	padding: 10rem 0 5rem;
}

/* right */
.block {
	margin: 0px 5px;
	padding: 10rem 0rem 5rem;
}
```

## Сортировка свойств

1. *-top
2. *-right
3. *-bottom
4. *-left

**Мотивация:** Ускоряет визуальный поиск нужного свойства

```css
/* right */
.block {
	top: 10px;
	right: 20px;
	bottom: 5px;
	left: 10px;
	
	margin-top: 10px;
	margin-left: 20px;

	border-right: 1px solid #c0c0c0;
	border-bottom: 1px solid #c0c0c0;
}
```

## Обязательные кавычки в ``url``

```css
/* wrong */
background: url(/now-banner.png) no-repeat;
background: url("/now-banner.png") no-repeat;
/* right */
background: url('/now-banner.png') no-repeat;
```
## Стилизация тегов

Стараться не стилизировать вложенные в классы теги. Исключением может быть стилизирование ``img`` внутри контейнера или задание стилей для текстов из, которые приходят из бекенда

**Мотивация:** Разметка может меняться и добавления тега может привести к не ожидаемому применению стилей к нему. 

```html
<form class="form">
	<input class="form__password-input">
</form>
```
```scss
/* wrong */
.form {
	input {
		color: #c0c0c0;
	}
}
/* right */
.form {
	&__password-input {
		color: #c0c0c0;
	}
}
/* right */
.tournament__image {
	img {
		display: block;
		margin: 0px auto;
	}
}
```

## Групирование селекторов

```css
/* wrong */
.games-container.home, .games-container-all {
  padding: 5px;
}

/* right */
.games-container.home, 
.games-container-all {
  padding: 5px;
}
```

## BEM

### Названия классов

Слова в названиях классов отделяются одинарным дефисом `-` и пишутся в нижнем регистре. 

```css
.class {}
.three-words-class{}
```

### Block

В общем случае, блок не должен содержать внешних отступов и позиционирования (``margin``, ``top`` ...).

```css
.block {}
.three-words-block {}
```
    
Блок отделяется от элемента двумя подчеркиваниями ``__``

### Element

```css
.block__element {}
.block__another-element {}
.long-block__long-element {}
```
    
Модификатор отделяется двойным дефисом ``--``

### Modifier

```css
.block--modifier {}
.block--is-visible {}
.block__element--modifier {}
```

```html
<form class="promocode promocode--activated" 
	  action="/promocode" 
	  method="POST"
>
    <div class="promocode__inner">
        <input class="promocode__input" value="" />
        <button class="promocode__btn promocode__btn--disabled"
                type="submit"
        >
            Submit
        </button>
    </div>
</div>
```    
## Состояние

Для псевдоклассов, которые определяю состояние блока(``:hover``) желательно делать модификатор, с теми же свойствами.

**Мотивация:** Дает возможность отобразить блок в нужном состоянии, не использую инспектор, просто добавив соответствующий модификатор

```scss

.block {
	text-decoration: none;
	
	&:hover,
	&--is-hover {
		text-decoration: underline;
	}
}
```

## Properties groups

Свойства, необходимо бить на группы, разделенные одной пустой строкой, и придерживаться порядка:

    1. display block
    2. box-size block
    3. position block
    4. background block
    5. font block
    
**Мотивация**: чаще всего, при изменении элемента, нужно модифицировать одни и те же свойства(``margin``, ``top``, ``color``). Разбитие их на группы и сортировка, позволяет быстрее найти нужное свойство глазами.

```css
.block {
    /* display block */
    display: flex;
    flex-direction: column;
    
    /* box-size block */
    box-sizing: content-box;
    width: 100px;
    margin: 0px;
    padding: 10px 12px;
    border: 1px solid #f4f4f4;
    
    /* position block */
    position: absolute;
    top: 5px;
    right: 5px;
    bottom: 7px;
    left: 0px;
    
    /* background block */
    background-color: #c0c0c0;
    
    /* font block */
    color: #ffffff;
    font-size: 12px;
    
    /* others.... */
}
```
## Сортировка внутри блока

Описание переменных и вложенных классов лучше разбивать на группы, отделять пустой строкой и сортировать по следующему принципу:

1. Variable block - переменные, которые используются внутри блока
2. Block styles - стили, которые применяются к текущему блоку
3. Pseudo elements - стили для псевдоэлементов блока
4. Inner classes block - вложенные в блок селекторы
5. Elements block - элементы (BEM) 
6. State blocks - селекторы, которые влияют на состояние блока
7. Modifiers block - модификаторы (BEM)

**Мотивация:** Ускоряет визуальный поиск блоков по классу.

``` scss
.block {
    /* variable block */
    $width: 500px;
    
    /* block styles */
    width: $width;
    /* ... */
    
    /* pseudo elements */
    &:before,
    &:after {
   
    }
    
    /* inner classes block */
    .inner-class1 {}
    .inner-class2 {}
    
    /* elements block */
    &__element1 {}
    &__element2 {}
    
    /* state blocks */
    &:hover {}
    &:visted {}
    
    /* modifiers block */
    &--block-modifier {
    
    }
}
```
## Разбитие имен в названии классов

**Мотивация:** Уменьшает вложенность в классах, не создает пустых, не используемых ``namespace-ов``. Упрощает поиск классов в исходном коде, т.к. запись ``block-name__element-name`` однозначно говорит, что в исходниках будут объявлены строки ``block-name`` и ``__element-name``(в противном случае, эти строки могли бы быть разбиты на состовляющие ``element``, ``name`` и т.д.) и их можно найти даже обычным поиском. Пример:

```scss
.block {
  &-name {}
}
```

Объявлен ``block``, но не было присвоено никаких стилей и использование его без ``block-name`` безсмысленено.

```scss
 // wrong
 .long-block {
    &-name {}
 }
 .long {
    &-block-name {}
 }
 // right
 .long-block-name {}
```
```scss
// wrong
.block__long{
    .element-name {}
}
.block__long-element{
    &-name {}
}
// right
.block{
    &__long-element-name {}
}
```
# 3. JavaScript

## Spaces 

```javascript
    //wrong 
    function run(){ ...
    // right 
    function run() { ...
    
    //wrong 
    function run () { ...
    // right 
    function run() { ...
    
    //wrong
    function run(when,where, how) { ...
    // right
    function run(when, where, how) { ...
```

## Variables

```javascript
    // wrong
    var a, b,c = 5;
    // right
    var a;
    var b;
    var c = 5;
```

## If condition 

```javascript 
    // wrong
    if (someConditionA === 1 && someConditionB === CONST_VALUE && someConditionC === 'super string') {
    // right
    if (someConditionA === 1 
        && someConditionB === CONST_VALUE 
        && someConditionC === 'super string'
    ) {
```
## 
```javascript 
// wrong
let string = "adsasd" + '222';
// right
let string = 'adsasd' + '222';
```

## New line before ``return``

```javascript
// wrong
function plus(a, b) {
    let c = a + b;
    let d = a / c + b / c;
    return d;
}
// right
function plus(a, b) {
    let c = a + b;
    let d = a / c + b / c;
    
    return d;
}
```

## Early exit function

```javascript
// wrong
function someFunction(cond1, name, value, perms) {
    let retval = SUCCESS;
    if (someCondition) {
        if (name !== null && name !== '') {
            if (value !== 0) {
                if (perms.allow(name) {
                    // Do Something
                } else {
                    reval = PERM_DENY;
                }
            } else {
                retval = BAD_VALUE;
            }
        } else {
            retval = BAD_NAME;
        }
    } else {
        retval = BAD_COND;
    }
    
    return retval;
}

// right
public SomeFunction(cond1, name, value, perms) {
    if (!someCondition) {
        return BAD_COND;
    }
    if (name === null || name === '') {
        return BAD_NAME;
    }
    if (value == 0) {
        return BAD_VALUE;
    }
    if (!perms.allow(name)) {
        return PERM_DENY;
    }
    
    return SUCCESS;
}

```

## Тернарный оператор

```js
// wrong
var path = CONSTANT === 'condition' ?  
  'some/long/string/value'  
  :  
  'another/long/string/value';

// right
var path = CONSTANT === 'condition' 
  ? 'some/long/string/value'  
  : 'another/long/string/value';
```

