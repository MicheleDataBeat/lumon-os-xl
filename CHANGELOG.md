# Changelog

LUMON OS XL is installed with
[Volca Studio XL 1.0.0](https://github.com/MicheleDataBeat/volcastudio-xl-releases/releases/tag/v1.0.0),
which builds the current version from Korg's own 1.42 updater. Earlier versions
are no longer offered.

## v1.0.2 — 17 October 2026 (current)

- The intra-bar loop set on the LooP page keeps running when LIVE pads are
  pressed, replaced or released. Returning to LooP preserves the interval and
  the remaining passes.
- WRITE re-arms the saved loop without cancelling a held LIVE effect.
- Pattern format LMX2 and the existing OFF, step-jump, Stop and load
  behaviour are unchanged. Tested on a physical Volca.

## v1.0.1 — 15 October 2026

- LIVE pads 1–2 lower or raise every sounding voice by one octave (in v1.0
  they affected the selected part). Pressing, replacing or releasing an octave
  pad takes effect immediately, including samples already playing.
- Pad 3 stays the stereo master gate; pads 4–7 stay selected-part repeats.
- Saved samples, patterns, motion and the LMX2 format stay compatible.
  Reverb, delay and freeze audio already captured keeps its playback rate.

## v1.0 — 14 October 2026

- Predictability ALL/P.01–P.15 per step and part, combined with bar filtering.
- ±15 microtiming, echo, ratchet and saved intra-bar looping.
- Sixteen SPEED scales, musical pitch-envelope depth, grid attack/decay and
  sixteen equal sample zones; FUNC retains free controls.
- Latched FUNC while preserving STEP editing.
- A sixteen-pad LIVE page: octave shifts, gate, beat repeat, eight backcue
  gestures and fading scratch, with newest-press priority.
- BPM-synchronized lo-fi delay and freeze alongside native reverb, with a
  MIX-controlled return, a dedicated stop pad and speed/reverse controls.
- New settings saved with WRITE, and audio pattern backup.
