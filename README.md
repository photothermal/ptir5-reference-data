# PTIR5 Reference Data

Reference datasets for the [PTIR5 file format](https://photothermal.com), the HDF5-based native format used by [PTIR Studio](https://photothermal.com) 5.0 and higher from Photothermal Spectroscopy Corp.

This repository is intended for software developers building PTIR5 readers/writers, validating parsers, or learning the format by example.

## Repository Structure

```
minimal/       Small, single-measurement files ideal for parser validation
real-world/    Larger, multi-measurement files from actual acquisitions
```

## Minimal Examples

Small files demonstrating one data type each with minimal complexity.

| File | Data Type | Description |
|---|---|---|
| `optir-spectrum.ptir` | O-PTIR Spectrum | Single spectrum, 1019 points |
| `optir-image.ptir` | O-PTIR Image | Single 501x501 image |
| `optir-image-stack.ptir` | O-PTIR Image Stack | 19-frame stack with generated spectra |
| `optir-hyperspectral.ptir` | O-PTIR Hyperspectral | 574-point cube (20x20) with generated spectrum and image |
| `raman-spectrum.ptir` | Raman Spectrum | Single spectrum with background |
| `camera-image.ptir` | Camera Image | BGRA camera image (400x300) with background |
| `flptir-image.ptir` | FL-PTIR Image | Single fluorescence-PTIR image (256x256) |
| `flptir-image-stack.ptir` | FL-PTIR Image Stack | 5-frame FL-PTIR stack (256x256) |

## Real-World Examples

Larger files from actual PTIR Studio acquisitions, showing typical measurement complexity.

| File | Data Type | Size |
|---|---|---|
| `optir-spectra.ptir` | O-PTIR Spectra | 177 KB |
| `optir-image.ptir` | O-PTIR Image | 243 KB |
| `optir-image-stack.ptir` | O-PTIR Image Stack | 57 MB |
| `optir-raman-hyperspectral.ptir` | O-PTIR + Raman Hyperspectral | 32 MB |
| `raman-spectra.ptir` | Raman Spectra | 202 KB |
| `camera-image.ptir` | Camera Image | 178 KB |
| `fl-camera-images.ptir` | Fluorescence Camera Images | 2.0 MB |
| `flptir-image.ptir` | FL-PTIR Image | 843 KB |
| `flptir-image-stack.ptir` | FL-PTIR Image Stack | 17 MB |
| `ptsrs-image.ptir` | PT-SRS Image | 3.5 MB |
| `ptsrs-image-stack.ptir` | PT-SRS Image Stack | 11 MB |

## PTIR5 Format

PTIR5 files use the `.ptir` extension and are HDF5 files with a root `DocType` attribute set to `"PTIR5"`. The format supports spectra, images, hyperspectral cubes, image stacks, and camera images across O-PTIR, Raman, FL-PTIR, and PT-SRS measurement techniques.

PTIR5 replaces the earlier PTIR4 format (PTIR Studio 4.x). Files from both formats use the `.ptir` extension; check the `DocType` attribute to distinguish them.

## License

[CC0 1.0 Universal](LICENSE) - these datasets are released into the public domain.
