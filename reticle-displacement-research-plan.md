# Research Plan Draft: Optical / Interferometric Detection of Reticle Displacement and deformation

## 1. Working Purpose of This Document

This document organizes the research framing, assumptions, candidate measurement routes, and first validation steps for a possible study on optical / interferometric detection of local displacement in EUV reticles or reticle-like samples.

It should serve as a living planning document rather than a record of every discussion detail. Meeting-specific conclusions and parameters should be collected separately so the main research plan remains readable.

The current first-stage focus is **detection**. Reconstruction of a full displacement field, physical explanation of the deformation source, scanner correction, and wafer overlay prediction are later-stage goals, not the first target.

## 2. Current Understanding

The problem should not initially be framed as:

> How can we measure real EUV reticle thermal deformation inside a scanner?

That is too constrained and depends on unavailable scanner-internal details.

The better first-stage question is:

> Given a reticle-like object with local in-plane and/or out-of-plane displacement, can we design an optical, diffraction-based, interferometric, image-based, or projected-image method that detects the displacement reliably?

Possible measurement routes include:

- **TIS-based detection using overlay (OVL) marks**,
- **grating interferometry,**
- marks or patterns,
- heterodyne interferometry,
- speckle or digital holography,
- image registration,
- projected image or aerial-image displacement.

Scanner use is optional. True EUV heating is not required in the first stage. The displacement may be imposed, simulated, preset, or otherwise treated as a known perturbation for method validation.

## 3. Main Goal

Develop and compare feasible optical / interferometric concepts for answering the first-stage question:

> If a reticle or reticle-like object has local **in-plane** or out-of-plane displacement, can an optical or interferometric method reliably detect it?

The first-stage goal is:

```text
detection of local displacement
```

not:

```text
full-field reconstruction
complete thermal-physical explanation
scanner integration
wafer overlay correction
```

The initial detection target may include:

- local in-plane displacement,
- local out-of-plane displacement,
- apparent projected-image displacement,
- differential displacement between two states,
- displacement at selected marks or gratings,
- **TIS signal changes from overlay marks projected from the reticle to the wafer plane.**

## 4. Meeting Minutes / Discussion Notes

### Meeting: 2026-05-27 - EUV Reticle Structure and Priority Routes

**Discussed**

- EUV Reticle layout and structure.
- Possible measurement routes for detecting reticle displacement.
- TIS-based detection using **overlay marks** as the first priority route.
- OVL mark geometry: @wafer-plane: pitch **0.5-1 um**, size **8-16 um**; reticle-to-wafer reduction **4x**; so, @reticle-plane: pitch **2-4 um**, size **32-64 um**.

**Decided**

- Three priority routes should be explored.
- Priority Route 1 is the **TIS solution based on overlay marks**.

**To do**

- Identify the feasibility of OVL-mark as the object for TIS
- calculate reflection efficiency of OVL-mark in visible light

## 5. Central Research Questions

### Q1. What displacement should be detected?

Candidate displacement types:

- local in-plane displacement of marks, gratings, or absorber-like patterns,
- local out-of-plane displacement / height change / tilt,
- apparent image displacement caused by out-of-plane motion or optical effects,
- projected image displacement,
- differential displacement between two known states.

**Current answer:**  
The first-stage target should be **detecting whether local displacement exists**, rather than fully reconstructing the displacement field. Both in-plane and out-of-plane displacement should remain in scope, but they must be treated as different observables.

### Q2. Is the first validation based on known displacement or unknown physical deformation?

Possible validation cases:

- known displacement imposed by a calibrated translation stage,
- known grating shift or designed pattern offset,
- simulated displacement field,
- controlled mechanical deformation,
- controlled thermal deformation,
- unknown real deformation.

**Current answer:**  
Start with **known or imposed displacement**. This is cleaner than starting with unknown thermal deformation because it allows the measurement principle, noise floor, sensitivity, and false-positive behavior to be tested directly.

### Q3. Is the target detection, reconstruction, or explanation?

Possible levels:

- detection: determine whether a displacement occurred,
- localization: determine where displacement occurred,
- quantification: estimate displacement magnitude,
- reconstruction: recover a displacement vector field,
- explanation: infer thermal, mechanical, or optical cause.

**Current answer:**  
The first target is **detection**. Quantification is useful if achievable, but full reconstruction and physical explanation should be treated as later goals.

