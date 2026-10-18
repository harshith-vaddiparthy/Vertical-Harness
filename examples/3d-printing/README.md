# 3D Printing Harness

**Repository:** [harshith-vaddiparthy/3D-Printing-Harness](https://github.com/harshith-vaddiparthy/3D-Printing-Harness)

An example of specializing Vertical Harness for a concrete workflow: point it at a 3MF/STL file, inspect actual geometry on localhost, rotate/zoom/pan, check its plate placement, make basic scale/rotation/position edits, and export the edited STL.

## Try it

Fork the specialized repository or use its template button, then follow its README. With Python 3.9+ and Node.js/npm:

```bash
git clone https://github.com/harshith-vaddiparthy/3D-Printing-Harness.git
cd 3D-Printing-Harness
npm ci --ignore-scripts
python3 -m app.server --file examples/models/inspection-wedge.stl --open
```

Open **http://127.0.0.1:8765** and choose your own model. No model API key is required. An original wedge model is included for learners.

The specialization retains `task.md`, configuration, domain rules, workflows, prompts, evaluations, operations and record templates, then adds a working viewer/importer/server. Physical printing requires the learner's own configured slicer/printer adapter; the maintainer's private device connection is not included.
