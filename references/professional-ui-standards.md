# Professional UI Standards

Priority-ordered rules for production-quality interfaces. Based on UI/UX Pro Max
design intelligence. Follow priority 1-10; higher priority = fix first.

## Priority 1: Accessibility (CRITICAL)

- Color contrast minimum 4.5:1 for normal text, 3:1 for large text
- Visible focus rings on all interactive elements (2-4px)
- Descriptive alt text for meaningful images
- aria-label for icon-only buttons
- Tab order matches visual order; full keyboard support
- Use label with for attribute on all form fields
- Skip to main content link for keyboard users
- Sequential heading hierarchy (h1-h6, no level skip)
- Don't convey info by color alone (add icon/text)
- Support system text scaling (Dynamic Type)
- Respect prefers-reduced-motion
- Meaningful screen reader labels and logical reading order
- Provide cancel/back in modals and multi-step flows
- Preserve system and a11y keyboard shortcuts

## Priority 2: Touch & Interaction (CRITICAL)

- Minimum touch target: 44x44pt (iOS) / 48x48dp (Android)
- Minimum 8px gap between touch targets
- Click/tap for primary interactions; never rely on hover alone
- Disable button during async operations; show spinner
- Clear error messages near the problem
- cursor-pointer on all clickable elements (web)
- Avoid horizontal swipe conflicts on main content
- Use touch-action: manipulation to reduce 300ms tap delay
- Visual feedback on press within 100ms (ripple/highlight/scale)
- Don't block system gestures (back swipe, Control Center)
- Keep primary targets away from notch, Dynamic Island, gesture bar
- Swipe actions must show clear affordance (chevron, label)
- Use movement threshold before starting drag to avoid accidental drags

## Priority 3: Performance (HIGH)

- WebP/AVIF images, responsive srcset/sizes, lazy load non-critical
- Declare width/height or aspect-ratio to prevent layout shift (CLS)
- font-display: swap/optional to avoid invisible text
- Preload only critical fonts
- Inline critical CSS or early-load stylesheet
- Lazy load non-hero components via dynamic import
- Split code by route/feature
- Load third-party scripts async/defer
- Skeleton screens instead of spinners for operations >300ms
- Keep per-frame work under 16ms for 60fps
- Debounce/throttle high-frequency events
- Virtualize lists with 50+ items

## Priority 4: Style Selection (HIGH)

- Match style to product type and audience
- Consistent style across all pages
- Use SVG icons (Heroicons, Lucide), never emojis as structural icons
- Choose palette from product/industry context
- Shadows, blur, radius aligned with chosen style
- Respect platform idioms (iOS HIG vs Material Design)
- Make hover/pressed/disabled states visually distinct
- Consistent elevation/shadow scale for cards, sheets, modals
- Design light/dark variants together
- One icon set/visual language across the product
- Each screen: only one primary CTA; secondary actions subordinate

## Priority 5: Layout & Responsive (HIGH)

- viewport meta: width=device-width, initial-scale=1 (never disable zoom)
- Mobile-first, scale up to tablet and desktop
- Systematic breakpoints (375 / 768 / 1024 / 1440)
- Minimum 16px body text on mobile (avoids iOS auto-zoom)
- 35-60 chars per line mobile; 60-75 desktop
- No horizontal scroll on mobile
- 4pt/8dp incremental spacing system
- Consistent max-width on desktop
- Semantic z-index scale (dropdown/sticky/modal/toast/tooltip)
- Fixed navbar/bottom bar must reserve padding for content
- Avoid nested scroll regions
- Prefer min-h-dvh over 100vh on mobile
- Show core content first on mobile; fold secondary content

## Priority 6: Typography & Color (MEDIUM)

- Body line-height 1.5-1.75
- Line length 65-75 characters
- Consistent type scale (12/14/16/18/24/32)
- Font-weight hierarchy: bold headings (600-700), regular body (400), medium labels (500)
- Semantic color tokens (primary, secondary, error, surface), not raw hex
- Dark mode: desaturated/lighter tonal variants, not inverted; test contrast separately
- Foreground/background pairs meet 4.5:1 (AA) or 7:1 (AAA)
- Prefer wrapping over truncation; ellipsis with tooltip when truncating
- Tabular/monospaced figures for data columns, prices, timers
- Intentional whitespace to group related items and separate sections

