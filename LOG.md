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

## 2026-06-02 15:40 KST

### Question

- Align the equipped-slot card hierarchy with the inventory card hierarchy.

### Implemented

- Changed equipped-slot cards from horizontal layout to vertical layout.
- Ordered each equipped card as relic icon, star rank, then synergy icons.
- Increased equipped-card height while keeping all three equipped cards inside the panel.

## 2026-06-02 15:45 KST

### Question

- Increase the visual priority of the integrated equipped-synergy summary.
- Distinguish activated synergy stages with circular line colors.

### Implemented

- Replaced small summary pills with larger circular synergy icons.
- Added count badges to the circular icons.
- Applied stage-based circle line colors for 1, 2, and 3 activated copies.

## 2026-06-02 15:46 KST

### Question

- Show integrated synergy activation as a three-segment circular progress line instead of replacing the full line color.

### Implemented

- Changed integrated synergy circles to progress rings.
- Filled one-third of the ring per activated synergy copy.
- Kept the maximum ring state at three activated copies.

## 2026-06-02 15:59 KST

### Question

- Reduce the equipped-slot panel and card widths, then give the saved width to the detail panel.

### Implemented

- Reduced the equipped-slot panel width from `306px` to `260px`.
- Standardized all equipped-slot card widths to `200px`.
- Centered equipped-slot cards inside the narrower panel.
- Expanded the detail panel from `522px` to `568px`.

## 2026-06-02 16:37 KST

### Question

- Expand the inventory to 12 relics without sorting equipped relics to the top.
- Reduce inventory card height from `136px` to `120px`.
- Center the three integrated synergy icons in the equipped-slot panel.

### Implemented

- Added four unowned preview relics and fixed the inventory catalog order independently of equipped state.
- Reduced inventory card height and compacted its internal spacing.
- Centered integrated synergy icons inside the equipped-slot panel.

## 2026-06-02 16:45 KST

### Question

- Keep the integrated synergy progress ring visible when hovering a summary icon.

### Implemented

- Changed the hover state to brighten only the inner circle without replacing the progress-ring background.

## 2026-06-02 16:52 KST

### Question

- Show more than three integrated synergy icons and place the fourth icon on the second row.

### Implemented

- Fixed the integrated synergy summary to a centered three-column grid.
- Added a fourth active synergy to the initial equipped preview state so the second-row layout is visible.

## 2026-06-04 15:18 KST

### Question

- Roll back the two-column integrated layout experiment and return to the three-column layout.

### Implemented

- Restored the latest committed three-column layout because the separated inventory, equipped-slot, and detail columns read better.

## 2026-06-04 15:24 KST

### Question

- Remove the visible synergy point total from the detail panel.
- Make the synergy slot heading match the equipped-effect and owned-effect section titles.

### Implemented

- Hid the visible `X / X pt` label while preserving the internal point calculation.
- Reused the section title styling for the synergy slot heading.

## 2026-06-04 15:31 KST

### Question

- Move relic star rank into the icon area and stop rendering empty star slots.
- Use the same icon rule in inventory, equipped slots, and detail.

### Implemented

- Added filled-only star rendering inside `renderIcon`.
- Removed external star rows from inventory and equipped-slot cards.
- Applied the same icon-with-stars rule to the detail icon.

## 2026-06-04 15:42 KST

### Question

- Prevent duplicate synergy selection within the same relic.
- Center the synergy selection modal title.
- Show current and maximum synergy points in the relic context area.

### Implemented

- Disabled synergies already equipped in another slot and labeled them as equipped.
- Added a duplicate guard before applying a pending synergy.
- Centered the modal header title and moved the close button to the fixed right side.
- Added `used / max pt` display to the modal relic context.

## 2026-06-04 15:49 KST

### Question

- Reduce inventory card height from `120px` to `110px`.
- Align relic icon metadata consistently across inventory, equipped slots, and detail.

### Implemented

- Centered inventory card contents within the shorter card.
- Moved equipped status to the card top-left.
- Moved level chips to the icon top-right and centered star rank at the icon bottom.
- Enlarged the equipped-slot icon and detail icon star rank to match their larger icon sizes.

## 2026-06-04 16:02 KST

### Question

- Keep the synergy selection modal open after applying a synergy.
- Show the stage that will actually apply after the change, based on the equipped build.
- Add three temporary synergies and differentiate synergy visuals by grade.

### Implemented

- Kept the synergy modal open and refreshed it in place after applying a synergy.
- Changed preview stage highlighting to use equipped-build counts instead of only the current relic.
- Added three temporary synergies for wider prototype coverage.
- Applied grade-based color treatment to synergy picks and preview icons.

## 2026-06-04 15:54 KST

### Question

- Allow unavailable synergies to be preview-selected even when they cannot be applied.
- Sort the synergy selection grid by grade so the first row contains the lowest grade synergies.

