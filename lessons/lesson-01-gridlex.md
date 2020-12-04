---
layout: page
title: Lesson 01_ Gridlex
type: lesson
permalink: /lesson-01-gridlex/
table_of_contents: [
  {
    title: 'Official Docs'
  },
  {
    title: 'The Basics',
    list: [
      {
        title: 'Example on a .grid'
      },
      {
        title: 'Example on a .col'
      },
      {
        title: 'Which one should I use?'
      }
    ]
  },
  {
    title: 'Responsive'
  },
  {
    title: 'Helpers',
    list: [
      {
        title: 'Horizontal alignment',
        list: [
          {
            title: 'Left (default)'
          },
          {
            title: 'Center'
          },
          {
            title: 'Right'
          }
        ]
      },
      {
        title: 'Vertical alignment',
        list: [
          {
            title: 'Top (default)'
          },
          {
            title: 'Middle'
          },
          {
            title: 'Bottom'
          }
        ]
      }
    ]
  },
]

---

## Official Docs
[https://gridlex.devlint.fr/](https://gridlex.devlint.fr/)

___

## The Basics
By default, a div with `.col`, that is within a `.grid`, will automatically adjust to be the same width as its siblings with `.col`. For example, this will split your elements into 3 equal parts.
```
<div class="grid">
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
</div>
```
<div class="lesson-1__section">
  <div class="grid">
    <div class="col"><div class="block"></div></div>
    <div class="col"><div class="block"></div></div>
    <div class="col"><div class="block"></div></div>
  </div>
</div>

To specify how wide you want your elements, you can either add a column count modifier to the `.grid` or to the `.col`. 

>
The modifier on a `.grid` will tell the elements to split into that many columns. But the modifier on a `.col` will tell it to split relative to 12 columns. That means that `col-3` will take up 3 columns in the Gridlex default of 12, which is 25%.
>

### Example on a .grid
```
<div class="grid-3">
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
</div>
```
<div class="lesson-1__section">
  <div class="grid-3">
    <div class="col"><div class="block"></div></div>
    <div class="col"><div class="block"></div></div>
    <div class="col"><div class="block"></div></div>
    <div class="col"><div class="block"></div></div>
    <div class="col"><div class="block"></div></div>
    <div class="col"><div class="block"></div></div>
    <div class="col"><div class="block"></div></div>
    <div class="col"><div class="block"></div></div>
    <div class="col"><div class="block"></div></div>
  </div>
</div>

Because our `.grid` has a modifier of `3`, it splits the columns into rows of 3 (33.33% each).

### Example on a .col
```
<div class="grid">
  <div class="col-3"></div>
  <div class="col-3"></div>
  <div class="col-3"></div>
  <div class="col-3"></div>
  <div class="col-3"></div>
  <div class="col-3"></div>
  <div class="col-3"></div>
  <div class="col-3"></div>
</div>
```
<div class="lesson-1__section">
  <div class="grid">
    <div class="col-3"><div class="block"></div></div>
    <div class="col-3"><div class="block"></div></div>
    <div class="col-3"><div class="block"></div></div>
    <div class="col-3"><div class="block"></div></div>
    <div class="col-3"><div class="block"></div></div>
    <div class="col-3"><div class="block"></div></div>
    <div class="col-3"><div class="block"></div></div>
    <div class="col-3"><div class="block"></div></div>
  </div>
</div>

Because our `.col` have modifiers of `3`, it tells the column to take up 3 spaces in our row of 12 columns (25% each).

### Which one should I use?

They both have their uses, but I personally only use the modifiers on the `.col`. It allows for more specfic column sizes and allows the complete removal of the `.grid` modifier classes from the CSS file which trims down the filesize considerably.

___

## Responsive

Responsive design with Gridlex is very simple. By default, Gridlex comes with 4 different size modifiers:

- lg: Large 1280px
- md: Medium 1024px
- sm: Small 768px
- xs: Extra Small 480px

To set a column to have a particular width at a certian breakpoint, you add a modifier to the `.col` class. Breakpoints are added as modifiers by adding an underscore, the size shorthand and a column width. Example:
```
<div class="grid">
  <div class="col-4_sm-12">
  </div>
  <div class="col-8_sm-12">
  </div>
</div>
```
<div class="lesson-1__section">
  <div class="grid">
    <div class="col-4_sm-12"><div class="block"></div></div>
    <div class="col-8_sm-12"><div class="block"></div></div>
  </div>
</div>
In this example, the columns will change to be full width once the screen is 768px or less. Resize your browser to see it in action.

Feel free to add as many breakpoints as you wish.
```
<div class="grid">
  <div class="col-2_lg-3_md-4_sm-6_xs-12">
  </div>
</div>
```
<div class="lesson-1__section">
  <div class="grid">
    <div class="col-2_lg-3_md-4_sm-6_xs-12"><div class="block"></div></div>
    <div class="col-2_lg-3_md-4_sm-6_xs-12"><div class="block"></div></div>
    <div class="col-2_lg-3_md-4_sm-6_xs-12"><div class="block"></div></div>
    <div class="col-2_lg-3_md-4_sm-6_xs-12"><div class="block"></div></div>
    <div class="col-2_lg-3_md-4_sm-6_xs-12"><div class="block"></div></div>
    <div class="col-2_lg-3_md-4_sm-6_xs-12"><div class="block"></div></div>
  </div>
</div>

___

## Helpers

There are multiple helpers classes that can be applied to the `.grid`.

### Horizontal alignment

#### Left (default)
```
<div class="grid">
  <div class="col-4">
  </div>
</div>
```
<div class="lesson-1__section">
  <div class="grid">
    <div class="col-4"><div class="block"></div></div>
  </div>
</div>


#### Center
```
<div class="grid-center">
  <div class="col-4">
  </div>
</div>
```
<div class="lesson-1__section">
  <div class="grid-center">
    <div class="col-4"><div class="block"></div></div>
  </div>
</div>

#### Right
```
<div class="grid-right">
  <div class="col-4">
  </div>
</div>
```
<div class="lesson-1__section">
  <div class="grid-right">
    <div class="col-4"><div class="block"></div></div>
  </div>
</div>

### Vertical alignment

#### Top (default)
```
<div class="grid">
  <div class="col-4">
  </div>
  <div class="col-4">
  </div>
  <div class="col-4">
  </div>
</div>
```
<div class="lesson-1__section">
  <div class="grid">
    <div class="col-4"><div class="block"></div></div>
    <div class="col-4"><div class="block block--large"></div></div>
    <div class="col-4"><div class="block"></div></div>
  </div>
</div>


#### Middle

>
This is one is especially helpful for things like headers where the logo height and the nav item heights are different, but you still want to see them vertically centered.
>

```
<div class="grid-middle">
  <div class="col-4">
  </div>
  <div class="col-4">
  </div>
  <div class="col-4">
  </div>
</div>
```
<div class="lesson-1__section">
  <div class="grid-middle">
    <div class="col-4"><div class="block"></div></div>
    <div class="col-4"><div class="block block--large"></div></div>
    <div class="col-4"><div class="block"></div></div>
  </div>
</div>

#### Bottom
```
<div class="grid-bottom">
  <div class="col-4">
  </div>
  <div class="col-4">
  </div>
  <div class="col-4">
  </div>
</div>
```
<div class="lesson-1__section">
  <div class="grid-bottom">
    <div class="col-4"><div class="block"></div></div>
    <div class="col-4"><div class="block block--large"></div></div>
    <div class="col-4"><div class="block"></div></div>
  </div>
</div>