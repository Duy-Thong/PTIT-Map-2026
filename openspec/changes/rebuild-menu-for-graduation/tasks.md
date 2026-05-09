## 1. Preparation

- [x] 1.1 Generate a modern "Parking" marker icon (SVG or PNG) and save it to `static/images/map/icon_parking.png`.

## 2. Desktop UI Updates (index.html)

- [ ] 2.1 Refactor the `.left-menu-map` sidebar:
    - Keep "Thăm quan học viện".
    - Remove "Khối phòng ban", "Đào tạo nghiên cứu", "Tiện ích sinh viên".
    - Add the new "Dự lễ tốt nghiệp" tab and its 5 sub-items (Gửi xe, Dự lễ, Theo dõi lễ, Chụp ảnh, Nghỉ ngơi ăn uống).
- [ ] 2.2 Add the new parking hotspot `div` (`id="floor-parking"`) with appropriate coordinates to the map container.
- [ ] 2.3 Create/Update `title_tooltip` divs for the 5 graduation items with the requested detailed descriptions.

## 3. Mobile UI Updates (map_mobile.html)

- [ ] 3.1 Apply the same sidebar menu refactor to `map_mobile.html`.
- [ ] 3.2 Add the parking hotspot to `map_mobile.html`, adjusting CSS positions for mobile scaling.
- [ ] 3.3 Ensure popup content is consistent with the desktop version.

## 4. Verification

- [ ] 4.1 Verify that clicking menu items triggers the correct map locations and popups.
- [ ] 4.2 Verify the visual alignment of the new parking spot icon on both PC and Mobile.
