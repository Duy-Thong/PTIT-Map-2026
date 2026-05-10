## Why

The current mobile version of the PTIT Map (`map_mobile.html`) has significant UI and UX issues. Specifically, the map markers are clustered (clumped) together on narrow viewports, making them difficult to interact with. Additionally, the Graduation Timeline modal is structurally tied to the parallax container, causing it to move incorrectly and lack proper mobile styling (background, positioning, etc.), which results in a broken overlay that overlaps with map content.

## What Changes

- **Structural Isolation**: Decouple the Graduation Timeline modal from the parallax container to ensure it behaves as a stable overlay.
- **Mobile Responsive Styling**: Implement proper CSS for the timeline modal and markers specifically for mobile viewports in `styles_mobile.css`.
- **Marker Optimization**: Scale down marker icons and adjust their relative positioning on mobile to prevent clumping and improve readability.
- **Asset Sync**: Synchronize missing styles from `styles.css` to `styles_mobile.css` to ensure visual consistency.

## Capabilities

### New Capabilities
- `mobile-map-ux`: Enhanced map interaction and marker display optimized for mobile devices.
- `graduation-timeline-overlay`: A stable, responsive modal system for displaying event timelines across all device types.

### Modified Capabilities
- (None)

## Impact

- `index.html`: Structural changes to the timeline modal placement.
- `map_mobile.html`: Structural changes and marker coordinate adjustments.
- `static/css/styles_mobile.css`: Addition of modal styles and marker scaling logic.
- `static/css/styles.css`: Minor consistency updates if needed.
