# Computer Vision — Problem Set 1: Images as Functions

Solution for Problem Set 1 of Georgia Tech CS6476 (Computer Vision). The
assignment covers representing images as functions: color-plane
manipulation, pixel-region replacement, arithmetic/geometric operations,
noise, and hybrid images built from low/high frequency blending.

## Key files

| File | Description |
|---|---|
| [`ps1.py`](ps1.py) | Core implementation — all graded functions (see below) |
| [`experiment.py`](experiment.py) | Driver script that runs `ps1.py` against the input images and generates the output files used in the report |
| [`PS1_Report/ps1_report.pdf`](PS1_Report/ps1_report.pdf) | **Final writeup/report** with results, output images, and discussion answers |
| [`CS6476-PS1.pdf`](CS6476-PS1.pdf) | Original assignment instructions |
| `cat.bmp`, `dog.bmp` | Input images used for the hybrid-image section |
| `southafrica*.png` | Input images used for the color-channel discussion questions |
| `ps1-*.png` | Generated output images referenced in the report |

### Functions implemented in `ps1.py`

- `extract_red` / `extract_green` / `extract_blue` — isolate a single color channel
- `swap_green_blue` — swap the green and blue channels
- `copy_paste_middle` / `copy_paste_middle_circle` — paste a square/circular region from one image into the center of another
- `image_stats` — min, max, mean, and standard deviation of pixel values
- `center_and_normalize` — center and rescale pixel values
- `shift_image_left` / `difference_image` — shift an image and compute a difference image
- `add_noise` — add Gaussian noise to a given channel
- `build_hybrid_image` / `vis_hybrid_image` — construct and visualize a hybrid image from low/high frequency components

## Report

See [`PS1_Report/ps1_report.pdf`](PS1_Report/ps1_report.pdf) for the full
writeup, including output images and the discussion answers. The
`PS1_Report/` directory also contains the LaTeX source (`report.tex`,
`sections/`, `yourAnswers/`) used to build it.

## Running it

```bash
pip install numpy scipy opencv-python
python experiment.py
```
