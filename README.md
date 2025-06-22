## CSS

**Cascading Style Sheets**

```css
selector {
  property: value;
}
```

* `.special` → All elements with class `special`
* `#special` → One element with ID `special`

**Style Priority (Specificity):**
`inline style > internal style > external style`

---

## Naming Conventions

* Cannot start a name with a number
* Use **kebab-case** (e.g., `main-header`)

---

## Background

### `background-image`

* `url("...")`

### `background-repeat`

* `repeat`, `no-repeat`, `repeat-x`, `repeat-y`

### `background-attachment`

* `scroll` → Image scrolls with the page
* `fixed` → Image stays fixed in place when scrolling

### `background-position`

* `left top`, `right top`, `right center`, etc.
* By pixels: `x px y px`

### `background-size`

* `auto`, `cover`, `contain` (fully visible)

---

## Display

### `display: block`

* Takes full width
* Adds line break
* Respects `margin`, `padding`, `width`, `height`

### `display: inline`

* Fits content width
* No line break
* Does **not** respect `width`, `height`, `margin` (top/bottom), `padding` (top/bottom)
* **Respects** `margin` and `padding` (left/right)

### `display: inline-block`

* Fits content width
* No line break
* Respects `margin`, `padding`, `width`, `height`

### `display: none`

* Removes the element from the DOM (document flow)

### `visibility: hidden`

* Hides the element but it still takes up space

---

## Grouping & Nesting

* **Grouping:** `.one, .two, ...`
* **Nesting:** `div p .product`

---

## Text Styling

### `text-shadow: 0 0 0 red;`

* Adds shadow to text

### `vertical-align`

* Aligns elements vertically in a line

### `text-transform`

* `uppercase`, `capitalize`, `lowercase`

### Spacing

* `letter-spacing` → Space between letters
* `word-spacing` → Space between words
* `line-height` → Space between lines

### `text-overflow: ellipsis`

* Adds `...` at the end of overflowed text

---

## Inheritance

Some properties are inherited from parent elements:

* Inherited: `text-align`, `font-size`
* Not inherited: `padding`, `margin`, etc.

---

## CSS Units

* `px`
* `1em` → Relative to parent
* `1rem` → Relative to root (`<html>`)
* `%` → Percentage relative to parent
* `1vw` → 1% of viewport width
* `1vh` → 1% of viewport height

---

## Clearing Floats

**Solutions:**

* `height`: Not recommended (content may overflow)
* `overflow`: Not ideal (may cut off dropdowns)
* `clear`: Best approach

---

## Positioning

* `static`: Default
* `relative`: Moves relative to its normal position
* `absolute`: Positioned relative to the nearest positioned ancestor (or `<html>` if none)
* `fixed`: Positioned relative to the viewport
* `sticky`: Behaves like `relative` until a scroll threshold is reached, then behaves like `fixed`

---

## Pseudo-Classes

* `:hover`, `:checked`, `:visited`, `:empty`, `:focus`

## Pseudo-Elements

* `::first-letter`, `::first-line`, `::selection`
* `::before`, `::after` → use with `content`

---

## Box Sizing

* `content-box` (default):
  Total width = content + padding + border
  Example: `200 + 20*2 + 5*2 = 250px`

* `border-box`:
  Padding and border included in the element’s width
  Example: `200px (includes padding and border)`

---

## Flexbox

### Parent Properties

* `display: flex`
* `flex-direction`
* `flex-wrap`
* `justify-content` → Default: `flex-start`
* `align-items` → Default: `stretch`
* `align-content` → Default: `stretch`
* `flex-flow: [direction] [wrap]`

### Child Properties

* `flex-grow`: Default `0`
* `flex-shrink`: Default `1`
* `order`: Default `0`
* `flex-basis`: e.g., `300px`
* `align-self`: Overrides `align-items`

---

## CSS Grid

### Parent Properties

* `display: grid`
* `grid-template-columns`: e.g., `repeat(auto-fill, minmax(200px, 1fr))`
* `grid-template-rows`
* `gap: row column;`
* `justify-content`
* `align-content`
* `grid-template-areas`

### Child Properties

* `grid-area`
* `grid-column: start / end` or `span x`
* `grid-row: start / end` or `span x`

---

## Gradient

```css
background-image: linear-gradient(direction || angle, color1, color2, ...);
```

---

## CSS Selectors

* `*` → All elements
* `element` → e.g., `div`
* `element element` → Descendant
* `.className` → Class
* `#id` → ID
* `.parent .child` → Any `.child` inside `.parent` (not necessarily direct)
* `.parent > .child` → Direct child only
* `.classOne.classTwo` → Has both classes
* `.classOne, .classTwo` → Grouping
* `element.classOne` → e.g., `p.classOne`
* `p + div` → `div` immediately after `p`
* `p ~ div` → All `div`s after `p` (siblings)
* `[attribute]` → Elements with the attribute
* `[attribute~="value"]` → Attribute contains word `value`
* `[attribute*="value"]` → Attribute contains substring `value`
* `element[attribute]` → e.g., `div[title]`
* `element[attribute="value"]` → e.g., `div[title="s1"]`
* `:first-child`, `:last-child`
* `:first-of-type`, `:last-of-type`
* `:not(:first-child)`
* `:nth-child(n | even | odd)`
* `:nth-of-type(n | even | odd)`
* `:root`, `:checked`, `:empty`, `:disabled`, `:required`, `:focus`, `::selection`, `::placeholder`

  Question: Can you explain the concept of specificity in CSS?

-------

What’s transform property?
The transform property in CSS is used to apply 2D or 3D transformations to an element, such as rotating, scaling, translating (moving), or skewing it.

---------

 إيه الفرق بين em, rem, و px في CSS؟ وامتى تستخدم كل واحد؟

------

 إزاي الـ Critical Rendering Path بيأثر على سرعة تحميل الصفحة؟


----


 إيه هي الـ Paint & Layout في الـ Rendering Engine؟ وازاي تقلل تأثيرهم على الأداء؟


-----

 إيه الفرق بين z-index والـ stacking context في CSS؟


-----

 إزاي تتأكد إن موقعك Responsive لكل الشاشات؟


-----

✅ Flexbox و Grid (الفرق بينهم، وأفضل استخدام لكل واحد).

