# Windcress 1.0 TEST
Native Android Nagareru crosswind puzzle. Android 8+ (min26), target35. Package com.gg007.windcress. Twelve original unique boards on a 4x4 grid.

## Rules
Nagareru on a 4x4 grid. Draw one noncrossing directed loop through every gold arrow, straight in its printed direction. Dark arrow tiles are impassable wind sources; wind travels in that direction until the next dark tile or the frame. Never move upstream in a wind-blown cell. If you enter wind from the side, your next step must follow that wind into another white cell. After a downwind step you may turn away. All overlapping winds apply. Other white cells may be unused. Tap gaps to add/remove links; the printed arrows determine the loop direction. Twelve original uniquely solved layouts and twelve different loops; undo/reset, levels and saved palette/wind overlay. Known Nagareru adaptation.

## Download and status
https://mega.co.nz/#!RckjiJwI!YNLn9DIUX1BGBMlwuSVei53wclVBj13LAhHPjx8V-vQ
APK SHA256 0b876a1f55889bc1d07c9b647cc9bb026e3fbac9626b22ac0094db3992649068; 20974 bytes. Original signing certificate SHA256 1651d9e269ece8a76f36ed4bba24ebc50f9de1e5f856e0567e0e8169fcb25597. Anonymous downloaded bytes match. No requested permissions. Original icon unchanged.

## Checks
Portable seed-791110 generator enumerates all 213 undirected and 426 directed cycles of the 4x4 grid. Twelve distinct uniquely solved layouts and loop solutions. Each board has a forced side-entry wind turn and has multiple answers if wind rules are removed, so wind is essential. Independent oracle uses disjoint-set connectivity, directed successor propagation and coordinate-by-coordinate source rays; production walks both cycle orientations and builds per-cell wind bitmasks. All 201,326,592 complete edge-state checks plus 120,000 randomized/invalid wind-arrow cases agree. Bounds, undo/replay/reset and solved lock pass. Actual drawing-adapter midpoint taps solve all twelve and check menu, privacy, levels, next and saved palette/wind-overlay/completion. Seven drawing previews inspected, not phone screenshots. Phone runtime/performance/external-browser QA and full Git source commit remain incomplete. Signed TEST, not final or Play published.

## Functional difference
Reviewed all 210 live studio descriptions and all 803 legacy entries. No wind-forced loop match found. Frostcross requires a directed path across ice patches and permits ice crossings; Windcress has a closed noncrossing loop whose legal entrance/exit pairs depend on ray-emitting wind sources, with forced downwind turns and optional ordinary cells. Gatecress uses gate order, not propagated winds. Known Nagareru adaptation; original generated layouts, code and visuals, not a globally new interaction. Six sources span official Nikoli rules, independent rules, a constructor, a community walkthrough, a playable implementation and cycle-enumeration research. No source layouts, code or art copied. Correction to the prior cycle: Detocress overlaps existing Bendhollow in full-cover loop room-bend totals. It is a working adaptation, not a distinct interaction; the earlier novelty assessment missed that match.
Rules https://www.nikoli.co.jp/en/puzzles/nagareru/ ; independent rules https://ihnnpuzzles.blogspot.com/2024/09/puzzles-662-663-24hpc-loops-nagare-all.html .

## Build
JDK17, Android SDK35/build-tools35.0.0. python generate-levels.py reproduces levels.json. javac -d /tmp/blue-test src/com/gg007/windcress/Board.java BoardTest.java then java -cp /tmp/blue-test com.gg007.windcress.WindBoardTest. bash build.sh makes an unsigned aligned APK unless KEYSTORE_PATH and KEYSTORE_PASSWORD_FILE point to your own private signing material. No signing secret is included.

## Privacy and branding
Windcress runs offline without accounts, ads, analytics, third-party SDKs or requested permissions. Palette, optional wind overlay and solved-board marks stay in this app on your device. Clear app data or uninstall to remove them. The studio link opens your external browser.
GG007 original icon, menu studio https://ilanis-agent.github.io/gg-007-gaming/ and privacy.

## Preservation and publishing
Complete source/APK, exact cumulative 211-card studio and published catalog/studio sources and updater privately preserved at https://files.instinct.com/t38t2qcygdvb-windcress-source-archive . Repository https://github.com/iLanis-agent/windcress holds README only; full Git source commit pending. Existing Jekyll static includes retained without changes; no Pages settings changes or client loader. Both site publications verified separately.
