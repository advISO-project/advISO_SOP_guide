# advISO SOP Writing Guide

This repository contains the source files for the [advISO SOP Writing Guide](https://adviso-sop-guide.readthedocs.io/en/latest/index.html), which presents a modular approach to writing Standard Operating Procedures (SOPs) for organisations working toward accreditation under the ISO 15189 (medical laboratories) and ISO 17025 (testing and calibration laboratories) standards.

The documentation uses the [advISO guide template](https://github.com/advISO-project/advISO_guide_tempate/tree/dev).

## Building locally

Install the documentation dependencies and build from the `docs` directory:

```console
python -m pip install -r docs/requirements.txt
make -C docs html
```

The generated site is available in `docs/_build/html/`. The guide settings,
including its title, subtitle, and sidebar colour, are in `docs/conf.py`.
All documentation pages use MyST Markdown.
