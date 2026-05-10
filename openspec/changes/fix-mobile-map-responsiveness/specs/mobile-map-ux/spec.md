## ADDED Requirements

### Requirement: Marker Scaling
The map markers must be sized appropriately for mobile devices to prevent excessive overlap.

#### Scenario: Marker icon size on mobile
- **WHEN** the viewport width is 768px or less
- **THEN** marker icons (`.prlx-ctn .pop img`) should have a height of 40px

### Requirement: Marker Distribution
Markers must be spaced out enough on mobile to allow for accurate touch interaction.

#### Scenario: Marker clumping prevention
- **WHEN** viewing the map on mobile
- **THEN** markers must maintain a minimum physical distance between each other by adjusting margin offsets
