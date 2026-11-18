---
layout: archive
title: "Software"
permalink: /software/
author_profile: true
---

Research software I develop for coarse-grained force-field training and simulation. All repositories below are public on GitHub.

AceCG: A Comprehensive Engine for Coarse-Graining
------
**Core developer** · Python, MPI (mpi4py), Numba, LAMMPS · 2025–present · [github.com/AceVolca/AceCG](https://github.com/AceVolca/AceCG)

AceCG is an MPI-parallel engine that takes all-atom MD to trained coarse-grained force fields for LAMMPS. It covers force matching (the standard ML force-field loss), denoising score matching, noise-augmented force matching, and likelihood (relative-entropy) training, along with conditional-derivative REM/FM, virtual-particle workflows, and trajectory mapping.

- Led the architecture rewrite of the ~43k-line code base into a 7-layer design (potentials → topology → I/O and config → compute runtime → trainers/optimizers → scheduler → workflows), in which each layer depends only on the one below; largest contributor by code volume.
- Built MPI CPU parallelism, a multitask scheduler and resource pool, unified topology management, parallel compute backends, YAML config parsing, and the command-line interface (`acg-fm`, `acg-rem`, `acg-cdrem`, `acg-dsm`, `acg-trajmap`, …).
- Implemented denoising score matching, noisy and mixed-noise force matching, noisy REM, and batched compute backends; added trajectory mapping with linear force mapping, dihedral B-spline potentials, on-the-fly validation simulations, and versioned force-field caching; wrote developer documentation and prepared the package for PyPI release.

LAMMPS-UCG-dev
------
**Author** · C++, MPI, LAMMPS · 2024–2025 · [github.com/KJAdams2000/LAMMPS-UCG-dev](https://github.com/KJAdams2000/LAMMPS-UCG-dev)

A LAMMPS package and patcher for lambda-dynamics ultra-coarse-graining (UCG) and Self-Consistent UCG ([*J. Chem. Phys.* 2026](/publications/2026-11-01-sc-ucg-jcp/)). Internal-state inference runs at simulation time inside the MD engine, with MPI parallelism.

TorchREM and OpenMSCG-dev
------
**Author** · PyTorch · 2024–2025 · [github.com/KJAdams2000/TorchREM](https://github.com/KJAdams2000/TorchREM) · [github.com/KJAdams2000/OpenMSCG-dev](https://github.com/KJAdams2000/OpenMSCG-dev)

TorchREM is a PyTorch-based relative-entropy minimization (REM) trainer for coarse-grained MD, used for the SC-UCG training workflows. OpenMSCG-dev extends OpenMSCG with UCG-weighted REM, internal-state I/O, and the Adam optimizer.

Related research code
------
- **MixUni** (NeurIPS 2026, co-author): joint multi-property prediction for chemical mixtures with physics-informed heads. [github.com/qinanh/MixUni](https://github.com/qinanh/MixUni)
