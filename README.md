🐨 Koala Choir Practice Tool

A private, offline voice-part player for choirs. Load a MuseScore or MusicXML file, pick your part, and hear it play back — with lyrics in sync, a mini staff notation display, tempo control, and loop support. No account, no uploads, no server. Everything stays on your device.

Built for the Koala choir in Berlin.


What it does


Plays your voice part from a MuseScore (.mscz) or MusicXML (.xml / .mxl) file
Shows lyrics in sync as each note plays, with the next bar previewed at reduced opacity
Mini staff notation — displays up to 3 voice parts as live sheet music (2 bars on mobile, 4 bars on wider screens), with a moving playhead and lyrics aligned under each note
Tap to hear — while paused, tap the now-playing area to hear the current note; hold to sustain it
Loop any passage — set a bar range and loop it, with a 1-second gap between loops and a clean metronome resync on each repeat
Recent loops — the last 5 loop ranges are saved and shown as one-tap pills so you can re-select them in the next rehearsal
Select bars to practise — check individual measures in the list and play only those bars
Tempo and volume control — slow a passage right down while learning, then bring it back up
Instrument tone — choose from Warm, Pure, Choir/Vocal, Piano, Organ, or Flute synthesis
Metronome — independent BPM timer, stays in sync across loops
Dark mode — toggle in the header, preference saved across sessions
Collapsible sections — onboarding, load score, voice parts, and settings can all be collapsed to reduce page length; state is remembered



How to use it


Get the score file — your conductor shares MuseScore files via the choir Google Drive. Download the .mscz file for the piece you want to practise.
Load it — drag the file onto the tool, or tap to browse. The file is read locally; nothing is uploaded anywhere.
Pick your part — tap your voice (Alto, Tenor I, Bass, etc.). You can select multiple parts to hear them together — useful for checking how your line sits against another voice.
Practise — press ▶ Play all, or tap any bar in the measures list to start from there.
Loop a tricky passage — toggle 🔁 Loop range, set the bar numbers, and press Play loop.


On iPhone / iPad: check the physical silence switch on the side of the phone. If it shows orange, flip it off — or plug in headphones. Safari will not play audio when the device is silenced.


Features in detail

Now playing display

Shows the current lyric or note name large on the left, with the next bar's lyric at reduced opacity on the right. Below that, a mini staff renders the actual notes — treble clef for higher voices, bass clef for lower ones, with lyrics positioned above the staff for bass-clef parts to avoid collision with low noteheads. A dashed purple playhead advances note by note.

Tap to hear

While paused, tap and hold the now-playing area to hear the current note sustained. Release to stop. Playback does not restart — you stay paused and resume manually.

Loop memory

The last 5 loop ranges (e.g. "Bars 9–16") are saved to localStorage and shown as clickable pills under the loop controls. Tap one to restore those bar numbers instantly.

Voice part detection

Part names from the score (Soprano I, Alto, Tenor, Baritone, Bass, etc.) are automatically recognised and given colour-coded dots and abbreviation badges. The staff renderer auto-detects whether each part should use treble or bass clef based on the median pitch of its notes.

Lyric carry-forward

If a note has no lyric assigned (common on tied or sustained notes), it inherits the last lyric seen — so "doo" sustains visually across its tied notes rather than showing a blank.


Supported file formats

FormatExtensionNotesMuseScore 4.msczRecommended — parsed directly, includes all part names and lyricsMuseScore XML.mscxUncompressed MuseScore formatMusicXML compressed.mxlStandard interchange formatMusicXML.xml, .musicxmlStandard interchange format


Technical notes


Single HTML file — no build step, no dependencies to install, no framework
Uses JSZip (loaded from CDN) to unpack .mscz and .mxl archives
Audio synthesis via the Web Audio API — no external audio files
Staff notation rendered as inline SVG, computed from parsed MIDI pitches
Tested on Chrome, Safari (desktop and iOS), Firefox, and Samsung Internet



Hosting

The tool is a single .html file. You can:


Share the file directly — download and open in any browser, works offline
Host on GitHub Pages — push to a repo, enable Pages, share the URL
Drop in Google Drive — share with the choir, they open it in browser


No server, database, or backend of any kind is needed or used.


Privacy

Score files are parsed entirely in the browser. No data leaves your device. There are no analytics, no cookies (beyond localStorage for your own preferences), and no external requests except loading JSZip from cdnjs at startup.


Acknowledgements

Built for the Koala choir, Berlin.
Designed and vibecoded by Gabriela Cotosck.
