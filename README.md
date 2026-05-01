# PL18 — a life

> A wordless film and notebook about a Burmese palm-leaf manuscript that has been at the University of Glasgow since 1873, and what it means to use AI to interpret an object whose script no one here can read.

**Live site:** https://evoqiherqc.github.io/pl18-a-life/
**Project notebook:** [notebook.ipynb](./notebook.ipynb)
**Film:** [watch on the live site](https://evoqiherqc.github.io/pl18-a-life/)

---

## What this is

This repository is the project portfolio for the final assessment of *AI for the Arts and Humanities (B)* at the University of Glasgow, 2025–26.

The object is **PL18**, a 19th-century Burmese palm-leaf pothi manuscript held in Glasgow University Library, Special Collections. The catalogue identifies it as the *Dhammapada*, gifted by a Burmese Buddhist monk to a school in Edinburgh in the 1830s and acquired by Glasgow University Library in 1873 (Weston handlist, acc. no. 202). To my knowledge no one currently at the University reads Pali in Burmese script; the catalogue's identification has not been independently verified within living memory.

The project consists of three things:

- **A four-minute wordless animated film** told from the manuscript's point of view, made with AI image and video tools (Google Flow, Veo 3.1, Nano Banana 2)
- **A Jupyter notebook** documenting the methodology, including the audit trail of what the AI generated, what was corrected, and what was kept visible as evidence rather than fixed
- **A 3D photogrammetric model** of the actual manuscript, embedded for interactive viewing

The accompanying evaluation report is submitted separately on Moodle.

## How to view the project

The intended way is via the **live site at https://evoqiherqc.github.io/pl18-a-life/** — watch the film, then explore the dry catalogue layer below it, then open the notebook.

If you want to run the notebook locally:

```bash
git clone https://github.com/evoqiherqc/pl18-a-life
cd pl18-a-life
pip install -r requirements.txt
jupyter notebook notebook.ipynb
```

## Tools used

| Layer | Tool |
|---|---|
| Still keyframe generation | Google Flow / Nano Banana |
| Image-to-video animation | Google Flow / Veo 3.1 Fast |
| Synchronised audio | Veo 3.1 native audio generation |
| Audio (ambient and any sourced material) | Per-clip status documented in [notebook §6.7](./notebook.ipynb) |
| 3D model | Scaniverse (iPhone) photogrammetry, January 2026 conservation visit |
| 3D viewer | `<model-viewer>` web component (Google) |
| Site | GitHub Pages, HTML/CSS, built with substantial AI assistance for both code and visual styling |
| Notebook | Jupyter |

**Where to obtain the tools:**

- Google Flow (Nano Banana, Veo 3.1 Fast): https://labs.google.com/flow
- Scaniverse (iPhone): https://scaniverse.com
- `<model-viewer>` web component: https://modelviewer.dev
- Jupyter: https://jupyter.org
- GitHub Pages: https://pages.github.com


## Datasets

This project does not consume external datasets. The data layer comprises:

- 28 conservation photographs of PL18 taken by the author on iPhone, January 2026, included in `stills/conservation/`
- the 3D photogrammetric model in `model/pl18.glb`, derived from those photographs via Scaniverse
- AI-generated stills and video produced for the film, hosted as a public YouTube playlist linked from the site

No third-party dataset is downloaded or required to run the notebook.


## Repository structure

pl18-a-life/
├── README.md              # this file
├── index.html             # the GitHub Pages landing site
├── styles.css             # site styling
├── notebook.ipynb         # the methodology notebook
├── requirements.txt       # Python dependencies for the notebook
├── LICENSE
├── model/
│   └── pl18.glb           # the 3D photogrammetric model
└── stills/
    └── conservation/      # 28 conservation photographs from January 2026

The film itself is hosted as a public YouTube playlist and embedded in the site; see index.html.


## Frameworks engaged

The methodology and evaluation engage the Lovelace–Boden–Ridler test as introduced in the course, and the London Charter (2009) for the Computer-Based Visualisation of Cultural Heritage. Full discussion is in the evaluation report and in [notebook §6](./notebook.ipynb).

## Acknowledgements

Robert Maclean (Special Collections, University of Glasgow Library), for introducing PL18.
Dr Yunhyong Kim, for the course framework and the Lovelace–Boden–Ridler formulation.
David Weston (2025), *Palm-leaf and pothi format manuscripts preserved in Glasgow University Library: A Handlist*, the source of the catalogue identification used here.

## Licensing

- Conservation photographs and the 3D photogrammetric model are © the author, 2026, released under **CC BY-NC-SA 4.0**. The underlying object (PL18) is held by GUL Special Collections; access and photography were granted for the conservation visit in January 2026.
- AI-generated stills, video, and audio in this project are released under **CC BY-NC-SA 4.0**.
- Code in this repository is released under **MIT**.

## Contact

For project enquiries, contact via the GitHub repository.
