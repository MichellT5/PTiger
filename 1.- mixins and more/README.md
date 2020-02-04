# Functions
### Responsive px
this function will allow you to make some properties "responsives" by making them grow to a specified size.

```scss
@function responsive-px($sm-px, $lg-px, $sm-vw, $lg-vw) {
    @return calc(#{$sm-px}px + (#{$lg-px} - #{$sm-px}) * ((100vw - #{$sm-vw}px) / (#{$lg-vw} - #{$sm-vw})));
}
```

**For example:** the code from below indicates that the font size will be 16px at 768px viewport and 25px at 1920px viewport width

```scss
.text {
    font-size: responsive-px(16, 25, 768, 1920);
}
```

# Mixins
### phone - (Included in ND styles)
This mixin allow you to style in xs view. equivalent to ` @media (max-width:767px) {} `

```scss
@include phone {
    @content;
};
```

### tablet-desktop - (Included in ND styles)
This mixin allow you to style starting sm. equivalent to ` @media (min-width:768px) {} `

```scss
@include tablet-desktop {
    @content;
};
```

### hoverall - (Hover all)
This mixin allow you to make styles for hover, focus and active pseudo-classes.

```scss
@mixin hoverall {
    &:hover, &:focus, &:active {
        @content;
    }
};
```

### hover - (Hover)
This mixin make styles on hover but only starting at 768px.

```scss
@mixin hover {
    @include tablet-desktop {
        @include hoverall {
            @content;
        };
    };
};
```

### min - (Media query min)
This mixin allow you to make a mediaquery starting from the min-px you want.

```scss
@mixin min($min) {
    @media(min-width:#{$min}px) {
        @content;
    }
};
```

### max - (Media query max)
This mixin allow you to make a mediaquery ending at the max-px you want.

```scss
@mixin max($max) {
    @media(max-width:#{$max}px) {
        @content;
    }
};
```

### range - (Media query range)
This mixin allow you to make a mediaquery between a minpx and a maxpx you want.

```scss
@mixin range($min: 0, $max: 1920) {
    @media (min-width:#{$min}px) and (max-width:#{$max}px) {
        @content;
    }
};
```

### transition - (make a transition)
This mixin allow you to create a transition for multiple properties that shares same values.

```scss
@function remove-nth($list, $index) { $result: null; @if type-of($index) !=number { @warn "$index: #{quote($index)} is not a number for `remove-nth`."; } @else if $index==0 { @warn "List index 0 must be a non-zero integer for `remove-nth`."; } @else if abs($index)>length($list) { @warn "List index is #{$index} but list is only #{length($list)} item long for `remove-nth`."; } @else { $result: (); $index: if($index < 0, length($list) + $index + 1, $index); @for $i from 1 through length($list) { @if $i !=$index { $result: append($result, nth($list, $i)); } } } @return $result; }
/* usage: @include transition(prop1, prop2, ..., 0.5s cubic-bezier(0.16, 0.85, 0.45, 1)); */
@mixin transition($args...) { $type: nth($args, length($args)); $props: remove-nth($args, length($args)); $result: (); @for $i from 1 through length($props) { $prop: nth($props, $i); $result: append($result, $prop); $result: append($result, $type); @if $i !=length($props) { $result: append($result, unquote($string: ",")); } } transition: $result; }
```

**For example:** ` @include transition(color, background-color, border-color, 0.3s ease-in-out) `
will produce

```scss
transition:
    color 0.3s ease-in-out,
    background-color 0.3s ease-in-out,
    border-color 0.3s ease-in-out;
```

### make-responsive - (Make class(es) to bootstrap style)
This mixin allow you to create your own clases and use them like bootstrap.

```scss
@mixin make-responsive($class, $prop, $value) {
    #{$class} {
        #{$prop}: $value;
        @media (max-width:575.98px) { &-xs { #{$prop}: $value; } }
        @media (min-width:576px) { &-sm { #{$prop}: $value; } }
        @media (min-width:768px) { &-md, &-td { #{$prop}: $value; } }
        @media (min-width:992px) { &-lg { #{$prop}: $value; } }
        @media (min-width:1200px) { &-xl { #{$prop}: $value; } }
    } 
}
```

**For Example:** writing `@include make-responsive(".d-none", display, none);` will create the following code
```scss
.d-none { display:none; }
@media (max-width:575px) { .d-none-xs { display:none; } }
@media (min-width:576px) { .d-none-sm { display:none; } }
@media (min-width:768px) { .d-none-md { display:none; } }
@media (min-width:992px) { .d-none-lg { display:none; } }
@media (min-width:1200px) { .d-none-xl { display:none; } }
```
Also you can write alias by putting them in the first argument like this ` @include make-responsive(".d-none, .dn, .display-none", display, none) ` and use them like `<p class="d-none-xs"></p>` or `<p class="display-none-xl"></p>`