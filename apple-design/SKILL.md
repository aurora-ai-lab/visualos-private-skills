---
name: apple-design
description: Design Apple-platform-inspired apps and interfaces using official Human Interface Guidelines. Use when a user asks for Apple-style UI, iOS/macOS design, Liquid Glass, navigation hierarchy, SF Symbols, app icons, or Apple design resources.
license: Internal-use
metadata:
  source: https://developer.apple.com/design/
---

# Apple Design

Use Apple’s official design guidance as a decision framework, not as a request to copy Apple branding.

## Core review

Before building, make it easy to answer: Where am I? What can I do here? Where can I go next? Establish a clear information hierarchy, predictable navigation, readable labels, and a visible primary action. Separate navigation and controls from the content layer. Align elements to communicate grouping and reading order, while adapting to platform, window size, language direction, keyboard, touch, Dynamic Type, contrast, and reduced motion.

Apply the three HIG principles: hierarchy, harmony, and consistency. Prefer standard platform components and conventions when they fit; do not invent custom controls when a familiar component communicates the action better.

## Liquid Glass

Use Liquid Glass primarily for the functional layer: navigation, tab bars, sidebars, toolbars, and important controls over content. Keep content legible beneath it, use clear glass only over visually rich backgrounds, and avoid applying it broadly to every content card. Standard SwiftUI, UIKit, and AppKit components should provide the material automatically where possible. Test reduced transparency and increased contrast settings.

## Symbols and icons

Use SF Symbols for familiar actions and align symbol weight and scale with the surrounding San Francisco font. Choose rendering mode intentionally (monochrome, hierarchical, palette, or multicolor). Respect symbol availability by OS version and SF Symbols terms; do not use Apple product symbols or confusingly similar symbols as app icons or logos. For custom icons, start from Apple’s grid/templates and keep layers meaningful.

For app icons, use a distinctive simple concept, layered artwork, consistent platform shapes, and Icon Composer for Liquid Glass properties and appearance variants. Export vector layers where possible and let the system apply the mask.

## Output contract

When designing an interface, return:

1. User location, primary task, and next destination.
2. Information architecture and navigation choice.
3. Component map using platform conventions.
4. Visual hierarchy, typography, color, materials, and icon choices.
5. Responsive and accessibility behavior.
6. Implementation notes for the project’s existing framework; do not add dependencies without need.

Use official references when a detail matters:
- HIG: https://developer.apple.com/design/human-interface-guidelines/
- Navigation and search: https://developer.apple.com/design/human-interface-guidelines/navigation-and-search
- Materials: https://developer.apple.com/design/human-interface-guidelines/materials
- Liquid Glass: https://developer.apple.com/documentation/technologyoverviews/liquid-glass
- SF Symbols: https://developer.apple.com/design/human-interface-guidelines/sf-symbols
- App icons: https://developer.apple.com/design/human-interface-guidelines/app-icons
- Icon Composer: https://developer.apple.com/icon-composer/
- Design resources and videos: https://developer.apple.com/design/
