# string_pulse_nonlocal_jump — contributor review

**Decision: PASS** (contributor self-check; Sara approval remains pending).

**Reviewed head:** `8d848b543fb3f28a70ce29a76177520bbdbcdcbb`

**Generator correctness:** PASS. **Runtime provenance:** PASS, NEW/REPLACEMENT.

**Declared scaling target:** 100,000 accepted cases. **Declared-target scale readiness:** PASS.

**Audited media:** exactly two submitted seeds, 42 and 98; eight formal native streams. Static 100,000-profile validation is not a claim of 100,000 rendered cases. Controlled probes are explicitly smoke-resolution evidence.

**Production readiness:** PRODUCTION READY under the analytical-trajectory, real-3D rendering contract reviewed here; no simulator-native dynamics claim.

## Blocking findings

None remaining in the six-gate generator and delivered-media contract. No fresh rerender-and-compare execution is claimed; standalone reproduction/compare entry points and deterministic trajectory tests were inspected/tested. The inherited upstream README/CITATION license wording differs from the upstream LICENSE; this review grants no additional rights and leaves upstream licensing terms intact.

## Six-gate result

| Check | Result | Evidence |
|---|---|---|
| Output contract | PASS | Eight formal 2048² H264 RGB streams: 24 fps, 120 frames, five seconds; independently ffprobed and fully decoded. |
| Violating-object-only mask | PASS | Only the visible free-span string; anchor posts, jaws and base excluded. Every formal pixel is 0 or 255, equal channels; active window exactly matches metadata. |
| Real scaling | PASS | 100,000 CPU profiles; primary axes separately rendered at 512²; two native 2048² cases across different length/response/onset/appearance/view buckets. |
| Official unpatched environment | PASS | Clean exact source head, official Python 3.11.17 + bpy 4.5.3, real Tesla T4 OpenGL renderer, pinned packages and actual encoder witness. |
| Decoded matched control | PASS | All 120 frames of True/CF/mask/overlay independently decoded; exact prefix equality and red-only active-mask replacement. |
| Semantic consistency | PASS | A single pulse travels right on the intact anchored 3D string. CF makes one visible nonlocal jump across an unvisited interval, then continues at its original speed; no simultaneous duplicate pulse or detached segment. Brightened shared palette improves purple-string contrast. README, title, registered operator, predicates and independent prompts inspected together. |

## Production-quality behavioral baseline

| Check | Result | Evidence |
|---|---|---|
| True completes the correct prompt outcome | PASS | A single pulse travels right on the intact anchored 3D string. CF makes one visible nonlocal jump across an unvisited interval, then continues at its original speed; no simultaneous duplicate pulse or detached segment. Brightened shared palette improves purple-string contrast. |
| Counterfactual has exactly one physical error | PASS | One displacement-and-velocity state translation; independent finite difference verifies one jump, positive skipped gap, ordinary post-jump speed and fixed endpoints. |
| Both independent prompts match their respective videos | PASS | Both seeds reviewed against source, full decoded sequences, and actual browser playback; prompts reproduced below. |
| Matched setup and branch identity | PASS | Exact decoded prefix, shared camera/color/support/latch conditions, correctly labeled paths. |
| No undeclared anomaly or unrelated geometry failure | PASS | Continuous 3D meshes, contacts and native selected frames reviewed; stated thread passage is part of the screw violation. |
| Completion, observation tail and final visibility | PASS | All streams play all 120 frames; visible final outcomes; no target crops, minimum borders in independent report. |
| Phenomenon-specific plausibility | PASS | One displacement-and-velocity state translation; independent finite difference verifies one jump, positive skipped gap, ordinary post-jump speed and fixed endpoints. |

## Timebase and playback integrity

| Check | Result | Evidence |
|---|---|---|
| Source seconds per video second | PASS | Trajectory t[n]=n/24, 24fps video: 1 source second per video second; last sample 119/24, container duration 5s. |
| Outer steps versus solver substeps | NOT APPLICABLE | Analytical sampled states; no undocumented solver substeps or time scaling. |
| Intentional and pair-matched speed | PASS | Shared timebase and camera; full sequences inspected, no slow/fast-motion label shortcut. |
| Timebase remediation | NOT APPLICABLE | No time mapping changed during remediation. |

## Optional simulator-profile result

Not applicable: Blender Workbench renders analytical trajectories and is not presented as their physics solver.

## Semantic matrix

Title, generator README, registered operator, scoring predicate and both rendered branches describe the same phenomenon: One displacement-and-velocity state translation; independent finite difference verifies one jump, positive skipped gap, ordinary post-jump speed and fixed endpoints.

Seed 42:

True: A single transverse pulse moves to the right along an intact elastic string anchored at both ends. The pulse passes continuously through each intervening part of the string and remains visible before reaching the far anchor.

