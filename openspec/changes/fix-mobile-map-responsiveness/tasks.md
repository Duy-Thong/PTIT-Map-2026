## 1. Structural DOM Relocation

- [x] 1.1 Move `#dialog_timeline` and `#black_bg_timeline` in `index.html` from inside `.prlx-ctn` to a direct child of `#web`.
- [x] 1.2 Move `#dialog_timeline` and `#black_bg_timeline` in `map_mobile.html` from inside `.prlx-ctn` to a direct child of `#web`.

## 2. CSS Optimization for Mobile

- [x] 2.1 Copy `.dialog_timeline` and related timeline classes from `styles.css` to `styles_mobile.css`.
- [x] 2.2 Adjust `.dialog_timeline` in `styles_mobile.css` to use `width: 90%`, `left: 5%`, and ensure `z-index` is higher than all parallax layers.
- [x] 2.3 Add a media query in `styles_mobile.css` to scale `.prlx-ctn .pop img` height to `40px` for mobile viewports.
- [x] 2.4 Update marker positions (`#floor-a1`, `#floor-a2`, etc.) in `styles_mobile.css` with increased margin offsets to prevent clumping.
- [x] 2.5 Push all labels down and reduce font size on mobile as per user request.

## 3. Verification and Polish

- [ ] 3.1 Verify that the timeline modal opens/closes correctly on mobile and remains fixed while panning the map.
- [ ] 3.2 Ensure markers are easily clickable and accurately placed relative to the map image.
- [ ] 3.3 Check for any regression in the desktop version of the map.
