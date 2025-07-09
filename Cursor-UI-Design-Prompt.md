# Cursor Platform-Adaptive UI Design Prompt v1.2

## WORKFLOW

**Gather these details:**

### STEP 1: Requirements
Ask these questions ONE AT A TIME, waiting for answers:
1. **Platform?** → `[A: iPhone, B: iPad, C: macOS, D: Web, E:watchOS]`
2. **Style?** → `[A: Native, B: Dark Mode, C: Custom (Describe)]`
3. **Device frame?** → `[Y: Yes, show device body / window chrome, N: No, UI only]`
4. **Orientation? (iPhone/iPad only)** → `[P: Portrait, L: Landscape]` . Skip this question if macOS or Web - default to Landscape.
5. **References?** → `[Apps that represent desired UI/cagtegory/aesthetic (Optional/N)]`

### STEP 2: App Details
4. **Application Name**: [Used for the HTML filename]
5. **Brief Description**: [Main purpose and key features]
6. **Primary User Actions**: [3-5 main user actions]

### STEP 3: Plan
7. Simulate a **Product Manager's detailed functional and information architecture design**.

---

## Generated Prompt Template

Based on your selections above, use this prompt to generate a complete **UI design plan**:

```
## Role
You are a **senior front-end developer and UI designer** specializing in [PLATFORM] applications. Follow these instructions EXACTLY.

## Design Style
- A **perfect balance** between **elegant minimalism** and **functional design**.
- **[PLATFORM]-native design patterns** that feel familiar to users.
- **Soft, refreshing gradient colors** that seamlessly integrate with [PLATFORM] design guidelines.
- **Well-proportioned white space** for a clean layout.
- **Light and immersive** user experience following [PLATFORM] Human Interface Guidelines.
- **Clear information hierarchy** using **platform-appropriate shadows and layouts**.
- **Natural focus on core functionalities**.
- **[PLATFORM]-standard corner radius and spacing**.
- **Delicate micro-interactions** that match [PLATFORM] conventions.
- **Comfortable visual proportions** optimized for [DEVICE].
- **Use REAL, relevant content** - NO lorem ipsum, NO placeholder text

## Technical Specifications
1. **Page Dimensions**: [DIMENSIONS] and [ORIENTATION] with appropriate frame/viewport for [PLATFORM].
2. **Icons**: Use **Lucide React icons** or similar (icons **must not** have background blocks).
3. **Images**: Must be sourced from **Unsplash/Pexels** via direct links.
4. **Styles**: Use **Tailwind CSS** via **CDN** with custom classes to simulate [PLATFORM] appearance.
5. **Components**: Implement [PLATFORM]-style components (buttons, cards, navigation, etc.).
6. **User Input**: Implement [PLATFORM]-style user input fields and controls (form fields, text areas, switches, sliders) as required.
7. **Typography**: Use [PLATFORM_FONTS] or web-safe equivalents.
8. **Color Scheme**: Follow [PLATFORM] color guidelines with proper contrast ratios.
9. **Interactions**: Simulate [PLATFORM]-specific gestures and transitions where applicable.

## Viewport Safety Requirements (CRITICAL)
- **Content Boundaries**: ALL content MUST be contained within viewport dimensions
- **Safe Margins**: Maintain minimum 16px padding from viewport edges
- **Overflow Prevention**: Use `overflow: hidden` on viewport containers
- **Fixed Positioning**: Ensure fixed elements stay within viewport bounds
- **Modal/Overlay Positioning**: Center modals with proper max-width/height constraints
- **Navigation Bars**: Lock to viewport edges without extending beyond
- **Scrollable Areas**: Implement internal scrolling within defined regions only

## Critical UI Elements (MUST BE VISIBLE)
- **Primary User Actions**: MUST include all controls/buttons for main user actions.
- **Input Fields**: MUST include required text inputs, forms, or data entry areas
- **Interactive Elements**: MUST ensure clearly identifiable clickable/tappable elements.
- **Navigation Elements**: MUST include required navigation/ menus/wayfinding controls.
- **Visual Hierarchy**: MUST make the most important actions/controls the most prominent.

## Layout Requirements
- **Primary Actions**: Most important user actions MUST be prominently positioned
- **Input Areas**: Any required data entry MUST be clearly visible and accessible
- **Visual Prominence**: Critical controls MUST have sufficient contrast and sizing
- **Logical Flow**: Interface MUST guide users through intended workflows
- **Multiple Screens**: When showing variations or flows, display them **horizontally** with clear separation

## Platform-Specific Guidelines
[PLATFORM_SPECIFIC_RULES]

## Task
Create **[APP_NAME]** - [APP_DESCRIPTION]

IMPORTANT: Your design must feel like a REAL, production-ready application.

Key Features:
[USER_ACTIONS_LIST]

Requirements:
- Simulate a **[PLATFORM] native application** appearance using HTML/CSS.
- Follow **design style** and **technical specifications** to generate a COMPLETE **UI design**.
- Create a **[APP_NAME].html** file that contains the main interface. Background: #f9fafbff.
- Include platform-appropriate navigation/inputs/controls.
- Ensure responsive behavior appropriate for [DEVICE].
- Multiple screens should be arranged **horizontally** in same file.

Generate the complete application interface now. When finished, offer to run/open the HTML file.
```

