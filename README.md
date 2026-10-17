<a href="https://micheledatabeat.github.io/"><img src="assets/databeat-mark.svg" alt="DataBeat" width="40" height="40"></a>

# LUMON OS XL

Musical firmware for the **first-generation Korg Volca Sample**, by
[DataBeat — Michele Ibba](https://micheledatabeat.github.io/).

Build rhythms that change across eight bars, place hits ahead of or behind the
beat, play samples in a scale, and turn a phrase into a repeat, a backcue or a
lo-fi loop.

> ## ➜ Install LUMON OS XL v1.0.2 with Volca Studio XL 1.0.0
>
> **This repository contains documentation only: no firmware, no updater and no
> code.** LUMON OS XL is installed with the free companion application
> **[Volca Studio XL 1.0.0](https://github.com/MicheleDataBeat/volcastudio-xl-releases/releases/tag/v1.0.0)**,
> which builds it on your computer from Korg's own updater:
>
> 1. **Download Volca Studio XL 1.0.0** for Windows, macOS or Linux from its
>    [release page](https://github.com/MicheleDataBeat/volcastudio-xl-releases/releases/tag/v1.0.0).
> 2. **Download Korg's official updater.** On Korg's
>    [volca sample download page](https://www.korg.com/us/support/download/software/0/370/1475/),
>    read Korg's licence agreement and download **System Updater 1.42**
>    (`volcasample_updater_1_42.zip`). Keep it unchanged.
> 3. **Patch it in Studio.** Add the zip in **Reintegration** (WMC),
>    **Severance** (Outie) or **Firmware** (Innie). Studio builds LUMON OS XL
>    v1.0.2, bit-identical to the release, and keeps Korg 1.42 for restoring.
> 4. **Flash it.** Connect the computer to the Volca's **SYNC IN**, power on
>    holding **FUNC + PLAY** until **UPdt** appears, follow Studio's guided
>    update and wait for **End**.
>
> Full step-by-step instructions, checksums and troubleshooting:
> **[Volca Studio XL — Firmware](https://github.com/MicheleDataBeat/volcastudio-xl-releases#firmware)**.

## What it adds

- **Predictability and bar filtering.** Set an eight-bar sequence separately
  for every step of every part, and combine it with four-bar filtering. A kick
  can play on the first bar and rest for seven; another step can alternate.
- **Microtiming, echo and ratchet.** Move individual hits by −15…+15 units of
  1/32 step. Add up to four diminishing echoes or divide a step into four strokes.
- **Intra-bar looping.** Repeat a chosen span of steps before completing the
  pattern. Store the span and repeat count with WRITE. In 1.0.2 the loop keeps
  running while you use LIVE effects.
- **Musical pitch and slicing.** Sixteen SPEED scales, pitch envelopes with
  musical depth and grid-based attack/decay, and sixteen equal sample zones.
  FUNC keeps the free controls available.
- **Live effects.** Octave shifts, a master gate, selected-part beat repeat,
  eight backcue gestures and fading scratch. The most recently pressed effect
  takes over. Backcue and scratch affect all parts.
- **Reverb, lo-fi delay and freeze.** Choose native reverb, a BPM-synchronized
  delay or a captured loop with half speed, double speed and reverse.
  REVERB MIX blends the frozen loop with the direct sound; pad 5 stops the loop.
- **Hands-free FUNC and saved settings.** Press FUNC once to keep it active;
  press it again to turn it off. Step editing remains available, and pattern
  banks can be exported through audio.

The [manual](docs/MANUAL.md) explains every page and control, including how
Predictability counts bars and how to capture or stop freeze. See the
[changelog](CHANGELOG.md) for what changed in each version.

## After installing

1. The startup display reads **LUMON OS**. The version check (power on with REC
   held) can show **1.60**: that is the updater version of LUMON OS XL 1.0.2.
2. Press FUNC, turn SAMPLE/SELECT to choose an extension page, then
   **press FUNC again to enter it**.
3. Use WRITE to save your pattern settings.

Volca Sample 2 is not supported. You do not need to install Korg 1.42 first:
Studio only uses Korg's updater file to build LUMON OS XL.

## Volca Studio XL

[Volca Studio XL](https://github.com/MicheleDataBeat/volcastudio-xl-releases)
installs LUMON OS XL and also prepares sample kits, manages LMX2 pattern banks
and applies groove templates. Choose **Innie** in a Linux terminal, **Outie** on
the desktop or **WMC** in Google Chrome. Pattern audio backup needs a MIDI
output connected to the Volca's MIDI IN and its headphone output connected to a
computer audio input.

## MIDI

LUMON OS XL retains **Korg's original MIDI control and synchronization**.
Pajen's Omni/polyphonic modes, channel-11 sequencer mapping, chromatic MIDI-note
response and extra MIDI controls are not included. LUMON adds a MIDI request
for its audio pattern backup.

## Credits and rights

Thanks to **Pajen** for his pioneering Volca firmware work. His BETA7 bar
filtering, probability, extended-menu workflow and access to the native reverb
choices informed LUMON's design. XL builds on Korg 1.42; BETA7 is a research
reference. Predictability replaces random probability with deterministic
sequences. [Pajen BETA7, hosted by Ranzee](https://ranzee.com/volca-sample-unofficial-firmware/).

LUMON is unofficial research and interoperability work, not affiliated with or
endorsed by Korg. **No open-source or redistribution license is granted.** This
repository distributes no Korg firmware and no LUMON OS XL updater. See
[credits and rights](THIRD_PARTY.md).

[DataBeat](https://micheledatabeat.github.io/) ·
[Volca Studio XL](https://github.com/MicheleDataBeat/volcastudio-xl-releases)
