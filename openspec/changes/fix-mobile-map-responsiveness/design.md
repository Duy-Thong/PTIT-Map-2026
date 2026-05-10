## Context

The mobile map currently suffers from marker clumping and a broken timeline overlay. The timeline modal is nested within the parallax layers, causing it to inherit unwanted transformations and movement. Styling for the modal is missing in the mobile-specific CSS file, leading to a transparent, unformatted display.

## Goals / Non-Goals

**Goals:**
- Move `#dialog_timeline` and `#black_bg_timeline` to a stable position in the DOM.
- Scale down marker icons to fit mobile screens without overcrowding.
- Reposition markers on mobile to ensure sufficient tap targets.
- Ensure the timeline modal has a professional look with a solid background and clear typography on mobile.

**Non-Goals:**
- Redesigning the entire parallax engine.
- Adding new map features or data points.
- Modifying the desktop version (`styles.css`) unless necessary for shared logic.

## Decisions

- **DOM Relocation**: Move the timeline modal and its background overlay out of the `.prlx-ctn` div. This prevents the parallax library from applying 3D transforms to the modal, ensuring it remains fixed relative to the viewport.
- **CSS Porting**: Extract `.dialog_timeline` related styles from `styles.css` and paste them into `styles_mobile.css`, with adjustments for small screen widths (e.g., changing width from 70% to 90%).
- **Marker Scaling**: Add a media query or mobile-specific rule to reduce the height of `.prlx-ctn .pop img` from 64px to 40px on devices with `max-width: 768px`.
- **Marker Spreading**: Update the `margin-top` and `margin-left` values for `#floor-*` elements in `styles_mobile.css` to better utilize the available screen space.

## Risks / Trade-offs

- **Coordinate Sensitivity**: Adjusting marker margins manually might require fine-tuning to ensure they still point to the correct visual locations on the map image.
- **CSS Maintenance**: Duplicating styles between `styles.css` and `styles_mobile.css` increases maintenance surface, but is necessary due to the project's structure of separate HTML/CSS files for mobile.
