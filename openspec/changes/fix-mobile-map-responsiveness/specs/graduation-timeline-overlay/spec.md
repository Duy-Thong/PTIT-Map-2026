## ADDED Requirements

### Requirement: Modal Stability
The graduation timeline modal must remain fixed relative to the viewport and not move with the parallax map.

#### Scenario: Modal positioning
- **WHEN** the graduation timeline is active
- **THEN** it must be positioned absolutely or fixed outside the parallax container

### Requirement: Visual Clarity
The modal must be clearly legible and visually distinct from the map background on mobile.

#### Scenario: Modal styling on mobile
- **WHEN** the viewport width is 768px or less
- **THEN** the modal should have a solid white background, 90% width, and proper vertical scrolling for content
