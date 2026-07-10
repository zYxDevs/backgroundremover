# Contributing to backgroundremover

Thanks for your interest in contributing!

## Getting started

1. Fork the repository and create a feature branch.
2. Set up a development environment:

```bash
python -m venv venv
source venv/bin/activate
pip install -e .
```

3. Make your changes and test them against real images and videos:

```bash
# Image
backgroundremover -i input.jpg -o output.png

# Video (use -fl to limit frames for quick testing)
backgroundremover -i input.mp4 -mk -fl 30 -o matte.mp4
```

4. Open a pull request with a clear description of the problem and the fix.

## Guidelines

- Keep changes focused — one fix or feature per pull request.
- Match the existing code style of the file you are editing.
- The CLI (`backgroundremover/cmd/cli.py`), the core library
  (`backgroundremover/bg.py`), and the video pipeline
  (`backgroundremover/utilities.py`) are the main entry points.
- Image-processing flags (`-a`, `-mt`, `-om`, etc.) should behave the same
  in single-file, pipe, and `-if` folder modes.
- If your change affects output quality or resolution, include before/after
  details in the PR description.

## Reporting issues

Please include the exact command you ran, the version
(`pip show backgroundremover`), your OS, and whether you are on CPU or GPU.
Sample input files that reproduce the problem help a lot.
