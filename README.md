# Kerr QNM validity boundary

Code, processed figure data, result receipts, and manuscript source for *Predicting the Validity Boundary of Finite Quasinormal Mode Spectroscopy*.

The repository estimates a source-dependent validity boundary for finite quasinormal-mode spectroscopy. Its principal calibrated result concerns the dominant h22 mode of nonprecessing aligned-spin binaries. It does not make a mode-general claim or a strong real-event no-hair claim. Negative results and superseded diagnostics remain in the claim registry.

## Reproduce the public package

With Python 3.10 or newer:

```text
python tools/validate_repository.py
python -m unittest discover tests -v
python manuscript/plot_prl_figures.py
```

The plotting script reads only `manuscript/figure_data`. Raw waveform, detector-strain, and posterior arrays are not redistributed. Their official identifiers and checksums are recorded in `manifests/external_data.json`.

The manuscript can be compiled with a REVTeX-capable TeX installation by running `latexmk -pdf` on `main.tex`, `Supplemental_Material.tex`, and `cover_letter.tex` in `manuscript`.

## Scope

The blind numerical-relativity result is for an N2 basis at ringdown SNR 100. The h33 stress test remains a preserved failure. The GW150914 common-support time-and-sky calculation is retrospective supporting evidence and does not restore prospective ordering.

Software is released under the BSD 3-Clause License. Citation metadata are provided in `CITATION.cff`.
