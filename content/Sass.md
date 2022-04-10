Status: 
Tags: 
Links: [[
___

# Sass
## Principles
### Variables

```sass
$red: hsl(0, 100%, 50%);

.button.danger {
	color: $red;
	border: 1px solid $red;
}
```
### Nesting
```sass
.accordion {
  max-width: 600px;
  margin: 4rem auto;
  width: 90%;
  font-family: "Raleway", sans-serif;
  background: #f4f4f4;

  &__copy {
    display: none;
    padding: 1rem 1.5rem 2rem 1.5rem;
    color: gray;
    line-height: 1.6;
    font-size: 14px;
    font-weight: 500;

    &--open {
      display: block;
    }
  }
}

//Becomes
.accordion__copy
.accordion__copy--open
```
```
### Mixin
```sass
@mixin reset-list {
  margin: 0;
  padding: 0;
  list-style: none;
}

@mixin horizontal-list {
  @include reset-list;
}
```
___
References:

Created:: 2022-03-18 04:01
