# Appendix

## 1. References

### Perception Q1
- OpenCV documentation for grayscale conversion and thresholding.
- UMIC SeDriCa Recruitment Assignment 2026–27.
- Provided SeDriCa perception starter data.

### Perception Q2
- UMIC SeDriCa Recruitment Assignment 2026–27.
- Provided crossing evidence and reference files.

### Motion Planning Q1
- UMIC SeDriCa Recruitment Assignment 2026–27.
- General references on A* search and Hybrid A* used to understand the difference between grid-based and vehicle-aware planning.

---

## 2. Decision Log

### Perception Q1
I started with a simple brightness-based lane detector because the lane markings in the supplied teaching scenes were visually distinguishable from the road.

The baseline deliberately used only local image evidence. After observing that a bright internal seam could be mistaken for a road boundary, I added expected lane width and temporal consistency rather than switching immediately to a more complex model.

### Perception Q2
I used the supplied vision scores for the baseline instead of building a separate detector because the main purpose of the question was reasoning under conflicting evidence.

The revised rule checks V2X freshness and uses a short STOP latch to reduce decision flicker.

### Motion Planning Q1
I implemented normal 8-connected grid A* first because the question asks to show why a collision-free point-robot path can still be unsuitable for the buggy.

I used the buggy's steering limit and wheelbase to calculate the minimum turning radius and then compared this with abrupt grid direction changes.

---

## 3. Failure Log

### Perception Q1
The baseline failed when one road boundary disappeared and a bright internal seam remained visible. The seam could be incorrectly selected as the missing road boundary.

The revised width-based method fixes this on the supplied examples, but the temporal fallback could become stale if both boundaries remain invisible while the road geometry changes.

### Perception Q2
The baseline sometimes produced unnecessary or missed STOP decisions because each frame was treated independently.

The revised rule reduces these errors, but it still uses a global person score rather than explicitly determining whether the pedestrian is inside the vehicle's future path.

### Motion Planning Q1
The grid A* planner produces collision-free paths but does not enforce the buggy's steering or turning constraints.

I did not implement full Hybrid A*. With more time, I would implement it on the same environment and compare path length, curvature and computation time.

---

## 4. AI Usage Note

AI tools were used to help:
- understand the assignment structure,
- discuss possible baseline methods,
- debug Python and Jupyter setup,
- structure notebook explanations,
- review implementation logic,
- and improve clarity of written explanations.

All code was run on the supplied data and the generated outputs were checked during development.

The AI conversations used during the assignment have been retained as requested.