### Q4. Should the method detect sparse local displacement or full-field displacement?

Possible spatial levels:

- one mark / one grating,
- multiple sparse marks,
- semi-dense distributed grating cells,
- selected product-like ROIs,
- full-field dense map.

**Current answer:**  
Start with sparse or semi-dense detection. Full-field dense recovery is attractive but premature. A first useful target is detecting displacement at selected marks, gratings, or ROIs.

### Q5. Should scanner use be included?

Possible options:

- no scanner,
- scanner-like optical projection path,
- projected image measurement,
- actual scanner measurement,
- later comparison to scanner / overlay data.

**Current answer:**  
Scanner use is **not mandatory**. It should remain optional. A scanner or scanner-like path may become relevant if the method detects displacement through projected image motion, but the first proof of concept should not depend on proprietary scanner internals.

### Q6. Is true EUV heating required?

**Current answer:**  
No. True EUV heating is not required for first-stage method development. The displacement can be preset and treated as known in simulation or imposed experimentally. Thermal realism becomes important only after the measurement concept is validated.

### Q7. What structures can be used as displacement probes?

Possible structures:

- **dedicated gratings**,
- **overlay (OVL) marks for TIS-based detection**,
- **existing reticle alignment marks,**
- product-like patterns,
- non-periodic or pseudo-random marks,
- random or pseudo-random patterns,
- edge marks,
- multilayer / absorber features,
- projected image features.

**Current answer:**  
The current priority is to study whether **overlay marks can work as the object for a TIS-based method**. Dedicated gratings remain a useful baseline because conventional TIS signals are usually based on clean grating objects, but the main feasibility question is whether realistic OVL marks can produce a usable TIS signal and what accuracy can be achieved.

### Q8. What reference frame should be used?

Possible reference frames:

- cold state versus displaced state,
- reference grating versus measurement grating,
- local differential pair,
- external metrology frame,
- best-fit rigid-body removal over multiple marks,
- projected image reference.

**Current answer:**  
Use differential measurement whenever possible. For multi-point measurements, remove global translation and rotation so that local displacement is not confused with rigid-body motion.

### Q9. How should in-plane and out-of-plane displacement be separated?

Possible strategies:

- choose a measurement geometry mainly sensitive to in-plane displacement,
- choose a separate geometry mainly sensitive to out-of-plane displacement,
- use multi-angle or multi-focus measurement,
- use an auxiliary height / tilt sensor,
- compare image-based and interferometric observables,
- accept projected image displacement as a mixed effective observable.

**Current answer:**  
Both in-plane and out-of-plane displacement are important, but they should not be collapsed into one quantity. The first study should explicitly state which observable each method detects and whether out-of-plane motion can create a false in-plane signal.

### Q10. What precision and confidence level are needed for detection?

Possible metrics:

- minimum detectable displacement,
- false-positive rate,
- repeatability,
- drift over time,
- sensitivity to focus / tilt / illumination,
- ability to distinguish local displacement from global motion.

**Current answer:**  
A useful initial target is detecting displacement on the order of **1 nm to a few nm** at selected marks or gratings. The exact requirement should be refined after estimating realistic displacement magnitudes and experimental noise.

### Q11. How should a candidate method be judged?

Suggested criteria:

- detectable displacement type: in-plane, out-of-plane, projected, or mixed,
- minimum detectable displacement,
- calibration difficulty,
- need for dedicated marks,
- robustness to drift,
- robustness to focus and tilt,
- compatibility with reticle-like samples,
- scalability from one point to multiple points,
- potential path toward scanner or projected-image relevance.

**Current answer:**  
Candidate methods should first be judged by whether they can reliably detect a known displacement under controlled conditions. Only after that should they be judged by scanner relevance or EUV thermal realism.

## 6. Priority Routes

The following routes are not final solutions. They are priority directions to compare and refine as the reticle layout, available marks, and measurement constraints become clearer.

Meeting note:

- The reticle layout and structure were discussed.
- Three priority routes should be explored.
- The first documented priority route is the **TIS solution based on overlay marks**.

### Priority Route 1: TIS-Based Detection Using Overlay Marks

#### Status

Highest current priority after discussion with ASML.

#### Basic idea

TIS signal changes caused by displacement of projected OVL mark patterns. The observable may be an effective projected-image displacement rather than a pure physical reticle displacement.

