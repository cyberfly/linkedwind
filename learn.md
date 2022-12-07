## Development Tips

----

### flex-1

This rule force the element to expand and take the available width

----

### Inline Flex

Inline element such as button, hyperlink will behave like block element if we use `flex`. 

When behave like block element, it means the inline element cannot sit side by side with others element anymore. 

The solution to this issue is to use `inline-flex`. It has the power of flex but keeping the inline behaviour intact.

Use case:

- Using svg image inside button and hyperlink

Example

```
<div>
<!-- hyperlink with home icon (svg) -->
 <a href="#" class="inline-flex items-center">
  <span>Home</span>

  <svg>...</svg>
 </a>

<!-- hyperlink with contact icon (svg) -->
 <a href="#" class="inline-flex items-center">
  <span>Contact</span>

  <svg>...</svg>
 </a>
</div>
```

----

### Flex Col

So you want to use flex rule such as `flex-1`, but this rule will only work if the parent element is `flex`

However if we apply `flex` to the parent element, the child elements will sit side by side together, but this time we didnt want that.

The solution to this issue is to use `flex-col`. It has the power of flex but doesnt make the child elements sit side by side together

Example

```
<div class="flex flex-col">
    <div>First</div>

    <div class="flex-1">Second, below the the first</div>
</div>
```

----

### Responsive stacked with Flex Row and Flex Col

Lets say you want the child elements stacked vertically on mobile, but on desktop you want it to sit side by side

We can utilize `flex-row` and `flex-col` for this situation, and using responsive modifier such as `md` and `lg`

Example

```
<div class="flex flex-col md:flex-row ">
    <div>A</div>
    <div>B</div>
    <div>C</div>
</div>
```

On mobile

```
A
B
C
```

On bigger screen

```
A B C
```

