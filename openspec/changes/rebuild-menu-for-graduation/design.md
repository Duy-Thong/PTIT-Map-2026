## Context

The application is a campus map for PTIT. The user wants to pivot the UI for a specific event: Graduation Ceremony. The current menu is too complex for this purpose.

## Goals / Non-Goals

**Goals:**
- Simplify the sidebar menu for graduation attendees.
- Add a specific "Gửi xe" location to the map.
- Implement specialized popups for ceremony-related locations.

**Non-Goals:**
- Completely redesigning the map background image.
- Changing the underlying search logic for other departments.

## Decisions

### 1. Sidebar Menu Update
- **Modification**: Remove the list items for "Khối phòng ban", "Đào tạo nghiên cứu", and "Tiện ích sinh viên" in `index.html` and `map_mobile.html`.
- **New Element**: Add a new `div` with ID `graduation-menu` containing the 5 requested items.
- **Iconography**: Use SVG icons consistent with the existing design for the graduation tab.

### 2. Parking Hotspot Implementation
- **Coordinates**: The hotspot will be placed at approx `top: 75%, left: 25%` (to be refined during implementation based on the `nhà xe` area in the background).
- **Structure**: 
  ```html
  <div class="over people btnFile" id="floor-parking">
      <div class="typewriter"><h6>Nhà xe</h6></div>
      <div class="title_tooltip graduation parking">...</div>
      <div class="pop"><img src="./static/images/map/icon_parking.svg"></div>
  </div>
  ```
- **Image**: A new `icon_parking.svg` will be generated and saved to `static/images/map/`.

### 3. Navigation and Popups
- **Logic**: Leverage the `myFunction(ele)` or similar trigger in `scripts.js` to ensure that clicking a menu item activates the corresponding `title_tooltip` on the map.
- **Content**: Hardcode the requested Vietnamese descriptions into the `des-foor` divs.

## Risks / Trade-offs

- **Coordinate Precision**: Aligning the new hotspot with the background image might require manual adjustments.
- **Responsiveness**: Coordinates in `map_mobile.html` will need separate adjustment to match the mobile background scaling.
