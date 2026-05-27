# Optical / Interferometric Detection of Local Reticle Displacement

## 1. Objective and Scope

Main research question:

> If a reticle has local in-plane or out-of-plane displacement, can an optical or interferometric method reliably detect it?

The displacement is assumed to be caused by reticle heating.

## 2. Candidate Detection Routes

### 2.1 Priority Route: TIS-Based Detection Using Overlay Marks

Key points to track:

- whether overlay-marks can generate a usable TIS signal;
- sensitivity to in-plane displacement; **aim for "<0.1 nm"**
- influence of nearby circuit patterns;
- possiblity of **non-periodic** OVL-marks / gratings

### 2.2 Route 2: Grating-base Interferometry

Key points to study:

- diffraction efficiency of EUV reticle gratings under visible or IR illumination;
- whether the diffracted signal is strong enough for interferometric displacement detection;
- dependence on wavelength, polarization, incidence angle, pitch, duty cycle, absorber, and multilayer stack.

### 2.3 Other Candidate Routes

Other routes may include:
- Digital image correlation;
- interferometric or holographic detection of out-of-plane displacement;
- projected or aerial-image displacement measurement.

## 3. First Feasibility Plan

The first feasibility check should use known, imposed, or simulated displacement, so that the detection result can be evaluated clearly.

Suggested comparison cases:

- clean grating;
- isolated overlay mark;
- overlay mark with nearby circuit-like patterns;
- optional coded or non-periodic mark.

Evaluation criteria:

- minimum detectable displacement;
- sensitivity and linearity;
- repeatability;
- bias;
- false-positive behavior;
- robustness to focus, tilt, illumination drift, and neighboring patterns.

## 4. Current Decisions and Open Questions

### Current Decisions

| Item | Current Status |
|---|---|
| Main target | Detect local reticle displacement |
| Displacement origin | Heating-induced displacement |
| First-stage validation | Known / imposed / simulated displacement |
| Priority route | TIS-based detection using overlay marks |
| Baseline | Clean grating |
| Full reconstruction | Not the first-stage target |

### Open Questions

| Question | Owner | Status / Next Step |
|---|---|---|
| Final overlay mark geometry? |  |  |
| Expected displacement range? |  |  |
| Simulation-only or simulation plus experiment? |  |  |
| Available wavelength / NA / illumination condition? |  |  |
| Diffraction efficiency of EUV reticle gratings under visible / IR illumination? |  |  |
| How should nearby circuit patterns be modeled? |  |  |

## Appendix A. Meeting Notes

Meeting notes should be kept here, not in the main body.

### Meeting: 2026-05-26 - EUV Reticle Structure and Priority Routes

**Discussed**

- EUV reticle layout and structure.
- Possible measurement routes for detecting reticle displacement.
- TIS-based detection using overlay marks as the first priority route.
- OVL mark geometry: wafer-plane pitch 0.5-1 um, size 8-16 um; 4x reticle-to-wafer reduction; reticle-plane pitch 2-4 um, size 32-64 um.

**Decisions**

- Three priority routes should be explored.
- Priority Route 1 is the TIS solution based on overlay marks.

**To do**

- Identify the feasibility of OVL marks as the object for TIS.
- Calculate reflection efficiency of OVL marks in visible light.

Each meeting note could use the following format:

```markdown
### Meeting: YYYY-MM-DD - Short Topic

**Discussed**

- 

**Decisions**

- 

**To do**

- 
```

## Appendix B. Change Log

| Date | Change | Reason / Source |
|---|---|---|
| 2026-05-27 | Initial internal sharing document created | Document cleanup |
