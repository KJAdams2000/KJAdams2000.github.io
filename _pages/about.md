---
permalink: /
title: "About"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a PhD candidate in theoretical chemistry at the University of Chicago, advised by Prof. Gregory A. Voth. I build physics-grounded machine-learning methods and HPC software for molecular simulation, and bottom-up coarse-grained (CG) models that reach biological length and time scales. Before UChicago, I earned a B.S. in Chemistry with a minor in Physics from Peking University.

My central idea is that **bottom-up coarse-graining is maximum-likelihood training of an energy-based model on all-atom data**. Latent variables make these models expressive while keeping them cheap: the joint energy stays pairwise, and the marginal becomes many-body. In Self-Consistent Ultra-Coarse-Graining ([SC-UCG, *J. Chem. Phys.* 2026](/publications/2026-11-01-sc-ucg-jcp/)), the discrete internal states of each CG molecule are inferred by graph message passing at simulation time, and the force field is trained with MISC, a KL-derived objective that needs no re-sampling of intermediate models. Physics also supplies hard generalization tests: trained at a single temperature (*T* = 4.3), SC-UCG places a 3D-Ising-class chiral symmetry-breaking transition near *T*<sub>c</sub> ≈ 4.4.

I apply the same toolkit to large biomolecular assemblies: from terabyte-scale all-atom trajectories of ~30-million-atom microtubule lattices, I built a bottom-up CG tubulin model showing that intrinsic lattice instability drives protofilament clustering at microtubule plus-end tips ([*Biophys. J.* 2026](/publications/2026-04-01-microtubule-lattice-instability-bpj/)). On the ML side, I co-authored [MixUni (NeurIPS 2026)](/publications/2026-12-01-mixuni-neurips/), an E(3)-equivariant multi-property model for chemical mixtures with a physics-informed conductivity head. I am also a core developer of [AceCG](https://github.com/AceVolca/AceCG), an MPI-parallel coarse-grained force-field training engine.

Research interests
------
- **Bottom-up coarse-graining as energy-based / latent-variable machine learning**: relative-entropy (likelihood) training, message-passing inference of hidden states, virtual-particle models
- **Machine-learning force-field training**: force matching, denoising score matching, and likelihood objectives at HPC scale
- **Multiscale biomolecular simulation**: microtubules and other many-protein assemblies, from all-atom MD to CG models
- **AI for science**: physics-informed architectures and readouts, equivariant GNNs, property prediction for materials and mixtures

*Current interests:* latent-variable energy-based models, ML for quantum nuclear dynamics.

News
------
- **Nov 2026**: Our SC-UCG paper, "Next generation of ultra-coarse-graining: Self-consistent inference of critical internal states," is published in [*The Journal of Chemical Physics*](https://doi.org/10.1063/5.0352901).
- **2026**: [MixUni](https://openreview.net/forum?id=e3HTIyxtsJ), joint multi-property prediction for chemical mixtures with physics-informed heads, is accepted at **NeurIPS 2026**. Code: [qinanh/MixUni](https://github.com/qinanh/MixUni).
- **Oct 2026**: Poster at the UChicago–Caltech AI+Science Conference: "A unified latent-variable framework for coarse-grained energy-based models."
- **Aug 2026**: Two talks and a poster at ACS Fall 2026 in Chicago, on ultra-coarse-graining for multistate systems, CD-REM for virtual-site coarse-graining, and free-energy-matching CG. See [Talks](/talks/).
- **2026**: First-author paper on protofilament clusters at microtubule plus-end tips published in [*Biophysical Journal*](https://doi.org/10.1016/j.bpj.2026.02.013).