#### Known mark parameters

On the wafer plane:

- OVL mark pitch: **0.5-1 um**,
- OVL mark size: **8-16 um**.

With **4x reduction** from reticle plane to wafer plane, the corresponding reticle-plane dimensions are:

- reticle-side OVL mark pitch: **2-4 um**,
- reticle-side OVL mark size: **32-64 um**.

#### Why this route matters

TIS commonly uses a grating object, where the surrounding region is usually empty or clean enough that stray signal interference is limited. Using OVL marks would be more directly relevant to realistic reticle / scanner use, but it creates additional feasibility questions because OVL marks are not necessarily ideal periodic gratings and may be surrounded by circuit patterns.

#### Main feasibility questions

- Can an OVL mark generate a sufficiently clean and interpretable TIS signal?
- What displacement sensitivity and accuracy can be achieved with OVL mark geometry?
- How does the TIS signal from an OVL mark compare with the signal from a conventional clean grating?
- Does the finite OVL mark size, pitch, duty cycle, or 2D geometry reduce accuracy or introduce bias?
- Can the TIS signal remain usable when circuit patterns near the OVL mark are also projected?
- How strong are stray signals from neighboring circuit patterns relative to the mark signal?
- Can signal processing, spatial filtering, pupil filtering, or mark design suppress the stray contribution?
- Would a non-periodic, pseudo-random, or specially coded mark be more robust than a periodic OVL mark?

#### First validation idea

Start with simulation and/or controlled optical experiments comparing:

- a clean periodic grating baseline,
- an isolated OVL mark,
- an OVL mark with nearby circuit-like patterns,
- a non-periodic or coded mark candidate.

For each case, impose a known displacement and evaluate the TIS signal linearity, sensitivity, bias, repeatability, and robustness against stray pattern interference.

The following routes remain useful comparison directions. They may become priority routes after the first TIS / OVL-mark feasibility check is better defined.

### Candidate Route A: Image Registration of Marks or Product-Like Patterns

#### What it detects

Apparent lateral displacement of local image features.

#### Possible implementation

Take repeated microscope images of marks, gratings, or product-like patterns before and after a known perturbation. Use image correlation, phase correlation, feature fitting, or local registration to detect displacement.

#### Strength

Simple, accessible, and flexible. Good for quickly testing whether displacement can be detected at all.

#### Main risk

Image shift can be biased by focus, out-of-plane displacement, contrast changes, illumination drift, and pattern-dependent optical effects.

#### First validation idea

Use a known stage translation or simulated image shift to test the displacement detection floor before adding thermal or mechanical deformation.

### Candidate Route B: Grating Phase / Diffraction-Based Detection

#### What it detects

Lateral displacement of periodic marks through diffraction phase, fringe shift, or phase difference between diffraction orders.

#### Possible implementation

Illuminate a grating and measure diffraction orders or interference between orders. A lateral displacement produces a phase shift.

#### Strength

Can be highly sensitive to in-plane displacement and may be compact.

#### Main risk

Requires phase reference, has modulo-pitch ambiguity, and may be sensitive to tilt, focus, polarization, and grating asymmetry.

#### First validation idea

Apply a calibrated lateral shift to a grating and test whether the optical signal detects the shift repeatably.

### Candidate Route C: Talbot / Moire / Grating Interferometric Detection

#### What it detects

Relative displacement between gratings or between a grating and an optical reference.

#### Possible implementation

Use Talbot self-imaging, moire phase, heterodyne grating interferometry, or related grating interferometric methods to detect sub-period displacement.

#### Strength

Potentially very high sensitivity. Especially promising if dedicated gratings are allowed.

#### Main risk

Requires stable reference geometry and careful separation of local displacement from global motion, tilt, and height changes.

#### First validation idea

Use two or more gratings on a test sample. Impose known lateral displacement at one location or simulate differential displacement. Check whether the method detects the differential signal after removing global motion.

### Candidate Route D: Interferometric / Holographic Detection of Out-of-Plane Motion

#### What it detects

Out-of-plane displacement, tilt, or surface deformation.

#### Possible implementation

Use interferometry, digital holography, phase-shifting interferometry, or speckle interferometry to detect height or phase changes.

#### Strength

Out-of-plane displacement is optically natural to measure and may be important for reflective EUV masks.

