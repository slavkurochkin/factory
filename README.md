# Package Router — Smarter Technologies

Interactive demo for the robotic arm package dispatch system.

**Live demo:** https://&lt;your-username&gt;.github.io/&lt;repo-name&gt;

## The Task

Implement `sort(width, height, length, mass)` to route packages to the correct stack:

| Condition | Stack |
|---|---|
| Neither bulky nor heavy | **STANDARD** |
| Bulky OR heavy (not both) | **SPECIAL** |
| Both bulky AND heavy | **REJECTED** |

Where:
- **Bulky**: volume ≥ 1,000,000 cm³ **or** any single dimension ≥ 150 cm
- **Heavy**: mass ≥ 20 kg

## The Function

```js
function sort(width, height, length, mass) {
  const volume  = width * height * length;
  const isBulky = volume >= 1_000_000 || width >= 150 || height >= 150 || length >= 150;
  const isHeavy = mass >= 20;

  if (isBulky && isHeavy) return 'REJECTED';
  if (isBulky || isHeavy) return 'SPECIAL';
  return 'STANDARD';
}
```

O(1) time and space — pure function, no side effects.

## Running Locally

```
open index.html
```

No build step. No dependencies.

## Deploy to GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Your demo is live at `https://<username>.github.io/<repo>/`