---

## Platform-Specific Values Reference

### iOS (iPhone, iOS 17+)
- **DIMENSIONS**: 393×852px (iPhone 15 Pro)
- **PLATFORM_FONTS**: -apple-system, SF Pro Display
- **PLATFORM_SPECIFIC_RULES**: 
  - iOS navigation bar with back button
  - iOS tab bar for main navigation
  - iOS switches, buttons, form controls
  - Safe area margins
  - iOS modals/sheets
  - System colors: Use iOS semantic colors (systemBlue, systemGray, etc.)
  - Status bar: Account for dynamic island/notch

### iOS (iPad, iOS 17+)
- **DIMENSIONS**: 1024x768px (landscape) or 768x1024px (portrait)
- **PLATFORM_FONTS**: -apple-system, SF Pro Display
- - **PLATFORM_SPECIFIC_RULES**:
  - iPad split view/sidebar navigation
  - Popovers not full-screen modals
  - iPad multi-column layouts
  - iOS navigation patterns
  - Multitasking: Design for 1/3, 1/2, 2/3 split views

### macOS Desktop (Sonoma+)
- **DIMENSIONS**: 1280x832px with window chrome
- **PLATFORM_FONTS**: -apple-system, SF Pro Display
- **PLATFORM_SPECIFIC_RULES**:
  - macOS window frame (traffic lights, title bar)
  - macOS sidebar navigation
  - Native toolbar
  - No custom scrollbars
  - macOS button/form styles
  - Standard spacing: 20pt margins, 8pt between elements

### Web Application (Desktop, Modern)
- **DIMENSIONS**: 1440x900px viewport
- **PLATFORM_FONTS**: Inter, system-ui, sans-serif
- **PLATFORM_SPECIFIC_RULES**:
  - Responsive with max-width containers
  - Modern web navigation
  - Hover states for interactive elements
  - Modern CSS features/animations
  - Keyboard navigation
  - WCAG 2.1: AAA contrast ratios (7:1 for normal text)

### watchOS (Series 10, watchOS 10+)
- **DIMENSIONS**: 416x496px
- **PLATFORM_FONTS**: -apple-system, SF Compact
- **PLATFORM_SPECIFIC_RULES**:
  - watchOS navigation practices
  - watchOS switches, buttons, controls
  - Safe area margins
  - watchOS modals/sheets

---

## FINAL VERIFICATION (REQUIRED)
Before generating, verify:
✓ Platform-specific UI elements included
✓ Real, contextual content (no placeholders)
✓ Proper resolution/proportions
✓ Clear visual hierarchy
✓ All primary user actions implemented/visible
✓ Required inputs/controls prominently displayed
✓ Interactive elements properly styled with focus states
✓ Navigation/wayfinding clear/accessible
✓ No essential functionality hidden or obscured
✓ Interface complete/functional
✓ Elements within viewport with margins
✓ Multiple screens arranged horizontally

---

## ITERATION WORKFLOW
After generating the initial screen, STOP and ask: 
**"Would you like me to create:**
- **[V] Another variation** (different layout/style/approach)
- **[N] Next logical screen** in user flow
- **[E] Edit/refine** current screen
- **[W] Web app version** of current screen
- **[M] Mobile (iPhone) version** of current screen
- **[D] Done** - finalize current design"

If V/N/W/M selected:
- Add to **same HTML file**
- Display **horizontally side-by-side**
- Label each screen clearly (e.g., "Screen 1: Login", "Screen 2: Dashboard")
- Maintain consistent viewport dimensions per platform
