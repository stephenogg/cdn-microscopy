+++
title = "Coverslip Thickness"
layout = "simple"
+++

## In short

Use **#1.5H coverslips (170 ± 5 µm)** for all high-resolution imaging, and put your cells on the coverslip surface that faces the objective.

## Why it matters

Most high-NA objectives are designed for a 0.17 mm coverslip (refractive index about 1.52), shown as "0.17" on the objective barrel. A different thickness, or an extra layer between sample and lens, causes spherical aberration. This blurs the image, lowers resolution and reduces signal. The effect increases with NA and is most important when you image at the diffraction limit (for example, pixels of about 100 nm).

Some objectives have a correction collar to compensate. Most oil objectives, including those on our systems, do not, so the correct coverslip is essential. (Confirm per objective)

{{< figure default=true src="Objectives.png" title="Objectives are marked with their design coverslip thickness" caption="40x objectives marked 0.17 mm." width=500 >}}

## Coverslip grades

| Number | Thickness (µm) |
|:--:|:--|
| #0 | 85–130 |
| #1 | 130–160 |
| **#1.5 / #1.5H** | **160–190 (1.5H: 165–175)** |
| #2 | 190–230 |
| #3 | 240–350 |
| #4 | 430–650 |

Buy #1.5H (not "#1.5" without the H) when imaging at high NA, and always check the box label.

## Signal loss

Objectives with NA above about 0.4 lose signal and resolution as coverslip error grows (see the graph below). Even a modest error can matter for 63x/1.4 oil lenses.

{{< figure default=true src="IntensityVsThicknessError.png" title="Intensity vs coverslip thickness error" caption="Source: [Nikon MicroscopyU](https://www.microscopyu.com/microscopy-basics/coverslip-correction)" width=500 >}}

## Imaging cells: use coverslips, not slides

The lens expects your sample to sit **directly against the coverslip**. 

- Grow cells on #1.5H coverslips, or in dishes and chambers with a #1.5H glass bottom, and use an inverted microscope.
- Avoid imaging through the thick plastic or glass slide base, or through a deep layer of mounting medium whose refractive index does not match. This degrades resolution.
- High-NA lenses have a short working distance (for a 63x/1.4 oil lens, about 0.14–0.19 mm). If your cells are farther away than this, the lens hits the sample before it focuses.

{{< figure default=true src="goodbad.png" title="Cells on the coverslip (good) vs on the slide (bad)" width=500 >}}

## Checklist

- [ ] #1.5H coverslip
- [ ] Cells on the coverslip surface facing the lens
- [ ] Mounting medium suited to the objective (oil, water or glycerol)
- [ ] Coverslip sealed and cleaned before imaging
