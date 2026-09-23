# GB

English teaching material for the Bioengineering (SAB) classes at IUT — interactive HTML activities, pronunciation practice, and games.

Files here are self-contained: one HTML file, CSS and JavaScript inline, no external dependencies. That is deliberate. It means any file can be embedded in Moodle or opened straight from disk, and nothing breaks when a CDN changes its mind.

## What's in here

| File | What it is |
|---|---|
| `index.html` | The front door. Timelines, pronunciation, activities. |
| `pronunciation/index.html` | The pronunciation index, split by year and ordered by the date each sound is taught. |
| `activities/brewing-scene/` | Beer Brewing Process — an interactive scene. Click an area of the brewery to get the term, its pronunciation, and where it sits in the process. Ships with `brewery.png`. |
| `activities/biotechnology/` | Introduction to Biotechnology — seven tabs covering traditional and modern biotechnology, the ten colours, food applications, vocabulary and a mini quiz. Built by merging two earlier standalone files. Serves SAB2 S3. |
| `activities/food-idioms/` | The food idioms session in three pieces for Moodle: `discussion.html`, `meanings.html`, `matching.html`, `whiteboard-race.html`, the picture presenter for Sarah's marker race (pictures embedded, 1.2 MB), and `night-shift.html`, the two-crew ticket board on the food phrasal verbs and idioms (same engine as GEII's Night Shift; Moodle fragment in Educ games). SAB2 S3 session 3. |
| `pronunciation/schwa/` | The schwa module, with a Food science bank and a Brewing bank on a switch. Serves SAB2 S3 session 2. |
| `pronunciation/transparent-words/` | Words French and English share on the page and not in the mouth. Coffee menu at the centre. SAB2 S3 session 1. |
| `pronunciation/ed/` | The -ed ending: /t/, /d/ and /ɪd/, and the one mistake that is adding a syllable. Brewing verbs throughout. SAB3 S5 session 2. |
| `pronunciation/h/` | The /h/ sound: saying it, not saying it, and not inventing one. Beer words throughout. SAB3 S5 session 1. |
| `pronunciation/ch-sh/` | CH /tʃ/ against SH /ʃ/, and the three things the letters ch can mean. Kitchen words throughout. SAB2 S3 session 3. |
| `pronunciation/silent-r/` | The written r that is not pronounced, and the linking r that comes back. SAB3 S5 session 3. |
| `pronunciation/th/` | The two TH sounds, quiet and buzzing, and the five French substitutes for them. GMO debate words throughout. SAB2 S3 session 6. |
| `pronunciation/l/` | Clear L, dark L, and the L that is silent. Beer-describing words throughout; *pale ale* is the anchor. SAB3 S5 session 5. |
| `pronunciation/w/` | The sound W: lips, not teeth; the w that is silent; the w hidden in qu. Bioremediation words throughout (waste, willow, groundwater, aquifer, sewage). SAB2 S3 session 7. |
| `pronunciation/short-long-i/` | The short /ɪ/ and the long /iː/, and the spelling rule that predicts which. Food and lab words throughout; *sieve* and *biscuit* are the exceptions that bite. SAB2 S3 session 5. |

## Where it's used

**SAB Year 3, Semester 5** runs the brewing thread — history of beer, how beer is made, the brewing process, describing a beer, and a crowd-funding pitch at the end. `activities/brewing-scene/` belongs to the brewing process session.

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
