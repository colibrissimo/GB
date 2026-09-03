# GB

English teaching material for the Bioengineering (SAB) classes at IUT — interactive HTML activities, pronunciation practice, and games.

Files here are self-contained: one HTML file, CSS and JavaScript inline, no external dependencies. That is deliberate. It means any file can be embedded in Moodle or opened straight from disk, and nothing breaks when a CDN changes its mind.

## What's in here

| File | What it is |
|---|---|
| `index.html` | Beer Brewing Process — an interactive scene. Click an area of the brewery to get the term, its pronunciation, and where it sits in the process. |
| `brewery.png` | The scene image used by `index.html`. |
| `pronunciation/schwa/` | The schwa module, with a Food science bank and a Brewing bank on a switch. Serves SAB2 S3 session 2. |
| `pronunciation/transparent-words/` | Words French and English share on the page and not in the mouth. Coffee menu at the centre. SAB2 S3 session 1. |
| `pronunciation/h/` | The /h/ sound: saying it, not saying it, and not inventing one. Beer words throughout. SAB3 S5 session 1. |
| `pronunciation/silent-r/` | The written r that is not pronounced, and the linking r that comes back. SAB3 S5 session 3. |

## Where it's used

**SAB Year 3, Semester 5** runs the brewing thread — history of beer, how beer is made, the brewing process, describing a beer, and a crowd-funding pitch at the end. `index.html` belongs to the brewing process session.

**SAB Year 2, Semester 3** covers food science and biotechnology.

Both years carry a pronunciation strand running underneath the topics. Material for it arrives here as it's built.

## House rules

- **British English in the prose, American English in the CSS.** `colour` in what students read; `color` in the stylesheet. CSS silently discards British spellings — `text-align: centre` doesn't fail loudly, it just doesn't centre anything.
- **Keep files self-contained.** Inline the CSS and JS; embed images as files in the repo rather than hotlinking.
- **Assume Moodle.** Anything added here should survive being embedded in an iframe.
- **Lowercase paths.** GitHub Pages is case-sensitive, so `Pronunciation/` and `pronunciation/` are different URLs and the wrong one 404s with no error anyone will notice. Everything web-facing stays lowercase.

## Audio

Pronunciation clips live beside their module, as `<module>/assets/audio/<key>.mp3`.
The key is generated from the button's own text: lowercase, apostrophes dropped,
every other run of non-alphanumerics collapsed to one hyphen. So `stumble across`
becomes `stumble-across.mp3`.

Modules look for a clip in GB first, then in the older `geii` collection, then fall
back to the browser's own voice. Nothing needs registering: drop an mp3 into the
folder and it plays on the next load. Each module's `AUDIO_TODO.txt` lists what is
still unrecorded, and is generated from that module's own buttons.
