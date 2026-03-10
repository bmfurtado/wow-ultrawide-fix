# UltrawideFix 1.4.1-alpha
## Midnight
### Fixed
- Resolved a recurring taint error ("attempt to perform arithmetic on local 'textHeight' — a secret number value tainted by 'UltrawideFix'") triggered when hovering over map Points of Interest. The cursor position hook was returning tainted values by mixing addon variables with real coordinates; it now reads UIParent's position directly from its secure-handler-set geometry, which is untainted.

# UltrawideFix 1.4.0-alpha
## Midnight
### Fixed
- Cutscenes and movies now play at full screen width instead of being clipped to the restricted UI width. Covers all three WoW cutscene systems: in-engine cinematics, pre-rendered video movies, and Lua-driven narrative scenes (added in patch 9.2.5).
- UI elements no longer misplace after exiting vehicles or other override-UI states.
- Resolved a taint error ("secret number value tainted by 'UltrawideFix'") that caused Blizzard's widget system to fail when processing certain tooltips and UI widgets. UIParent is now resized through a secure handler to avoid spreading taint to frame geometry.

# UltrawideFix 1.3.0
## Midnight
### Fixed
 - World map: zooming in no longer uses the incorrect zoom point.

# UltrawideFix 1.2.0
## Midnight
### Fixed
- Edit Mode: Nudging elements with arrow keys no longer causes them to jump to wrong positions.
- Edit Mode: Snapping to grid lines now places elements at the correct position for all anchor sides.
- Edit Mode: Snap preview guide lines now draw at UIParent edges instead of screen edges.

# UltrawideFix 1.1.0
## Midnight
### Fixed
- Dropdown and context menus (e.g. right-clicking unit frames) now render at the correct cursor position when UIParent is restricted.

# UltrawideFix 1.0.0
## Midnight
### New
- First automated release of the addon.