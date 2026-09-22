# Echelon Signal Engine Boundary

This directory owns application meaning for Echelon Signal.

Production domain state, legal transitions, scoring, validation, privacy rules,
capabilities, obligations, effects-as-data, and view projection belong on this
side of the Limen boundary. The production implementation is F#/.NET WebAssembly.

Browser APIs and DOM authority do not belong here.
