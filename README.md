# MuseScore Studio web builds

Web (wasm) build of [musescore/MuseScore](https://github.com/musescore/MuseScore), served with GitHub Pages:
https://musescore.github.io/mss_web_builds/

| Path | What | Updated by |
|---|---|---|
| `index.html` | overview: the latest build and the list of publishes | hand |
| `history.csv` | `date,commit,branch,version` of every publish | CI, appends a row |
| `app/` | the latest build, the app is `app/viewer.html` | CI, replaced |
| `app/build.json` | version, commit, branch and date of the latest build | CI, replaced |

The build is published by the `Build: Wasm` workflow in musescore/MuseScore
(manually with `publish_web_build` enabled).

A build weighs about a hundred megabytes, so the history of this repository is not kept:
every publish is a single commit that replaces the `main` branch (force push).
