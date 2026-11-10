# Design QA — pierwszy ekran

- Source visual truth: `C:\Users\adelk\AppData\Local\Temp\codex-clipboard-48f2d68a-c1c8-48e6-8691-0c287f3f05d6.png`
- Implementation screenshot: `implementation-qa.png`
- Combined comparison: `design-qa-comparison.png`
- Viewport/state: desktop, 1065 × 838 px, initial scroll position
- Source pixels: 1065 × 838
- Implementation comparison crop: 1065 × 838
- Density: compared at equal output pixel dimensions; browser capture reported DPR 1.25

## Full-view comparison

The first-screen composition uses the same supplied image assets, white background, navigation copy, pool and dog crops, intro text, duck joke, mixed-font title, yellow stripe, lower running dog, warning copy, pink STOP block, and small caption.

## Focused comparison

No separate focused crop was required because all typography and image edges remain legible in the full 1065 × 838 comparison.

## Comparison history

1. P1: the warning copy had been shortened and the lower dog was outside the recreated composition. Fixed by restoring the full copy and treating the dog/warning as part of the first screen.
2. P2: the title and warning heading inherited oversized later-section typography. Fixed with screen-specific desktop sizes and line heights.
3. P2: the page was centered using an internal 850 px frame rather than the visible composition. Fixed by measuring positions from the selected 1065 × 838 source and applying a dedicated desktop frame.

## Fidelity surfaces

- Fonts and typography: Oswald, Sarpanch, Inconsolata, Trebuchet-style accented letter, weights, line heights, and mixed title treatment preserved.
- Spacing and layout rhythm: positions measured from the selected desktop screenshot; lower warning remains within the same first-screen composition.
- Colors and tokens: white, yellow, pink, blue, and existing green image outlines preserved.
- Image quality: original supplied `t1.png`, `m1.png`, `kaczuszka.png`, and `t3.png` used without generated replacements.
- Copy/content: source wording restored, including spaced `C A Ł O W A Ć?` and `[P JAK PIES]`.

## Residual P3

- Browser font rasterization may differ slightly from the Webflow capture.

final result: passed

## Responsive QA

- Mobile viewport checked at 393 × 852 px.
- Tablet viewport checked at 834 × 900 px.
- Mobile: hero stacks into two image columns, intro and title remain readable, warning section stacks vertically, later copy uses reduced type, mint interlude is enabled, and full photographs fit the viewport.
- Tablet: hero retains the two-column relationship, warning image/copy use a balanced 45/55 grid, and later sections keep readable line lengths.
- No app-authored JavaScript is present; navigation anchors remain functional.
- Desktop source-matched rules begin at 1025 px and were not altered by the tablet/mobile pass.