### Implemented

- Kept all synergy picks selectable for preview and limited only the apply action.
- Sorted modal synergy picks as `일반 -> 고급 -> 희귀`.

## 2026-06-04 16:11 KST

### Question

- Make the promotion modal's equip and owned effect sections match the main detail panel layout.

### Implemented

- Replaced promotion effect rows with the same `stat-title + effect-card` structure used in the main detail panel.
- Kept synergy point and synergy slot comparison rows in their compact promotion layout.

## 2026-06-04 16:18 KST

### Question

- Increase the synergy selection modal height to fit the larger icon layout cleanly.
- Enlarge the star-rank marker inside the modal relic icon.

### Implemented

- Changed the synergy selection modal to a fixed `600px` responsive height and made the internal grid fill that space.
- Increased the modal relic icon star marker size by about 1.2x and adjusted its spacing.

## 2026-06-07 16:36 KST

### Question

- Make promotion modal synergy point and synergy slot comparisons use a distinct compact UI.
- Reduce awkward vertical space in the owned-effect row inside the promotion modal.

### Implemented

- Replaced the promotion modal point and slot rows with separate compact metric cards.
- Tightened promotion modal effect-card spacing so the owned-effect row reads as a clean single line.

## 2026-06-09 16:20 KST

### Question

- Differentiate promotion shard count and upgrade material count inside action gauges.

### Implemented

- Added distinct resource icons to action gauges: shard for promotion and material marker for upgrade.
- Kept the existing gauge layout and progress values while making the owned-resource count easier to identify.

## 2026-06-09 16:42 KST

### Question

- Change synergy stages from cumulative interpretation to highest-stage-only interpretation.
- Make synergy stage UI focus only the currently applied stage.
- Rewrite synergy stage copy so 3-stage effects do not read as comma-separated option lists.

### Implemented

- Updated `시스템_고민.md` to define synergy stages as highest-stage replacement effects.
- Changed synergy stage rendering so only the current stage is active and previous/future stages are secondary.
- Reworked synergy stage data so 3-stage effects use two-line final value plus relic-effect adjustment copy.

## 2026-06-09 17:05 KST

### Question

- Rename synergies around build concepts instead of stat-option labels.
- Make normal synergies pure scaling, advanced synergies conditional scaling, and rare synergies feel distinct without becoming new relic effects.

### Implemented

- Replaced the prototype synergy names with `맹공`, `연격`, `예리함`, `처형`, `수호`, `추격`, `급소`, `파열`, and `폭주`.
- Reworked synergy stage values so highest-stage-only scaling is clearly stronger, such as `연격` reaching `공격 속도 +40%`.
- Updated `시스템_고민.md` to remove the hard requirement that 3-stage effects must include relic-effect adjustment text.

## 2026-06-09 17:18 KST

### Question

- Remove relic effects that use synergy activation as their trigger.
- Make relic equip effects use observable combat situations instead of system-internal events.

### Implemented

- Replaced `낡은 지팡이` and `별의 씨앗` equip effects with time-based combat effects.
- Updated explicit and generated relic equip effects to use clearer combat trigger/result wording.
- Added relic effect design rules to `시스템_고민.md`.

## 2026-06-09 17:40 KST

### Question

- Reduce the visual weight of the dummy relic draw buttons.
- Remove visible inventory and equip-slot title text while keeping panel alignment clean.

### Implemented

- Changed relic draw buttons to two muted 170px buttons in one row.
- Lowered draw-button color contrast and font weight so they read as secondary prototype controls.
- Visually hid the inventory and equip-slot titles while preserving their accessibility labels.

## 2026-06-09 17:48 KST

### Question

- In the synergy selection preview, do not make stage 1 look applied just because a candidate synergy is selected.

### Implemented

- Changed synergy preview stage highlighting to use only currently equipped synergy counts.
- Kept the right-side preview information visible while removing false active-stage styling from unapplied candidates.

## 2026-06-09 21:35 KST

### Question

- Change the detail-panel synergy slots so the effect can be read before opening the selection modal.
- Make synergies on non-equipped relics feel inactive while still showing what they would apply.

### Implemented

- Replaced the detail-panel synergy cards with compact rows.
- Added icon/name on the left and current or equip-preview stage effect text on the right.
- Preserved locked, empty, unowned, and clickable states with the existing synergy slot behavior.

## 2026-06-09 23:26 KST

### Question

- Increase the detail-panel synergy effect description space so it can read as roughly two lines.

### Implemented

- Increased synergy slot row height and spacing.
- Narrowed the icon/name column to give the effect column more width.
- Changed synergy effect text from single-line ellipsis to a two-line clamp.

## 2026-06-09 23:33 KST

### Question