#### Main risk

It may not directly detect in-plane displacement. It can also produce apparent lateral image shift in projected or microscope images.

#### First validation idea

Measure known out-of-plane displacement or tilt and quantify whether it creates false lateral displacement in image registration or diffraction methods.

### Candidate Route E: Projected Image / Aerial Image Displacement

#### What it detects

Effective projected image displacement, which may include in-plane motion, out-of-plane motion, phase effects, and imaging effects.

#### Possible implementation

Use a scanner-like projection path, microscope projection, or aerial-image measurement to detect whether local pattern displacement appears in the projected image.

#### Strength

Closest to lithographic relevance.

#### Main risk

It is a mixed observable, not a pure measurement of physical in-plane or out-of-plane displacement.

#### First validation idea

Apply known in-plane and out-of-plane perturbations separately and test whether the projected image method can distinguish them.

## 7. Recommended First-Stage Plan

### Step 1: Define the detection problem

Choose one or two displacement types:

- known in-plane displacement,
- known out-of-plane displacement,
- or known mixed perturbation.

Define the observable and success metric before choosing hardware.

### Step 2: Start with known displacement

Use simulation, calibrated stage motion, shifted grating patterns, or mechanically imposed displacement. Avoid unknown thermal deformation in the first validation.

### Step 3: Compare at least two detection routes

Recommended comparison:

- **TIS detection using OVL marks as the priority route**,
- image registration,
- grating / diffraction / Talbot phase detection,
- optional out-of-plane interferometry.

This comparison is useful because each method has different false-positive mechanisms. The clean grating case should be treated as a baseline for judging whether OVL marks are workable in a TIS method.

### Step 4: Add complexity only after detection is proven

Later add:

- thermal loading,
- reticle-like substrate,
- pellicle or pellicle surrogate,
- scanner-like projection,
- realistic alignment marks,
- low-order deformation model,
- overlay or actinic relevance.

## 8. Initial Decision Table

| Question | Current working answer | To be revised by user |
|---|---|---|
| First-stage target | Detection | |
| Displacement type | In-plane and out-of-plane both in scope, but treated separately | |
| First validation | Known / imposed / simulated displacement | |
| Scanner required? | No | |
| True EUV heating required? | No | |
| Dedicated gratings allowed? | Yes, mainly as clean TIS / diffraction baseline | |
| Existing marks also considered? | Yes; OVL marks are now the priority structure | |
| Main candidate methods | **priority: TIS using OVL marks**; baseline: clean grating TIS / diffraction; supporting: image registration, out-of-plane interferometry, projected image | |
| First success metric | reliable TIS detection of known OVL mark displacement and quantified accuracy / bias | |
| Reconstruction required? | Not initially | |
| Physical cause explanation required? | Not initially | |
| Known OVL mark geometry | wafer pitch 0.5-1 um, wafer size 8-16 um, 4x reticle-to-wafer reduction | |
| Main new risk | circuit patterns around OVL marks may introduce stray TIS signals | |

## 9. My Current Recommendation

The most sensible first study is not a scanner or thermal deformation study. It is a **controlled TIS feasibility study using OVL marks**.

Recommended starting point:

```text
clean grating TIS baseline
+ isolated OVL mark TIS simulation / experiment
+ OVL mark with nearby circuit-like patterns
+ optional non-periodic or coded mark design
+ known imposed displacement
+ detection accuracy, bias, and stray-signal robustness analysis
```

The first milestone should be:

> Demonstrate whether a TIS method can reliably detect a known displacement of an OVL mark, and quantify the accuracy loss or bias compared with a clean grating baseline.

Only after that milestone should the study move toward:

- unknown thermal deformation,
- scanner-like conditions,
- projected image relevance,
- full-field reconstruction,
- or physical thermal modeling.

## 10. Open Notes for User Edits

- Preferred displacement type:
- Candidate sample:
- Available OVL mark design:
- OVL mark pitch / size:
- Nearby circuit-pattern assumptions:
- Clean grating baseline:
- Non-periodic or coded mark candidate:
- Available optical tools:
- Available interferometers:
- Available camera / microscope:
- Possible stage or actuator for known displacement:
- Possible height / tilt reference:
- Desired detection threshold:
- Whether projected-image displacement is acceptable:
- Ideas to keep:
- Ideas to reject:
