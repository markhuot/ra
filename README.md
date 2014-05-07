Ra
====

Ra is a simple Sass "grid system" that gets out of the way and lets you write styles the way you want to. It comes with just a few mixins that provide all the power you’ll need.

Example
----

```scss
section {
  @include row();
}
nav {
  @include col(2/6);
}
article {
  @include col(3/6);
}
aside {
  @include col(1/6);
}
````

Simply use `row()` to denote your grid container (this essentially provides a clearfix). Then use `col($width)` to define the size of a column within. For example, to cratea a list of posts that, responsively, moves from a single column, to two columns, to four columns you may…

```scss
.story {
  @include col(1);

  @media screen and (min-width: 500px) {
    @include col(1/2);
  }

  @media screen and (min-width: 1000px) {
    @include col(1/4);
  }
}
```
