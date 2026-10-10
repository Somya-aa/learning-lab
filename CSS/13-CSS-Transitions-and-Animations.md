# CSS Transitions and Animations

CSS transitions and animations are used to add movement and visual effects to webpage elements.

They make websites more interactive by allowing elements to change their appearance smoothly or perform animations automatically.

---

## 1. What Are CSS Transitions?

A CSS transition allows a property to change gradually over a specified duration instead of changing instantly.

For example, a button can smoothly change its background color when the user hovers over it.

```css
button {
    background-color: blue;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: green;
}
```

When the user hovers over the button, its background color changes smoothly.

---

## 2. transition-property

The `transition-property` property specifies which CSS property should transition.

```css
.box {
    transition-property: width;
}
```

You can transition multiple properties:

```css
.box {
    transition-property: width, background-color;
}
```

The `all` value can transition all eligible properties:

```css
.box {
    transition-property: all;
}
```

However, transitioning only the properties you need is generally easier to maintain.

---

## 3. transition-duration

The `transition-duration` property defines how long the transition takes.

```css
.box {
    transition-duration: 0.5s;
}
```

Time can be specified in seconds (`s`) or milliseconds (`ms`).

**Examples:**
- `transition-duration: 1s;`
- `transition-duration: 300ms;`

A duration of `300ms` is equal to `0.3s`.

---

## 4. transition-timing-function

The `transition-timing-function` property controls the speed pattern of a transition.

| Value | Behavior |
| :--- | :--- |
| `ease` | Starts slowly, speeds up, then slows down |
| `linear` | Maintains a constant speed |
| `ease-in` | Starts slowly |
| `ease-out` | Ends slowly |
| `ease-in-out` | Starts and ends slowly |
| `cubic-bezier()` | Defines a custom speed curve |

**Example:**

```css
.box {
    transition: transform 0.5s ease-in-out;
}
```

---

## 5. transition-delay

The `transition-delay` property specifies how long the browser waits before starting a transition.

```css
.box {
    transition-delay: 0.2s;
}
```

The transition starts after a delay of 0.2 seconds when the triggering change occurs.

---

## 6. Transition Shorthand

The `transition` property combines several transition settings.

```css
.box {
    transition: background-color 0.3s ease;
}
```

You can also transition multiple properties:

```css
.box {
    transition:
        background-color 0.3s ease,
        transform 0.3s ease;
}
```

This makes the CSS shorter and easier to read.

---

## 7. CSS Transform

The `transform` property changes an element's visual position, size, rotation, or shape.

Common transform functions include:
- `translate()`
- `rotate()`
- `scale()`
- `skew()`

### Translate
Moves an element visually.

```css
.box {
    transform: translate(20px, 10px);
}
```

The element moves 20px horizontally and 10px vertically.

### Rotate
Rotates an element.

```css
.box {
    transform: rotate(15deg);
}
```

### Scale
Changes the visual size of an element.

```css
.box {
    transform: scale(1.2);
}
```

The element becomes 1.2 times its original size.

### Skew
Slants an element.

```css
.box {
    transform: skew(10deg);
}
```

Transforms can be combined with transitions to create smooth effects.

---

## 8. Hover Effects with Transitions

Transitions are commonly used to improve buttons, cards, and links.

### HTML
```html
<button class="btn">Click Me</button>
```

### CSS
```css
.btn {
    padding: 12px 24px;
    background-color: #2563eb;
    color: white;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    transition: background-color 0.3s ease,
                transform 0.3s ease;
}

.btn:hover {
    background-color: #1d4ed8;
    transform: translateY(-3px);
}
```

The button changes color and moves slightly upward when hovered over.

---

## 9. What Are CSS Animations?

CSS animations allow elements to change styles through multiple stages.

Unlike a basic transition, an animation can run automatically and use multiple keyframes.

Animations are created using:
- `@keyframes`
- `animation-name`
- `animation-duration`
- `animation-timing-function`
- `animation-delay`
- `animation-iteration-count`
- `animation-direction`
- `animation-fill-mode`
- `animation-play-state`

---

## 10. @keyframes

The `@keyframes` rule defines the stages of an animation.

```css
@keyframes changeColor {
    from {
        background-color: blue;
    }

    to {
        background-color: green;
    }
}
```

The animation moves from the starting color to the ending color.

It can be applied to an element:

```css
.box {
    animation-name: changeColor;
    animation-duration: 2s;
}
```

---

## 11. Using Percentages in Keyframes

Keyframes can contain multiple stages.

```css
@keyframes moveBox {
    0% {
        transform: translateX(0);
    }

    50% {
        transform: translateX(100px);
    }

    100% {
        transform: translateX(0);
    }
}
```

The animation moves the element to the right and then returns it to its original position.
Percentage values represent points along the animation timeline.

---

## 12. animation-duration

This property specifies how long one animation cycle takes.

```css
.box {
    animation-duration: 3s;
}
```

The animation takes three seconds to complete one cycle.

---

## 13. animation-iteration-count

This property controls how many times an animation runs.

```css
.box {
    animation-iteration-count: 3;
}
```

