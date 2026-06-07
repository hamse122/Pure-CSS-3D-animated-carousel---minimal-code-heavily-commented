# Pure CSS 3D Animated Carousel

A minimal, no-JavaScript 3D carousel built with HTML and CSS. Images are arranged in a circle using CSS transforms and rotate continuously for a smooth carousel effect.

## Preview

Open `index.html` in your browser to see the carousel in action.

## Getting Started

1. Clone or download this repository.
2. Add your images to the `png/` folder as `1.jpg`, `2.jpg`, and so on.
3. Open `index.html` in a modern browser (Chrome, Firefox, Safari, or Edge).

No build step or dependencies required.

## Project Structure

```
├── index.html   # Carousel markup and image references
├── style.css    # 3D layout, animation, and styling
└── png/         # Carousel images (1.jpg, 2.jpg, ...)
```

## How It Works

- **3D scene** — `perspective` on `.scene` and `transform-style: preserve-3d` on `.a3d` create the 3D space.
- **Card placement** — Each `.card` is rotated around the Y-axis and pushed outward with `translateZ`, forming a ring.
- **Animation** — The `@keyframes ry` rule rotates the entire ring with `rotateY(1turn)` over 32 seconds.
- **Fade edges** — A CSS `mask` on `.scene` softens the left and right edges.

## Customization

| What | Where | Example |
|------|-------|---------|
| Number of cards | `--n` on `.a3d` in `index.html` | `style="--n: 12"` |
| Card index | `--i` on each `.card` | `style="--i: 0"` (0-based) |
| Rotation speed | `animation` on `.a3d` in `style.css` | `32s` → faster with a smaller value |
| Card size | `--w` on `.card` in `style.css` | `17.5em` |
| Background color | `body` in `style.css` | `#fff3ed` |

When changing the number of cards, update `--n`, add or remove `<img>` elements, and set each card’s `--i` from `0` to `n - 1`.

## Browser Support

Uses modern CSS features: `perspective`, 3D transforms, `aspect-ratio`, and `mask`. Works best in current browsers.

## License

Free to use and modify for personal and commercial projects.
