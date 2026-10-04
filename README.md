# PraatDataAnalysis

Praat scripts I used to prepare stimuli for a study on dialectal variation and the perception of English interdental fricatives (/θ, ð/) and lateral liquids. The study compared how 108 listeners identified African American English and Southern White English speakers; the manuscript is under review at the *Journal of Speech, Language, and Hearing Research*.

## Scripts

### `GetWAVsCut.praat`

Cuts a long recording into one WAV file per labeled interval of a TextGrid tier, which is how we turned annotated recordings into individual stimulus files.

- Select a LongSound and its TextGrid (same name) in the Objects window, then run the script.
- Options: which tier and interval range, a margin around each interval (default 0.2 s), and a filename prefix/suffix (e.g. `AD_08_CON_` for speaker and condition).
- Skips empty labels, `xxx`, labels starting with `.`, and `<eps>` (the empty-segment label forced aligners emit).
- Adds a running number instead of overwriting when two intervals share a label.

This is adapted from Mietta Lennes' 2002 script *Save intervals to small WAV sound files* (GPL). My changes are the `<eps>` skip and defaults for our file layout.

### `SaveMultipleFilesInPraat.praat`

Saves every selected Sound object to a folder as `<object name>.wav`, then reselects them. Useful after editing many stimuli in one Praat session.

## Running

Open a script in Praat (Praat → Open Praat script…) and choose Run. The default paths in the forms are Windows-style; change them to your own folder. `SaveMultipleFilesInPraat.praat` joins paths with `\`, so on macOS or Linux change that to `/`.

## License

`GetWAVsCut.praat` keeps the original GPL terms. See the header of each script.
