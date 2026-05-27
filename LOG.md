# Work Log

## 2026-05-26

### Done

- Rebuilt `index.html` as a clean UTF-8 single-file prototype to remove broken Korean strings and unstable data literals.
- Restored relic names, synergy names, stat labels, modal labels, and locked-slot copy.
- Polished the prototype presentation with a stronger panel background and clearer state feedback.
- Added modal subtitle context, per-option synergy effect copy, and a `현재 시너지 비우기` action.
- Verified rendered DOM output in headless Chrome and Edge against the local `index.html` file.
- Updated `README.md` to reflect the repaired prototype state and local-server run option.

### Notes

- The prototype still uses placeholder action toasts for `승급`, `강화`, and `장착해제`.
- The current validation confirms successful render and script execution; no separate build step exists yet.

### Next

- Decide whether the next pass should implement real equip/unequip interactions.
- Review emoji icon choices versus any final in-game icon direction.

## 2026-05-26

### Done

- Created the public GitHub repository:
  https://github.com/bigtory-web/Relic_prototype
- Installed and configured Git on this laptop.
- Initialized the local Git repository.
- Added the first `README.md` commit.
- Connected the local repository to GitHub.
- Pushed the project to the `main` branch.
- Repaired and restarted the OneDrive sync app.
- Moved a working copy into the OneDrive project folder:
  `OneDrive/[project folder]/game project/relic_prototype`
- Added this project log for smoother handoff across PCs, accounts, or collaborators.

### Notes

- The active working folder should be:
  `OneDrive/[project folder]/game project/relic_prototype`
- The GitHub remote is:
  https://github.com/bigtory-web/Relic_prototype
- If continuing from another PC, sign in to the same OneDrive account and open the project folder above.
- If continuing from another account or chat, read this file and `README.md` first.

### Next

- Add the real prototype source files.
- Choose the engine/framework and development workflow.
- Add run/build instructions to `README.md`.

## 2026-05-26

### Done

- Added `relic_prototype_prompt.md` as the source prompt for the relic prototype.
- Implemented the first playable prototype in `index.html`.
- Matched the first UI direction with a dark in-game relic management layout.
- Added inventory selection, equipped slot selection, relic detail updates, synergy slot editing, and synergy selection modal behavior.
- Verified the prototype in a local browser server at `http://127.0.0.1:4173/`.

### Notes

- The prototype is a single-file HTML/CSS/JS implementation.
- The current visual direction intentionally follows the dark UI mockup rather than the earlier white-base common guide.
- The first data correction changes the third equipped synergy on `불꽃의 심장` from a 1pt rare synergy to the 1pt normal synergy `공격력 증가`.

### Next

- Review whether duplicate rare synergies should be allowed.
- Decide whether star display and synergy dot display need clearer separation.
- Add any final portfolio-facing polish before using screenshots in the planning document.

## 2026-05-26

### Done

- Centered the fixed `1280 x 720` prototype stage in the browser viewport.
- Reduced heavy font weights outside section titles and primary button labels.
- Stabilized equipped slot cards so selection and icon clicks do not push the layout outside the panel.
- Moved star/ascension display into the equipped relic icon as a `★` badge.
- Removed synergy dot rows from equipped slots.
- Added an equipped synergy summary area under the equipped slots.
- Added duplicate synergy grouping in the summary, such as `치명 강화 x2`.
- Updated synergy slots to focus on the synergy icon and current stage.
- Expanded the synergy selection modal to show all 1/2/3 stage effects.
- Highlighted the currently active stage and marked point-blocked choices as unavailable.

### Notes

- Synergy stage is calculated from the number of copies equipped on the selected relic.
- The dark UI direction remains the active visual direction.
- The equipped slot panel now reserves separate height for slot cards and summary cards.

### Next

- Review stage effect copy and exact numerical values.
- Decide whether the planning document should describe duplicate synergy stacking as the main rule.

## 2026-05-26

### Done

- Expanded the relic catalog from 9 relics to 22 relics.
- Matched the target grade distribution: `N 4 / R 4 / SR 6 / SSR 8`.
- Kept newly added relics as locked/unowned entries so the equipped-slot unlock condition remains unchanged.

### Notes

- The inventory now relies on its internal vertical scroll area for the larger catalog.

## 2026-05-27

### Done

- Allowed unowned relics to be selected from the inventory and inspected in the detail panel.
- Removed relic names from inventory cards and added shard progress in `owned / required` format.
- Removed the synergy box layout from equipped slot cards.
- Added read-only integrated synergy popup from the equipped synergy summary area.
- Added upgrade preview values in the detail panel using `current > next` formatting.
- Implemented upgrade button behavior: level +1, equipped effect increase, owned effect increase.
- Disabled promote, upgrade, and unequip actions for unowned relics.
- Disabled upgrade at max level.

### Notes

- Upgrade values currently use fixed prototype rules: attack +1.0%p, critical rate +0.2%p, owned attack +0.1%p.
- Integrated synergy popup is information-only and does not edit equipped relic synergy slots.

## 2026-05-27

### Done

- Added `장착중` badges to inventory cards for relics currently in equipped slots.
- Replaced plain inventory shard text with a compact shard progress gauge.
- Updated the detail panel owned-effect display from `공격력` to `공격력/체력/방어력` while keeping the upgrade calculation data unchanged.
- Changed the synergy modal to a two-column layout: selectable synergy icons on the left and stage effects on the right.
- Restored the selected synergy icon, name, grade, and required point to the right-side modal preview while keeping current-state and one-line effect copy removed.
- Moved detail shard progress from the top metadata row to a gauge below the relic name.
- Restored equipped relic synergy icons in the main equipped-slot cards without returning to the previous boxed synergy layout.
- Enlarged the detail relic icon and removed the `조각` caption from the detail shard gauge.
- Added the promotion modal flow with before/after comparison for equip effects, owned effects, synergy points, and synergy slots.
- Added star-based synergy unlock rules: 0-1 star opens 2 slots, 2 stars opens 3 slots, and 3+ stars opens 4 slots.
- Changed `불꽃의 심장` to a 1-star, promotion-ready demo state so locked synergy slots are visible on the first screen.

### Notes

- Inventory shard gauge progress is calculated from `shards / requiredShards` and capped at 100%.
- The modal overlay now has an explicit high layer so inventory badges and gauges cannot render above it.
- Promotion currently uses fixed prototype deltas: equip attack +2.0%p, equip critical rate +0.5%p, owned effect +0.3%p.
