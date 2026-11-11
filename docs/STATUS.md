# Migration status (2026-11-11)

Source of truth today (LiberNT-LDW, branch `leeway/ribbon-f1`, tip fd84051a4c9):
- `sdk/include/leewayui/` (ribbon.h, frame.h, theme.h, dpi.h)
- `sdk/lib/leewayui/` (ribbon.cpp, frame.cpp, theme.cpp, dpi.cpp, CMakeLists.txt, LEEWAYUI-PROVENANCE.md)
- `modules/rostests/apitests/leewayui/` (ribbon_test)
- Design docs and icons in the hive: `shared/libernt/shell/appframework/` (RIBBON-*.md, icons/)

Consumers in LiberNT-LDW: `dll/win32/shimgvw` (leeway/viewer-ribbon), `base/applications/mspaint` (leeway/paint-ribbon).

Pending (needs owner approval before any move):
1. Choose the integration mechanism for LiberNT (git submodule, vendored snapshot with recorded upstream sha, or subtree).
2. Import the LeewayUI history from LiberNT-LDW into this repository (history-preserving extraction, no rewrite of LiberNT).
3. Switch LiberNT's build paths to the chosen mechanism; then stop developing LeewayUI inside LiberNT.