The animation runs three times.

To repeat it continuously:

```css
.box {
    animation-iteration-count: infinite;
}
```

Use infinite animations carefully to avoid distracting users.

---

## 14. animation-direction

This property controls the direction in which an animation runs.

Common values:
- `normal`
- `reverse`
- `alternate`
- `alternate-reverse`

**Example:**

```css
.box {
    animation-direction: alternate;
}
```

With `alternate`, successive iterations reverse direction.

---

## 15. animation-delay

This property delays the beginning of an animation.

```css
.box {
    animation-delay: 1s;
}
```

The animation starts after one second.
A negative delay can make an animation appear to have already been running when it becomes active.

---

## 16. animation-fill-mode

The `animation-fill-mode` property controls how styles apply before or after an animation.

| Value | Behavior |
| :--- | :--- |
| `none` | Does not retain animation styles outside the active period |
| `forwards` | Retains the final keyframe styles |
| `backwards` | Applies the appropriate starting keyframe styles during the delay |
| `both` | Applies both backwards and forwards behavior |

**Example:**

```css
.box {
    animation: fadeIn 1s ease forwards;
}
```

The element retains the final styles defined by the animation after it finishes.

---

## 17. animation-play-state

This property controls whether an animation is running or paused.

```css
.box {
    animation-play-state: paused;
}
```

To resume the animation:

```css
.box {
    animation-play-state: running;
}
```

This property is useful when implementing interactive animations.

---

## 18. Animation Shorthand

The `animation` property combines multiple animation settings.

```css
.box {
    animation: moveBox 2s ease-in-out 0.5s infinite alternate;
}
```

This specifies:
- **Animation name:** `moveBox`
- **Duration:** `2s`
- **Timing function:** `ease-in-out`
- **Delay:** `0.5s`
- **Iteration count:** `infinite`
- **Direction:** `alternate`

The order of shorthand values matters when interpreting time values.

---

## 19. Complete Animation Example

### HTML
```html
<div class="box"></div>
```

### CSS
```css
.box {
    width: 100px;
    height: 100px;
    background-color: royalblue;
    border-radius: 10px;
    animation: moveBox 2s ease-in-out infinite alternate;
}

@keyframes moveBox {
    from {
        transform: translateX(0);
    }

    to {
        transform: translateX(150px);
    }
}
```

The box repeatedly moves horizontally between two positions.

---

## 20. Transitions vs Animations

| Feature | Transitions | Animations |
| :--- | :--- | :--- |
| **Keyframes required** | No | Yes |
| **Multiple stages** | Limited to property changes between states | Supported |
| **Automatic playback** | Usually triggered by a state change | Can start automatically |
| **Repetition** | Not designed for repeated cycles | Supports repeated cycles |
| **Common use** | Hover and focus effects | Loading indicators and motion effects |

Use transitions for simple state changes and animations when you need more control over the sequence of movement.

---

## 21. Performance Best Practices

- Prefer animating `transform` and `opacity` when possible.
- Avoid unnecessarily animating layout properties such as `width`, `height`, and margins.
- Keep animations short and purposeful.
- Avoid excessive movement that distracts users.
- Use `prefers-reduced-motion` to respect motion preferences.
- Test animations on mobile devices.
- Avoid running too many animations simultaneously.

**Example:**

```css
@media (prefers-reduced-motion: reduce) {
    *,
    *::before,
    *::after {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
        scroll-behavior: auto !important;
    }
}
```

This reduces motion for users who have requested reduced motion in their operating system settings.

---

## 22. Common Mistakes

- **Mistake 1: Forgetting the Animation Duration**
  ```css
  .box {
      animation-name: moveBox;
  }
  ```
  Without a positive duration, the animation generally has no visible active period.

- **Mistake 2: Using Undefined Keyframes**  
  The animation name must match the name defined in `@keyframes`.

- **Mistake 3: Overusing Infinite Animations**  
  Continuous movement can distract users and make a website harder to use.

- **Mistake 4: Animating Too Many Properties**  
  Animating properties that trigger repeated layout calculations can affect performance. Prefer `transform` and `opacity` when they achieve the desired result.

---

## What I Learned

- Transitions create smooth changes between CSS states.
- `transition` is shorthand for transition settings.
- `transform` supports translation, rotation, scaling, and skewing.
- Animations use `@keyframes` to define stages.
- `animation-duration` controls cycle length.
- `animation-iteration-count` controls repetition.
- `animation-direction` controls animation direction.
- `animation-fill-mode` controls styles outside the active animation period.
- Reduced-motion preferences should be respected.

---

## Summary

CSS transitions and animations improve the appearance and interactivity of websites.

- **Transitions:** Smooth changes between states
- **Animations:** Keyframes and controlled motion
- **Transforms:** Move, rotate, scale, or skew elements

Use motion purposefully, maintain good performance, and ensure that animations do not interfere with accessibility.

---

➡️ Previous: [CSS Responsive Design](12-CSS-Responsive-Design.md)

➡️ Next: [CSS Pseudo Classes and Psuedo Elements](12-Pseudo-Classes-and-Psuedo-Elements.md)