Counterfactual: A single transverse pulse moves to the right along an intact elastic string anchored at both ends. The whole pulse suddenly jumps to a farther section without crossing the intervening span; there is still only one pulse, and it then continues moving right at its original speed.

Operator: `{}`; onset 31; visible change 31; physical evidence 31.

Seed 98:

True: A single transverse pulse moves to the right along an intact elastic string anchored at both ends. The pulse passes continuously through each intervening part of the string and remains visible before reaching the far anchor.

Counterfactual: A single transverse pulse moves to the right along an intact elastic string anchored at both ends. The whole pulse suddenly jumps to a farther section without crossing the intervening span; there is still only one pulse, and it then continues moving right at its original speed.

Operator: `{}`; onset 35; visible change 35; physical evidence 35.

## Verified passes

Independent measurements for both accepted cases:

```json
[
  {
    "case_id": "string_pulse_nonlocal_jump_00000042",
    "first_changed_frame": 31,
    "mask_end_frame": 120,
    "minimum_target_border_px": 267,
    "physical_witnesses": {
      "jump_distance": 2.7739999999999996,
      "skipped_unvisited_gap": 1.0980569664294575,
      "normal_wave_speed": 0.5569999999999999,
      "interventions": 1,
      "evidence_frame": 31
    }
  },
  {
    "case_id": "string_pulse_nonlocal_jump_00000098",
    "first_changed_frame": 35,
    "mask_end_frame": 120,
    "minimum_target_border_px": 283,
    "physical_witnesses": {
      "jump_distance": 2.9629999999999996,
      "skipped_unvisited_gap": 1.2647923930192522,
      "normal_wave_speed": 0.6515,
      "interventions": 1,
      "evidence_frame": 35
    }
  }
]
```

## Successful-render runtime provenance

| Check | Result | Evidence |
|---|---|---|
| Exactly one successful witness per submitted case | PASS | runtime-witness-index.json plus official fail-closed runtime audit; two accepted cases. |
| Commit, source state, command and seeds | PASS | runtime-witness.json binds this exact clean head and seeds42,98. |
| Actual components and delivered hashes | PASS | Python/bpy/packages/OS/GPU/OpenGL/driver and actual encoder binary hash/version retained; SHA-256 inventory audited. |
| Nested runtime | NOT APPLICABLE | bpy executes in the same recorded Python process; no separate Blender embedded interpreter. |
| Reproduction recipe | PASS | Standalone examples/reproduce.py and compare.py; historical successful runtime evidence is separately retained. |

## Client-facing artifact consistency

| Check | Result | Evidence |
|---|---|---|
| Browser playback and seeking | PASS | All eight HTML streams actually played to ended=true, duration/currentTime=5, error=null; native Chrome controls expose seeking, HTTP Range returns 206 in public verification. |
| Black/white masks and red overlays | PASS | Actual browser frames inspected; no green/magenta/channel swaps or blank media. |
| Formal overlay consistency | PASS | Every decoded formal off-mask pixel equals CF; every active pixel is [255,0,0]; no shadows. |
| Review derivatives | PASS | HTML clearly labels 1024² lossy yuv420p copies separately from formal lossless 2048² RGB files. |

## Scale-readiness result

| Check | Result | Evidence |
|---|---|---|
| CGC-v1 deterministic coverage | PASS | 100,000 accepted static signatures/profile IDs, 100M profile space, all axis buckets covered; zero reported errors. |
| Independent primary axes reach rendered output | PASS | Clean exact-head axis-probes.json: length, response, onset low/high rendered independently; recorded PNG hashes and per-image MAD/changed pixels. |
| Formal material diversity | PASS | Seeds42/98 differ across all five relevant buckets; two native decoded clips visibly differ in dimensions, response, onset, palette and view. |
| Pair-shared nuisance variation and exact prompts | PASS | Scene/camera/color shared within each pair; incidental profile IDs are absent from prompts. |
| Sharding/quota and manifests | PASS | Canonical eight-shard disjointness audit; source/output SHA-256 manifests; accepted-case quota checked. |
| Safe resume | PASS | Actual compatible resume fully decoded existing cases; incompatible quota rejected. Original receipt retained; wave visibility remediation reruns this check at its new head. |
| Fail-closed runtime and media audits | PASS | Official runtime witness audit and independent full final-MP4 decoding; no monkey patches. |

## Commands and artifacts checked

`python -m compileall`, `python -m pytest`, official `examples/generate.py`, canonical `examples/audit_scaling.py`, controlled `examples/probe_axes.py`, official run/audit/index provenance scripts, independent_review.py and anonymous full-file HTTP hash/Range verification. Evidence is linked from review.html and included in packet-manifest.json.

## Re-review requirements

Any source-head change requires fresh applicable exact-head evidence and a new versioned public packet. Sara's review is independent of this contributor self-check.
