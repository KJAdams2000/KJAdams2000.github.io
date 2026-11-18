---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<a href="{{ base_path }}/files/Weizhi_Xue_CV.pdf" class="btn btn--primary">Download full CV (PDF)</a>

Education
======
* **Ph.D. Candidate in Theoretical Chemistry**, The University of Chicago, 2023–present (expected June 2028)
  * Advisor: Prof. Gregory A. Voth
  * M.S. in Chemistry, December 2024
* **B.S. in Chemistry, Minor in Physics**, Peking University, College of Chemistry and Molecular Engineering, 2019–2023
  * "Chemistry Star," the department's highest honor degree
  * B.S. thesis advisor: Prof. Yiqin Gao

Research experience
======
* **Graduate Research Assistant, Voth Group**, The University of Chicago, 2023–present
  * Unified latent-variable framework for coarse-grained energy-based models: Ultra-Coarse-Graining (observable discrete latents) and virtual-particle CG (unobservable particle latents) as two instances of one construction.
  * Self-Consistent Ultra-Coarse-Graining (first author, *J. Chem. Phys.* 2026): message-passing inference of internal states, MISC training without iterative sampling, and temperature transferability across a chiral phase transition.
  * Multiscale microtubule modeling (first author, *Biophys. J.* 2026; co-author, *Biophys. J.* 2025 and 2026).
  * Mentored 2 summer students on testing and applications of SC-UCG (2025).
* **Collaborative machine-learning research: MixUni** (NeurIPS 2026, second author), The University of Chicago, 2026
  * Ran the first physics-head probe experiments, which established the value of physics-informed readouts and set the paper's direction; led the main physics-head comparison (Arrhenius vs. VTF vs. stretched-Arrhenius vs. free MLP).
* **Visiting Undergraduate Research Intern, Voth Group**, The University of Chicago (remote), Jul–Sep 2022
  * Co-developed K-means clustering coarse-graining (KMC-CG; co-first author, *JCTC* 2023).
* **Undergraduate Research Intern, Gao Group**, Peking University, Mar 2022–May 2023
  * Computational prediction of ligand-induced conformational changes and their free-energy profiles; code contributions to the GPU MD engine SPONGE.

Publications
======
<p>(<sup>&dagger;</sup> equal contribution)</p>
<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

Presentations
======
<ul>{% for post in site.talks reversed %}
  {% include archive-single-talk-cv.html %}
{% endfor %}</ul>

Software
======
* **AceCG** (core developer): MPI-parallel coarse-grained force-field training engine. [GitHub](https://github.com/AceVolca/AceCG)
* **LAMMPS-UCG-dev** (author): LAMMPS package for lambda-dynamics UCG and SC-UCG. [GitHub](https://github.com/KJAdams2000/LAMMPS-UCG-dev)
* **TorchREM** (author): PyTorch relative-entropy trainer for CG MD. [GitHub](https://github.com/KJAdams2000/TorchREM)

See the [Software](/software/) page for details.

Honors and awards
======
* George Herbert Jones Fellowship, Department of Chemistry, University of Chicago (2025)
* Olshensky Student Travel Award, Department of Chemistry, University of Chicago (2024, 2025)
* "Chemistry Star," highest honor degree in the Department of Chemistry, Peking University (2023)
* Model Student of Academic Records, Peking University (2020, 2021, 2022), with the Zheng Yongxi (2020), Peking University (2021), and POSCO (2022) Scholarships
* Gold Medal, Chinese Chemistry Olympiad (2018)

Teaching and mentoring
======
* Tutor and grader, CHEM 364 Advanced Statistical Mechanics, University of Chicago (Winter 2025, Winter 2026)
* Tutor and grader, CHEM 365 Chemical Dynamics (Spring 2025)
* Tutor and grader, CHEM 261 Introductory Quantum Mechanics (Fall 2025)
* Teaching Assistant, CHEM 111/112/113 General Chemistry sequence (Fall 2023–Spring 2024)
* Research mentor, PKU–UChicago Summer Research Program (2024, 2025)

Skills
======
* **Languages and HPC:** Python, C/C++, CUDA, MPI (mpi4py), Numba, Bash, SLURM clusters, Git, LaTeX
* **Machine learning:** PyTorch, PyTorch Geometric, NumPy/SciPy, pandas; equivariant GNNs, energy-based and latent-variable models, score matching, mixture-of-experts, multi-task learning
* **Simulation:** LAMMPS, GROMACS, OpenMM, PLUMED, AmberTools, SPONGE, Gaussian, MDAnalysis, MDTraj, OpenMSCG; enhanced sampling, free energy perturbation, coarse-graining (FM/MS-CG, REM, IBI, UCG)
