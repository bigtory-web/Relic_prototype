# Work Log

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
- Moved star/ascension display into the equipped relic icon as a `★N` badge.
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
