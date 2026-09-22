# Echelon Signal Browser Boundary

This directory is the thin browser-facing side of the Limen boundary.

Code here may perform mechanical loading, serialization, transport wiring, and
browser integration through Limen. It must not own or re-derive Signal domain
decisions, scoring, validation, privacy rules, capabilities, or application state.

The generic browser kernel itself is supplied by Limen.
