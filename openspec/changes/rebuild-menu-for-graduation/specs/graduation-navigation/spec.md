## ADDED Requirements

### Requirement: Graduation Sidebar Menu
The sidebar menu must be updated to display a focused "Dự lễ tốt nghiệp" tab instead of the generic university tabs.

#### Scenario: User opens graduation menu
- **WHEN** the user clicks the "Dự lễ tốt nghiệp" tab
- **THEN** it should expand to show: Gửi xe, Dự lễ, Theo dõi lễ, Chụp ảnh, Nghỉ ngơi ăn uống

### Requirement: Graduation Navigation Logic
Clicking an item in the graduation menu should navigate the map to the specific location and show information.

#### Scenario: User clicks "Nghỉ ngơi ăn uống"
- **WHEN** the user clicks "Nghỉ ngơi ăn uống" in the menu
- **THEN** the map pans to the Canteen location AND shows the popup with text: "Căn tin học viện nằm sau hội trường A2, có bàn ghế, quạt, có thể mua nước uống, đồ ăn..."
