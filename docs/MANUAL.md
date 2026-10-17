# LUMON OS XL v1.0.2 — manual

For the first-generation Korg Volca Sample. Version 1.0.2 identifies itself as
LUMON OS at startup. Install it with
[Volca Studio XL](https://github.com/MicheleDataBeat/volcastudio-xl-releases#firmware). This manual describes firmware **1.0.2**.

A [DataBeat](https://micheledatabeat.github.io/) project.

## FUNC and extension pages

Press FUNC once to keep it active; press it again to turn it off. With STEP
active, the pads remain steps to edit while FUNC modifies the knobs.

To access extension pages:

1. Press FUNC to activate it.
2. Turn SAMPLE/SELECT to choose a page.
3. **Press FUNC again to enter the page.**
4. Press FUNC to leave the page. FUNC is now active; press it once more to
   return to ordinary controls.

| Page | SAMPLE/SELECT | Pads |
| --- | --- | --- |
| PrEd | Change Predictability of held steps | Hold steps to edit |
| Bar filtering | — | Toggle excluded bars; groups of four repeat the same four bars |
| rb.ty | Programs 0–2 reverb, 3 delay, 4 freeze | Duration and freeze controls below |
| tIME | Adjust microtiming of held steps | Hold steps to edit |
| ECho | 0–4 additional triggers | Pads 1–8 select interval |
| rAtC | 1–4 strokes | Pads 1–4 select strokes |
| LIVE | — | Hold a performance effect |
| LooP | OFF or 1–16 total passes | Hold the first and last steps of the interval |
| SCAL | Scale 0–15 | Pads 1–16 select scales |

## Predictability and bar filtering

For example, put a kick on step 1 and set that step to P.03. You hear it on
bars 1 and 5 of each eight-bar cycle. Set another kick step to ALL and it plays
on every bar, unless bar filtering excludes it.

Predictability is stored separately for every step of every part. Its sequence
runs across eight logical pattern bars and then repeats. `X` plays that step;
`0` skips that occurrence. All parts share the same bar phase.

| Setting | Bars 1–8 |
| --- | --- |
| ALL | `XXXXXXXX` |
| P.01 | `X0000000` |
| P.02 | `0000000X` |
| P.03 | `X000X000` |
| P.04 | `000X000X` |
| P.05 | `X0X0X0X0` |
| P.06 | `0X0X0X0X` |
| P.07 | `XXX0XXX0` |
| P.08 | `0XXX0XXX` |
| P.09 | `X000X0X0` |
| P.10 | `X0X0X000` |
| P.11 | `X0X000X0` |
| P.12 | `XXX0X0X0` |
| P.13 | `0XXX0X0X` |
| P.14 | `0X0X0XXX` |
| P.15 | `000X0X0X` |

Select the part before opening PrEd. Hold one or more step pads and turn
SAMPLE/SELECT: each held step advances or retreats through ALL and P.01–P.15.
The display shows the setting of the lowest held step. Turning without held
steps changes nothing. Releasing a pad does not toggle its setting. Editing a
silent step does not add a note. WRITE saves all 160 choices with the pattern.
Initialization restores ALL.

Bar filtering independently excludes the selected part in any of four bars.
The original sequenced note must pass **both** filters. Echoes and ratchets
play only when that original note passes; a skipped note creates no repetitions. Exclusive hi-hat priority is resolved after filtering, so an excluded open hat does not
suppress an admitted closed hat.

Stop/Start restarts the sequence at bar 1. An intra-bar loop advances the bar
phase only after the complete expanded phrase; internal returns keep the same
phase. Live beat repeats and manual triggers remain independent of these
sequencer filters.

## Microtiming, echo and ratchet

Select the part before opening one of these pages.

On tIME, hold one or more step pads and turn SAMPLE/SELECT to move those hits
earlier or later: −15…+15 units of 1/32 step. Zero keeps native timing. Each
step has its own value. The offset follows that step's duration, including
swing. A very short preceding step can limit how early a hit can play.

On ECho, turn SAMPLE/SELECT to choose 0–4 additional triggers, each quieter
than the last. Press a pad to set the time between triggers:

| Pad | Interval in step durations | Note value without swing |
| --- | --- | --- |
| 1 | 1/2 | 1/32 |
| 2 | 1 | 1/16 |
| 3 | 2 | 1/8 |
| 4 | 3 | Dotted 1/8 |
| 5 | 4 | 1/4 |
| 6 | 6 | Dotted 1/4 |
| 7 | 8 | 1/2 |
| 8 | 16 | One bar |

The interval uses the original note's step duration, including swing. Echo
count and interval apply to the whole selected part, rather than individual
steps. Echoes retain the original note's captured parameters.

On rAtC, press pad 1, 2, 3 or 4 to select one, two, three or four strokes within
a step; turning SAMPLE/SELECT selects the same values. This is a per-part
setting. One stroke is the original note, with no added strokes.

WRITE saves per-step microtiming and per-part echo/ratchet settings with the
pattern. Dense combinations can lose echoes or run out of voices; the
instrument cannot play an unlimited number of overlapping notes.

## Intra-bar loop

Open LooP, then hold the first and last desired steps together. The outermost
held pads define an inclusive interval; one pad selects a single step. Turn
SAMPLE/SELECT for the total number of passes, including the first.

Steps 1–8 with three passes produce `1…8, 1…8, 1…8, 9…16`. The complete
expanded phrase repeats. One pass adds no repeats; turn below one for OFF.
The interval remains visible while OFF. New patterns default to steps 1–8,
three stored passes, OFF. WRITE stores interval, count and enabled state.

### Loop boundaries and interruptions

Edits take effect after the next already-selected boundary. A return whose
negative-microtiming notes already sounded can finish before OFF takes effect.
An interval without enabled steps is bypassed. Native step jumps and pending
pattern/song changes take priority. Stop/Start and pattern load recall the
stored settings. WRITE and audio backup suspend and subsequently rearm the loop,
unless a native step jump or explicit loop cancellation has cancelled that
activation. LIVE effects preserve the configured loop and its remaining passes.

## Scales, pitch envelope and sample zones

SCAL maps semitone-mode SPEED to a scale relative to the sample's original
pitch. It does not identify or tune the root note. FUNC+SPEED is continuous.
WRITE saves all ten parts' choices.

| Number | Scale |
| --- | --- |
| 0 | Chromatic |
| 1 | Major / Ionian |
| 2 | Natural minor / Aeolian |
| 3 | Dorian |
| 4 | Phrygian |
| 5 | Lydian |
| 6 | Mixolydian |
| 7 | Locrian |
| 8 | Harmonic minor |
| 9 | Melodic minor, ascending |
| 10 | Major pentatonic |
| 11 | Minor pentatonic |
| 12 | Minor blues |
| 13 | Whole tone |
| 14 | Diminished, whole–half |
| 15 | Diminished, half–whole |

PITCH EG INT selects approximately −24…+24 semitones, with zero at the center.
ATTACK and DECAY use the following eight knob regions. FUNC retains free time.

| Display code | Duration |
| --- | --- |
| 0 | Instant |
| 1 | 1/16 |
| 2 | 1/8 |
| 3 | Dotted 1/8 |
| 4 | 1/4 |
| 5 | Dotted 1/4 |
| 6 | 1/2 |
| 7 | One bar |

Divisions follow the straight clock before swing. Stored values stay free until
edited; WRITE, motion and held-step editing preserve grid/free choices. The
envelope moves continuously between its endpoints, independently of the scale.

FUNC+START and FUNC+LENGTH choose start/end zones from sixteen equal divisions
of the sample. End cannot precede start. Ordinary knobs retain continuous
sample controls. WRITE and motion preserve the zone choices.

## Live performance

Select a part, enter LIVE, then hold a pad. Pads 1–3 and 8–16 affect the whole
performance; pads 4–7 repeat only the selected part.

| Pad | Effect |
| --- | --- |
| 1 | All sounding parts one octave down (half playback speed) |
| 2 | All sounding parts one octave up (double playback speed) |
| 3 | Gate the stereo master for the second half of each swung step |
| 4–7 | Selected-part beat repeat at 1/8, 1/16, 1/32 or 1/64 |
| 8 | Global backcue, 1/2 note, return at next bar |
| 9 | Global backcue, 1/4 note, return at next bar |
| 10 | Global backcue, 1/8 note, return at next bar |
| 11 | Global backcue, 1/16 note, return at next bar |
| 12 | Global backcue, 1/2 note, return at next qualifying sequenced note |
| 13 | Global backcue, 1/4 note, return at next qualifying sequenced note |
| 14 | Global backcue, 1/8 note, return at next qualifying sequenced note |
| 15 | Global backcue, 1/16 note, return at next qualifying sequenced note |
| 16 | Global scratch: repeated 1/16 braking with decreasing volume |

Pressing another LIVE pad replaces the current effect. Releasing the winning
pad ends it, subject to the backcue and scratch return rules below; it does not
reactivate an older pad still held.
Simultaneous new presses choose the lowest pad. Page exit, Stop, pattern load,
initialization and backup cancel LIVE. These performance settings are temporary.

Pads 1–2 change all sounding voices immediately, including fading
retrigger tails, and preserve each note's pitch envelope and captured SPEED.
Releasing either octave pad immediately restores normal playback speed without
restarting samples or changing pattern/motion values. Existing reverb, delay and freeze history
keeps its own playback rate. Samples still stop at their native endpoints.

Beat repeat starts at the next actual step boundary and follows swing. It
replaces the selected part's sequenced triggers, echoes and ratchets while held,
using current sample parameters. Other parts keep playing. Mute and native
voice/choke rules remain active. Late service skips missed subdivisions.
LIVE effects run over the configured intra-bar loop. Pressing, replacing or
releasing a LIVE pad, and returning to LooP, preserve the interval and remaining
passes. Enabling or changing an enabled loop still cancels LIVE.

Backcue reverses individual sample cursors and slows to zero over the selected
straight division. The duration is taken from the clock when the pad is pressed,
before swing: at 120 BPM, 1/2, 1/4, 1/8 and 1/16 last 1000, 500, 250 and 125 ms.
Releasing pads 8–15 before braking finishes restores playback immediately.
After a full brake, pads 8–11 mute until the next native bar; pads 12–15 mute
until the next original sequenced note that passes Predictability and bar
filtering and belongs to an enabled, unmuted part with an available sample and
nonzero volume. Playback returns at that note's scheduled time, including
microtiming. A note suppressed by the exclusive hi-hat rule does not reopen
playback. Echoes, ratchets, manual triggers and beat repeats cannot reopen it. Either
automatic return works even if the pad remains held; release and press again
to rearm.

Pad 16 restarts the braking ramp every straight 1/16 while held. Global volume
is 100%, 87.5%, 75%, 62.5%, 50%, 37.5%, 25% and 12.5% over the first eight
cycles, then zero. It stays active and silent while held. Releasing it waits
for the next qualifying original sequenced note described above, restoring
normal direction, speed and volume there. Unlike pads 8–15, a brief scratch
release also waits for that note. Scratch repeats the brake on the current voices: it does
not capture audio, reset sample positions or restart ended voices.

Samples that reach their endpoints end normally; returning from either effect
cannot revive them. Non-looped slices may reverse beyond the selected slice
within the original sample; looped slices retain their bounds. The scratch
volume control affects the stereo master, including an active reverb, delay or
freeze tail. Page exit, Stop, pattern load, initialization and backup force a
normal return without waiting for a musical boundary.

### Moving from 1.0

In 1.0, LIVE pads 1–2 affected only the selected part. In 1.0.1 they affect all
sounding voices. Pad 3 remains the stereo master gate, and pads 4–7 remain
selected-part repeats. Stored patterns and samples use the same formats.

## Reverb, lo-fi delay and freeze

The display names this page **rb.ty**. Press FUNC, use SAMPLE/SELECT to choose
rb.ty, then **press FUNC again to enter**. Turn SAMPLE/SELECT inside the page:
programs 0–2 are native reverbs, 3 is mono lo-fi delay, and 4 is freeze. They
are exclusive: only one of these programs runs at a time. LIVE can operate
alongside it. Delay and freeze receive the **mono effect send**, not a
recording of the entire stereo mix. Parts without their effect send enabled
remain audible directly but do not feed delay or freeze.

### Try delay, then capture a loop

1. Choose a part with an audible sustained sound or a busy rhythm. Outside the
   extension pages, turn STEP off. If this part's effect send is off, press FUNC,
   hold **PART >**, press the pad for that part (1–10), release PART >, then
   press FUNC to turn it off. This toggles the send: do not repeat it if the
   send is already on.
2. Set REVERB MIX around its middle position. Enter rb.ty and choose program
   **3**. Start the sequencer and press **pad 2** for a two-step delay.
3. Choose program **4**, then press **pad 4**. Freeze captures four steps from
   the next step boundary and repeats that fragment. Use a sound that continues
   through that window; a short window between sparse notes may capture silence.
4. Press pads **9–12** to change the existing fragment's speed or direction.
   Press transport STOP to hear the loop without the sequencer. Lower MIX to
   zero, then raise it: the same fragment returns.
5. Press **pad 5** to stop the frozen loop. MIX and the speed/reverse controls
   do not restart a loop stopped this way.
6. To capture again and resume, start the sequencer and press one of **pads
   1–4**. These pads request a new recording; pads 9–12 keep the existing one.

With freeze (program 4), REVERB MIX sets the balance between the direct sound
and the frozen loop. At zero, you hear only the direct sound. Turn it up to add
more of the frozen loop; the direct signal remains present. MIX does not
change the capture or stop its playback. You can capture with MIX at zero and
hear that loop when you raise it. Programs 0–3 retain their native MIX/send
behavior.

Pads 1–4 select one, two, three or four straight steps: a sixteenth, eighth,
dotted eighth or quarter note. At 120 BPM these are 125, 250, 375 and 500 ms.
Delay defaults to two steps, freeze to one. Longer windows automatically reduce
storage sample rate. Tempo-change artifacts are intentional lo-fi behavior.
With freeze selected, pressing any of pads 1–4 requests a new capture starting
at the next actual step boundary; pressing the selected duration again also
recaptures. A short window can capture silence between sparse notes: use pad 4
with a sustained sound or a busy rhythm to include audio reliably.

| Freeze pad | Action |
| --- | --- |
| 1–4 | Select duration and capture a new fragment; resume after pad 5 |
| 5 | Stop the frozen loop and cancel a pending capture, keeping program 4 selected |
| 9 | Play the existing fragment at half speed |
| 10 | Play the existing fragment at normal speed |
| 11 | Play the existing fragment at double speed |
| 12 | Toggle reverse on the existing fragment |

Pads 9–12 **do not request a new capture**. They transform the same captured
audio, including while the sequencer is stopped. Pad 15 indicates pending
capture; pad 16 indicates an unavailable clock/window. Unsupported capture
requests retain the last valid audio state.

Transport STOP retains an active captured loop. Restart requests a new capture
with the selected controls. In contrast, **pad 5 keeps freeze stopped** through
transport Stop/Start, page exit and changes to speed/reverse; only a new capture
from pads 1–4 resumes it; selecting program 4 again also arms a new capture.
To stop the effect quickly, use pad 5 rather than
changing algorithm. Switching algorithm also clears the buffer. Audio backup
clears effect history: delay resumes empty and an active freeze needs a new
capture, retaining the selected controls; a pad-5 stop remains stopped.

## Storage and companion software

Use the native WRITE operation to save pattern settings. Predictability and
microtiming belong to each step; bar filtering, echo, ratchet and scale choices
belong to each part; intra-bar loop settings belong to the whole pattern.
LIVE gestures and captured effect audio are temporary and are not saved by
WRITE. Initialization establishes defaults; selecting a part or opening a page
does not save automatically.
LUMON OS XL uses LMX2 pattern storage. [Volca Studio XL](https://micheledatabeat.github.io/volcastudio-xl-releases/)
Innie, Outie and WMC support its banks, groove editing, reset and audio
export/restore, including P.01–P.15.
Samples and global settings remain separate from pattern banks.

## MIDI

Standard Korg MIDI control and synchronization remain available. Pajen's Omni,
polyphonic and channel-11 modes, chromatic MIDI-note response and additional
MIDI controls are not included. Studio uses MIDI to request an audio pattern
backup and, optionally, reset the current edit buffer.
