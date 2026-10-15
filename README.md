# Talos claw concepts

Interactive 3D viewer for the OSU Underwater Robotics Team's Talos claw redesign: every claw concept shown on the
robot where it mounts, with jaw and stow animations, pickup attempts for every RoboSub 2024–2026 table object,
check results (reach, torpedo clearance, DVL, stow, mass, structure, grasp), strengths and weaknesses, and a
comparison table.

**Live:** https://zehdari.github.io/ClawEvaluation/

Static site: `index.html` plus `data/` (meshes and results stored as gzip+base64 text, decoded in the browser).
Needs a current browser (Chrome/Edge, Firefox 113+, Safari 16.4+). To run it locally:

    python3 -m http.server 8765    # then open http://localhost:8765/

**CAD downloads:** one zip of STEP files (every part) per concept in [`cad/`](cad/), e.g.
`https://zehdari.github.io/ClawEvaluation/cad/c7_intermesh.zip`; [`cad/index.json`](cad/index.json) lists them. Target
printer: Bambu Lab P1S (256 x 256 x 256 mm); Bambu Studio imports STEP directly.

Generated from the `~/claw_prototypes` workspace (clawlab toolkit + concept models) with `viewer/make_publish.py`
and `viewer/make_local.py`. Results are pre-revision: a revision pass and a consistent re-run on the final toolkit
are pending.
