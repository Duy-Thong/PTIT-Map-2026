## Why

The current map menu is generalized for all university activities. To better serve the upcoming graduation ceremony, the menu needs to be simplified and focused on essential needs for graduates and their families: parking, ceremony attendance, ceremony viewing, photography, and resting/eating.

## What Changes

- **Menu Refactor**: 
    - Remove 3 existing tabs: "Khối phòng ban", "Đào tạo nghiên cứu", "Tiện ích sinh viên".
    - Keep the "Tham quan học viện" tab.
    - Add a new "Dự lễ tốt nghiệp" tab with localized icons and interactive items.
- **Map Interaction**: 
    - Implement navigation logic: Clicking a graduation item will pan the map to the target location and trigger its popup.
- **New Content**:
    - Add a "Gửi xe" (Parking) hotspot to the map at the lower-left area (as indicated by the user's screenshot).
    - Create/Update detailed popups for:
        - Gửi xe: Parking instructions.
        - Dự lễ: Council/Ceremony hall (HT A2).
        - Theo dõi lễ: Live-stream viewing area (A2 Floor 1).
        - Chụp ảnh: Photo spot (B5).
        - Nghỉ ngơi ăn uống: Resting area (Canteen).

## Capabilities

### New Capabilities
- `graduation-navigation`: Custom menu and navigation logic for graduation events.
- `parking-spot`: A dedicated parking location on the map with specific instructions.

## Impact

- `index.html`: Sidebar menu HTML/JS, Map hotspot definitions.
- `map_mobile.html`: Equivalent mobile UI updates.
- `static/js/scripts.js`: Potential navigation helper functions.
- `static/images/map/`: New icon for the parking spot.
