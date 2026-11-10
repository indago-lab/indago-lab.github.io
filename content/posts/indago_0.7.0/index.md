---
date: '2026-11-09T23:00:00+01:00'
draft: false
title: 'Indago 0.7.0 released'
linkto:
    - "software/indago"
images: []
featuredImage: "indago_0.7.0.jpg"
---

A long waited release of Indago has finally arrived! With a bunch of exciting novelties!

We migrated Indago code to GitHub [https://github.com/indago-lab/indago](https://github.com/indago-lab/indago) and made a significant overhaul to the code, while adding new useful features and optimization methods.

The PyPI installation ([https://pypi.org/project/Indago](https://pypi.org/project/Indago)) and the documentation ([https://indago.readthedocs.io/index.html](https://indago.readthedocs.io/index.html)) are updated. 

Released on 2026-11-09

### New features
- **Variable types and mixed-variable support**
- **New method: CMAES**
- New PSO variant `'CL'` implementing Comprehensive Learning PSO (CLPSO)
- New DE variant `'RankLSHADE'` supporting constraints
- New DE variant `'iLSHADE'` implementing the improved LSHADE algorithm
- New DE variant `'jSO'` implementing the jSO algorithm
- Changes in available anakatabatic models for Vanilla PSO: `'DoubleSummit'` added, `'MessyTie'` removed <i class="fa-solid fa-triangle-exclamation"></i>
- New default anakatabatic models when using anakatabatic inertia in PSO: `'TipsySpider'` for Vanilla PSO and `'OrigamiSnake'` for TVAC PSO <i class="fa-solid fa-triangle-exclamation"></i>
- Introducing new default PSO variant (`'Flagship'`), representing "best in show" of all PSO (sub-)variants. Using this variant you get Vanilla PSO with anakatabatic inertia and `'TipsySpider'` anakatabatic model, which has shown to be the overall best implemented version of PSO in our rather extensive testing <i class="fa-solid fa-triangle-exclamation"></i>
- Utility functions `inspect`, `inspect_optimizers` and `minimize_exhaustive` have been removed <i class="fa-solid fa-triangle-exclamation"></i>
### Improvements
- **Significant code refactoring, making Indago ready for future extensions**
- Removed BA and MRFO due to uncompetitive performance <i class="fa-solid fa-triangle-exclamation"></i>
- Removed MSGD for the time being (future reimplementation planned) <i class="fa-solid fa-triangle-exclamation"></i>
- `Optimizer.evaluation_function` renamed to `Optimizer.evaluator` <i class="fa-solid fa-triangle-exclamation"></i>
- For compatibility with mixed-variable optimization, `Candidate.X0` is now a `tuple` or a `list` of `tuple` instead of an `ndarray` (or `int`, as previously) <i class="fa-solid fa-triangle-exclamation"></i>
- Members for `VariableType` and `XFormat` enums are now following PEP-8 naming conventions (CONSTANT_CASE)
- Enum `Status` is renamed to `OptimizerStatus`
- Documentation updated and improved
### Bug fixes
- Fixed NM not working when initialized at the upper bounds
- Many minor bug fixes
