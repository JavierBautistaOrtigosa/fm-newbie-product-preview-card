# fm-newbie-product-preview-card

## The width property when value is auto

-   Why `width: auto;` doesn't stretch?

    -   Because it takes up as much space as the content needs.
    -   It doesn't take all available space.

-   How to fill the remaining space horizontally?
    -   When a parent div container is `display: flex;` and has 2 div container children, then:
        -   One div can be set to have a fixed width, ex: `width:200px`.
        -   The other div can be `flex: 1;`.
        -   This way, the second div can stretch and fill the available space.

## How border-radius Works in CSS

-   `border-radius` property only applies to the element it's set on.

    -   It clips the element's background and it's visible border.
    -   It doesn't clip the child elements such as inner divs, background images or child elements.

-   Apply `overflow: hidden;` to the parent element that has `border-radius`.
    -   The child elements get clipped to the parent's border-radius.

## How to insert an icon into a Button

-   If you have the icon as an image then:

```
<button>
<img src="path-to-your-icon.svg" alt="icon" width="20" height="20">
  Click me
</button>
```

## How to reset a button while keeping accessibility intact

```
button {
  all: unset;
  outline: revert;
}
```
- `all: unset;` completely removes all default styling from the button including:
  - padding, border, background, font and importantly **focus outlines**.
  - The problem is that kills keyboard accessibility, ex: the outline that shows when you use Tab to focus is gone.
- Add `outline: revert;`
  - This restores the browser's default outline behavior, but still removes all other styles.
  - Works well across modern browsers (Chrome, Edge, Firefox, Safari).


## How to make a background image cover the entire `<div>`

```
div {
  background-image: url('your-image.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
```

- `background-size: conver;` Makes sure the image covers the whole div, cropping if necessary.
- `background-position: center;` Centers the image.
- `background-repeat: no-repeat:` Prevents tiling.


https://gist.github.com/MoOx/9137295?permalink_comment_id=4525068#gistcomment-4525068
