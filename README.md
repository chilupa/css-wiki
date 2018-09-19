# css-wiki

### Overriding of CSS `class`es: 

Order of declaration of class matters. Consider the below example, the h1 element turns **blue** since the class `.blue-text` was declared after the `.pink-text` class. 

```
<style>
  .pink-text {
    color: pink;
  }
  .blue-text {
    color: blue;
  }
</style>

<h1 class="pink-text blue-text">Hello World!</h1>
```

***

### Overriding of `id` over `class`es: 
In this scenario, the `h1` text color is **Orange**. The order of declaration of classes doesn't matter. The `id` takes over precedence. 

```
<style>
  .pink-text {
    color: pink;
  }
  .blue-text {
    color: blue;
  }
  .orange-text {
   color: orange;
  }
</style>

<h1 id="orange-text" class="pink-text blue-text">Hello World!</h1>
```

***

### Overriding CSS styles with `inline` style: 
In this scenario, the `h1` text color turns **White** since we declared `inline` style to that elememt. `inline` style element overrides all the CSS declarations in the `<style>` element

```
<style>
  .pink-text {
    color: pink;
  }
  .blue-text {
    color: blue;
  }
  .orange-text {
   color: orange;
  }
</style>

<h1 id="orange-text" style="color: white;" class="pink-text blue-text">Hello World!</h1>
```

styles with !important declaration cannot be overridden. 

```
<style>
  .pink-text {
    color: pink;
  }
  .blue-text {
    color: blue !important;
  }
  .orange-text {
   color: orange;
  }
</style>

<h1 id="orange-text" style="color: white;" class="pink-text blue-text">Hello World!</h1>
```
