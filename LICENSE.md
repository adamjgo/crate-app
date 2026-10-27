# Licensing of Crate

**Crate is free for non-commercial use. You may not sell it, bundle it into a paid product, or use it to provide a paid service.**

This page explains why, and what Crate is built from. It is the author's own reading of the licences involved, written in good faith. It is not legal advice and it isn't a replacement for the licences themselves.

## Why Crate is non-commercial

Crate's analysis relies on [Essentia](https://essentia.upf.edu), its pretrained models and a few other components. Two of them set the terms for everything else:

1. **The analysis models are licensed for non-commercial use.** The models Crate downloads from the Music Technology Group (Universitat Pompeu Fabra) are published under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). The NonCommercial term applies to using them. Commercial use needs a separate licence from the authors.
2. **Essentia itself is AGPL-3.0.** It is free software under the [GNU Affero General Public License v3](https://www.gnu.org/licenses/agpl-3.0.html), with a commercial licence available from UPF. Distributing an app that includes it brings AGPL obligations, discussed under "Source code" below.

Because commercial use would need licences from others, Crate is free and non-commercial. It is not for sale and has no paid tier.

## What you can do

- Use Crate for your own DJing, practice, events and hobby, including playing gigs. Using the app is not selling it.
- Share the app with friends, free of charge, with this licence file.
- Study how it works.

## What you can't do

- Charge for Crate, or include it in something you charge for.
- Offer Crate's analysis as a paid or ad-supported service.
- Remove this notice or the credits below.

If you want to use Crate commercially, the components above would need commercial licences. Contact their authors, not the Crate author.

## What's in it

Licences below are as the author understands them at the time of writing. Check the linked sources for current terms.

| Component | What Crate uses it for | Licence |
| --- | --- | --- |
| [Essentia](https://essentia.upf.edu) and its TensorFlow build | Tempo, key and audio analysis | AGPL-3.0 (commercial licence available from UPF) |
| Essentia pretrained models (Discogs-EffNet, MusiCNN and the genre, mood, voice, instrument and emotion classifiers) | Genre, mood, vocals, instruments, energy | CC BY-NC-SA 4.0. Downloaded on first run from essentia.upf.edu and not redistributed in Crate's download. Some were trained on datasets with their own terms (Discogs, Jamendo, Million Song Dataset, DEAM). |
| [TensorFlow](https://www.tensorflow.org) (inside Essentia's build) | Runs the models | Apache-2.0 |
| FFmpeg libraries (inside Essentia's build) | Decoding audio | LGPL-2.1 or later |
| [mutagen](https://mutagen.readthedocs.io) | Reading file tags | GPL-2.0-or-later |
| [pywebview](https://pywebview.flowrl.com) | The app window | BSD-3-Clause |
| [FastAPI](https://fastapi.tiangolo.com), [Starlette](https://www.starlette.io), [Pydantic](https://docs.pydantic.dev) | Internal API | MIT |
| [Uvicorn](https://www.uvicorn.org) | Local server | BSD-3-Clause |
| [NumPy](https://numpy.org) | Number crunching | BSD-3-Clause |
| [keyring](https://github.com/jaraco/keyring) | Storing your API key in the Keychain | MIT |
| [Anthropic Python SDK](https://github.com/anthropics/anthropic-sdk-python) | Optional: Discover and chat building | MIT |
| [React](https://react.dev) | Interface | MIT |
| [Python](https://www.python.org/psf-landing/) and [PyInstaller](https://pyinstaller.org) | Running and packaging the app | PSF licence; GPL-2.0 with a bootloader exception that permits distributing the packaged app |

## Services Crate talks to

- **Anthropic API** (optional): Discover and chat building send your written brief (and, for Discover, web search queries) using your own API key, under Anthropic's terms. Your audio is never sent.
- **MusicBrainz** (optional lookup of missing years): sends artist and title. MusicBrainz data is CC0. Requests are rate-limited to what their terms allow.
- **iTunes Search API** (Discover previews, prices and buy links; optional lookup of genre and year): sends artist and title. Previews and links are used as Apple's terms allow, and only link out to Apple Music or iTunes.
- **Essentia model server** (first run): downloads the model files. Nothing about your library is sent.

## Source code

Because the app includes AGPL and GPL components, anyone who receives Crate is entitled to the corresponding source code. The corresponding source for each release is attached to that release alongside the download, as a source archive, under **AGPL-3.0-or-later** and with the licences of the components above intact. The AGPL's terms on modification and redistribution apply to that code, and the non-commercial terms on the models still apply to their use.

## Trademarks and affiliation

Crate is an independent project. It is not made, endorsed or sponsored by Apple, Native Instruments, Algoriddim, Anthropic or the Music Technology Group. Apple Music, iTunes, Traktor, djay, Mixed In Key and Open Key are trademarks or names belonging to their owners, used here only to describe compatibility.

## No warranty

Crate is provided as is, without warranty of any kind. It writes to your Apple Music library, so it backs up the library first and lets you undo changes, but you use it at your own risk.
