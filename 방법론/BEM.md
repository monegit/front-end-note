# BEM이란?

> BEM은 Block(문단), Element(요소), Modifier(수식어)을 뜻한다.

* menuitemvisible
* menu-item-visible
* menuItemVisible

**위 예제를 보고 BEM의 필요성에 대한 설명이다.**

1. 각 단어의 뜻을 명확히 이해하기 어렵다.
2. 이해할 수 있어도 block, element, modifier의 구분이 모호하다.



# 명명 규칙

`block-name__element-name_modifier-name_modifier-val`

* 이름은 소문자로 작성
* 단어는 `-`로 구분
* 블록 이름은 요소 및 수식어에 대한 `namespace` 를 정의
* 요소 이름은 이중 밑줄 `__` 로 블록 이름과 구분
* 수식어 이름은 단일 밑줄 `_` 로 블록 또는 요소 이름과 구분
* 수식어 값은 단일 밑줄 `_` 로 수식어 이름과 구분
* bool 수식어의 경우 값이 이름에 포함되지 않음



# 예제

HTML에서 BEM 엔티티는 `class` 속성으로 표시



## Block name

> menu

```html
<div class="menu">
  ...
</div>
```

```css
.menu { color: red; }
```



## Element name

> menu__item

```html
<div class="menu">
  ...
  <span class="menu__item"></span>
</div>
```

```css
.menu__item { color: red; }
```



## Block modifier name

> menu_hidden
>
> menu_theme_islands

```html
<div class="menu menu_hidden">
  ...
</div>
<div class="menu menu_theme_islands">
  ...
</div>
```

```css
.menu_hidden { display: none; }
.menu_theme_islands { color: green; }
```



## Element modifier name

> menu__item_visible
>
> menu__item_type_radio

```html
<div class="menu">
  ...
  <span class="menu__item menu__item_visible menu__item_type_radio">...</span>
</div>
```

```css
.menu__item_visible { }
.menu__item_type_radio { color: blue; }
```

