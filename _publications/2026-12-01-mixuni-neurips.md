---
title: "MixUni: Joint multi-property prediction for chemical mixtures with physics-informed heads"
collection: publications
category: conferences
permalink: /publications/2026-12-01-mixuni-neurips/
excerpt: "A unified, geometry-aware multi-task model for liquid-mixture properties in battery-electrolyte design: an E(3)-equivariant encoder, a shared sparse mixture-of-experts head, and a physics-informed stretched-Arrhenius conductivity head."
date: 2026-12-01
venue: "Advances in Neural Information Processing Systems (NeurIPS 2026)"
status: "Accepted at"
citation: 'Q. Huang, <b>W. Xue</b>, W. Wang, M. Cao, I. Su. "MixUni: Joint multi-property prediction for chemical mixtures with physics-informed heads." <i>Advances in Neural Information Processing Systems (NeurIPS)</i> (2026).'
openreviewurl: "https://openreview.net/forum?id=e3HTIyxtsJ"
codeurl: "https://github.com/qinanh/MixUni"
---

MixUni trains one model on several properties of liquid mixtures relevant to battery-electrolyte design: ionic-liquid conductivity and viscosity, polymer-electrolyte conductivity, and the viscosity and density of solvent mixtures, all from CheMixHub.

- Each component is encoded from its 3D structure by an E(3)-equivariant EGNN; a transformer over components gives one embedding per mixture.
- A property-conditioned sparse mixture-of-experts head is shared across properties.
- For conductivity, the prediction is blended with a physics-informed stretched-Arrhenius head, log σ = log A − B / T<sup>γ</sup>, whose parameters are read from the mixture embedding.
- Five-seed experiments on five CheMixHub tasks show that MixUni matches or improves over single-property geometric baselines, with the largest and most robust gain on chemically out-of-distribution ionic-liquid conductivity.

**My contribution:** I ran the first physics-head probe experiments, which established the value of physics-informed readouts and set the paper's direction; I then led the main physics-head comparison (Arrhenius vs. VTF vs. stretched-Arrhenius vs. free MLP) and ran additional chemically out-of-distribution (Butina-cluster split) seed experiments.