## Priority 7: Animation (MEDIUM)

- 150-300ms for micro-interactions; complex transitions under 400ms
- Only animate transform and opacity
- Show skeleton/progress when loading exceeds 300ms
- Max 1-2 animated elements per view
- ease-out for entering, ease-in for exiting
- Every animation must express cause-effect, not just decoration
- State changes animate smoothly, never snap
- Maintain spatial continuity in page transitions
- Prefer spring/physics-based curves for natural feel
- Exit animations shorter than enter (60-70% of enter duration)
- Stagger list items by 30-50ms; avoid all-at-once
- Animations must be interruptible; never block user input
- Crossfade for content replacement within same container
- Subtle scale (0.95-1.05) on press for tappable elements
- Unify duration/easing tokens globally

## Priority 8: Forms & Feedback (MEDIUM)

- Visible label per input (not placeholder-only)
- Error messages below the related field with recovery path
- Loading then success/error state on submit
- Mark required fields
- Helpful empty states with action
- Auto-dismiss toasts 3-5s
- Confirm before destructive actions
- Persistent helper text below complex inputs
- Disabled: reduced opacity (0.38-0.5) + cursor change + semantic attribute
- Progressive disclosure: don't overwhelm upfront
- Validate on blur, not every keystroke
- Semantic input types for correct mobile keyboard
- Show/hide toggle for password fields
- Support autofill (autocomplete attributes)
- Undo for destructive/bulk actions
- Multi-step flows show progress indicator
- Long forms auto-save drafts
- After submit error, auto-focus first invalid field

## Priority 9: Navigation (HIGH)

- Bottom navigation max 5 items with labels
- Drawer/sidebar for secondary nav, not primary
- Back navigation predictable and consistent; preserve scroll/state
- All key screens reachable via deep link/URL
- iOS: bottom Tab Bar for top-level; Android: Top App Bar
- Navigation items need both icon and text label
- Current location highlighted in nav
- Clear primary vs secondary nav separation
- Modals/sheets offer clear close/dismiss
- Search easily reachable; provide recent/suggested queries
- Breadcrumbs for 3+ level deep hierarchies (web)
- Support system gesture navigation without conflict
- Never silently reset navigation stack
- Navigation placement same across all pages
- Dangerous actions (delete, logout) visually separated from normal nav

## Priority 10: Charts & Data (LOW)

- Match chart type to data type (trend/line, comparison/bar, proportion/pie)
- Accessible color palettes; supplement with patterns/textures
- Provide table alternative for screen readers
- Always show legend near chart
- Tooltips/data labels on hover (web) or tap (mobile)
- Label axes with units and readable scale
- Charts reflow on small screens
- Meaningful empty state when no data
- Skeleton placeholder while loading
- Respect prefers-reduced-motion on chart animations
- For 1000+ points, aggregate; provide drill-down
- Locale-aware number formatting
- No pie/donut for >5 categories; switch to bar
- Data vs background contrast minimum 3:1

## Professional UI Rules

### Icons
- Vector-only assets (SVG), never raster PNG that blur
- Consistent icon sizing via design tokens (icon-sm, icon-md, icon-lg)
- Consistent stroke width within same visual layer
- One icon style per hierarchy level (filled OR outline, not mixed)
- Icon alignment to text baseline with consistent padding

### Light/Dark Mode
- Cards/surfaces clearly separated from background
- Body text contrast 4.5:1+ in both themes
- Borders/dividers visible in both themes
- Pressed/focused/disabled states distinguishable in both
- Semantic color tokens mapped per theme
- Modal scrim strong enough to isolate foreground (40-60% black)

### Layout
- Safe-area compliance for fixed headers, tab bars, CTAs
- System bar clearance (status bar, gesture indicator)
- 4/8dp spacing rhythm maintained across all levels
- Long-form text readable on large devices (not edge-to-edge)
- Clear vertical rhythm tiers (16/24/32/48) by hierarchy
- Adaptive gutters by breakpoint
- Scroll content not hidden behind fixed bars
