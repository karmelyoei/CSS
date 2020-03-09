# First thing you should know about the CSS

###### tags: `Design`


## <span style="color:orange;">CSS ID & Classes </span>

In the CSS a class selector is a name preceded by a full stop (“.”) and an ID selector is a name preceded by a hash character (“#”).

The difference between an ID and a class is that an ID can be used to identify one element, whereas a class can be used to identify more than once.

## <span style="color:orange;">Grouping and Nesting  </span>

Through nesting and grouping, you can simplify your code.

The meaning of **Grouping** is that instead of giving multiple selectors the same property. You can simply separate selectors with commas in one line and apply the same properties to them all.

Example : 

```CSS
h1 {
color : red;
}

.class1 {

color: red;
}

.class2 {
color: red;
}
```

You can simply can do this 
``` css
h1, .class1, .class2 {
color : red;
}
```

While **The Nesting** means that there is no need to use many classes or ID's selectors. Beacuse you can specify properties to selectors within other selectors.

Example :

```css
#nav {
    background-color: #ccc;
    padding: 1em
}

#nav h1 {
    color: #ff0;
}

#nav p {
    color: red;
    font-weight: bold;
}

```
No need to give IDs or classes for  h1, P tags
```htmlmixed=
<div id="nav">
    <h1>I love Rainbow </h1>
    <p> This is a unicorn </p>
    <p>Pretty Flower</p>
</div>
```

## <span style="color:orange;">Pseudo Classes  </span>

A pseudo-class is used to define a special state of an element.

For example, it can be used to:

- Style an element when a user mouses over it.
- Style visited and unvisited links differently.
- Style an element when it gets focus.

```css
selector:pseudo-class {
  property:value;
}
```

For the Links You can target if visited or not visited the links

```css
a:vistied {
color : pink;
}

a:link {
color : pink;
}
```
other dynamic pseudo-classes : 

- active : Selects the active link.
- hover : Selects links on mouse over
- focus : Selects the <input> element that has focus.


```css
/* mouse over link */
a:hover {
  color: green;
}

/* selected link */
a:active {
  color: red;
}
```
:::warning
Note: 
- **a:hover** MUST come after **a:link** and **a:visited** in the CSS definition in order to be effective! 
- **a:activ**e MUST come after **a:hover** in the CSS definition in order to be effective! Pseudo-class names are **not case-sensitive**.
:::

<br>

## <span style="color:orange;">The :first-child Pseudo-class  </span>

The :first-child pseudo-class target a specified element that is the first child of another element.

For Example : 

```htmlmixed=
<body>
<p>This is The first child.</p>
<p>This is The second child.</p>
```
```css
p:first-child {
color: green;
}
```

## <span style="color:orange;">Resources  </span>
- [W3School](https://www.w3schools.com/css/css_pseudo_classes.asp).
 