- Remove the stage prefix from the detail-panel synergy slot effect text.
- Move the owned-effect block slightly upward so the detail-panel vertical gaps feel more consistent.

### Implemented

- Changed detail-panel synergy effect rows to show only the effect text.
- Reduced the fixed equip-effect row height and stat-block gap so owned effects sit closer to equip effects.

## 2026-06-09 23:37 KST

### Question

- Change locked synergy slot copy so the first column still reads as an empty slot.

### Implemented

- Updated locked synergy rows to show `빈 슬롯` on the left.
- Moved the unlock requirement into the effect column as `N성 승급 시 해금`.

## 2026-06-10 14:55 KST

### Question

- Make equip-effect percentages increase through upgrade, not only owned-effect values.
- Change unowned relic synergy slot copy to show empty slots and explicit unlock conditions.

### Implemented

- Added upgrade and promotion percentage updates for equip-effect descriptions.
- Added equip-effect next-value preview for owned relics that can still level up.
- Changed unowned synergy rows to show `빈 슬롯` with `획득 시 해금` or `N성 달성 시 해금` conditions.

## 2026-06-10 15:00 KST

### Question

- Adjust `강철의 심장` because its counterattack could trigger too often against dense monster groups.

### Implemented

- Changed `강철의 심장` from a short post-hit attack window to a 4-hit received counter trigger.
- Raised the counter damage to keep the effect meaningful while controlling trigger frequency.

## 2026-06-10 15:08 KST

### Question

- Show upgrade growth as `current(+delta)` instead of `current > next`.
- Keep upgrade growth visible at all times for equip and owned effects.

### Implemented

- Changed equip-effect percentage previews to inline delta badges such as `45%(+1%)`.
- Changed owned-effect percentage previews to use the same inline delta format.
- Removed the condition that only showed upgrade preview when the relic was currently upgradeable.

## 2026-06-10 15:14 KST

### Question

- Apply the same compact delta notation to the promotion modal.
- Show synergy point and synergy slot changes as one-line rows.

### Implemented

- Changed promotion equip and owned effect values to inline delta notation.
- Reworked promotion point and slot comparison cards into two compact one-line rows.
- Used unit-aware deltas for promotion metrics, such as `pt` and `칸`.

## 2026-06-10 15:28 KST

### Question

- Make upgrade and promotion increases target effect values instead of condition percentages.
- Example: `공허의 등불` should increase its attack damage value, not the `체력 30% 이하` condition.

### Implemented

- Changed equip-effect percentage targeting to use the final percentage in the description.
- Kept chance-only effects increasing their chance value, while mixed condition/result effects now increase the result value.
- Verified examples so `30% 이하 ... 35% 피해` targets `35%`, and `25% 확률 ... 12% 보호막` targets `12%`.

## 2026-06-10 16:00 KST

### Question

- 강화석을 유물별 재료가 아니라 공용 재화로 처리한다.
- 승급은 유물별 조각, 강화는 공용 강화석으로 분리해서 두 성장 방식이 비슷하게 보이는 문제를 줄인다.

### Implemented

- 유물별 `upgradeMaterials` 값을 제거하고 공용 `playerUpgradeMaterials` 풀을 추가했다.
- 강화 가능 조건과 강화 버튼 게이지가 공용 강화석 보유량을 보도록 변경했다.
- 강화 시 공용 강화석을 차감하고, 유물 뽑기의 강화석 보상도 공용 풀에 더하도록 변경했다.
- 강화석 획득 토스트에서 특정 유물명을 제거했다.

## 2026-06-10 16:08 KST

### Question

- 장착 시너지 요약 토큰에도 시너지 등급별 색상을 적용한다.

### Implemented

- 요약 토큰에 `normal`, `advanced`, `rare` 등급 클래스를 붙이도록 변경했다.
- 요약 토큰의 원형 진행 링과 아이콘 색상이 등급별 색상으로 보이도록 CSS 변수를 추가했다.

## 2026-06-10 17:06 KST

### Question

- 최고 성급 이후 남는 승급 재료를 어떻게 처리할지 정리한다.
- 캐릭터 수집형 BM이 아니라 유물/장비 BM 기준으로 초과 조각 처리 방향을 다시 잡는다.

### Implemented

- `시스템_고민.md`에 `최고 성급 이후 초과 조각 처리` 문단을 추가했다.
- 초과 조각을 상위 유물 선택권이나 직접 뽑기권으로 연결하면 뽑기 확률 가치가 약해진다는 문제를 기록했다.
- 초과 조각은 새 유물 획득 보정이 아니라 등급별 정련/분해 재료 같은 장비 품질 개선 방향으로 검토하는 것이 적합하다고 정리했다.
- 고액 과금 손실감 완화와 뽑기 확률 가치 보존을 함께 판단 기준으로 남겼다.
