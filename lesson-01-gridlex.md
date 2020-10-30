# Lesson 01: Gridlex
---

## Benefits
* Faster layout development
* Easier responsive styling
* Accurate mockup builds
---

## Official Docs
[https://gridlex.devlint.fr/](https://gridlex.devlint.fr/)
---

## The Basics
By default, a div with `.col`, that is within a `.grid`, will automatically adjust to be the same width as its siblings with `.col`. For example, this will split your elements into 3 equal parts.
```
<div class="grid">
  <div class="col">
  </div>
  <div class="col">
  </div>
  <div class="col">
  </div>
</div>
```

---

To specify how wide you want your elements, you can either add a column count modifier to the `.grid` or to the `.col`.

Example on a `.grid`
```
<div class="grid-4">
  <div class="col">
  </div>
  <div class="col">
  </div>
  <div class="col">
  </div>
  <div class="col">
  </div>
</div>
```

Example on a `.col`
```
<div class="grid">
  <div class="col-3">
  </div>
  <div class="col-3">
  </div>
  <div class="col-3">
  </div>
  <div class="col-3">
  </div>
</div>
```

Both of those examples will split the elements into 4 equal columns.

>>>
**But wait, grid has a modifier of 4 and col has a modifier of 3. How are they both split into 4 equal parts?🤔**
>>>

Great question. The modifier on a `.grid` will tell the elements to split into that amount. So `.grid-4` will split the columns into 4 equal parts. The modifier on a `.col` will make the element span the number of columns thatg is specified, in relation to a 12 column grid.

>>>
**😳 wait, I have to do math?! That's it, I'm done.**
>>>

Whoa, whoa, whoa, hold it right there. It's easy math, I promise. Gridlex by default is a 12 column grid. That means that columns will stay on the same row as long as their modifiers add to up 12 or lower. For example:
```
<div class="grid">
  <div class="col-5">
  </div>
  <div class="col-7">
  </div>
  <div class="col-8">
  </div>
  <div class="col-4">
  </div>
</div>
```
That will create 2 rows. **col-5** and **col-7** will be on the first row, **col-8** and **col-4** will be on the second.

### Which one should I use?
They both have their uses, but I personally only use the modifiers on the `.col`. It allows for more specfic column sizes and allows the complete removal of the `.grid` modifier classes from the CSS file which trims down the size considerably.

## Responsive
---

Responsive design with Gridlex is very simple. By default, Gridlex comes with 4 different size modifiers:
- lg: Large 1280px
- md: Medium: 1024px
- sm: Small: 768px
- xs: Extra Small: 480px