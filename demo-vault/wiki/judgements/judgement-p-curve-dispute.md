---
type: judgement
title: "Do published p-value distributions show p-hacking to be widespread? Head et al. against Bishop and Thompson"
description: The maintainer's recorded view on the dispute between Head et al. (2015) and Bishop and Thompson (2016), with Hartgerink's (2017) reanalysis, over whether the distribution of published p-values shows p-hacking to be widespread.
created: 2026-09-23
updated: 2026-09-23
sources: [bishop-2016, hartgerink-2017, head-2015]
status: draft
generated:
  by: claude-code/claude-fable-5-1
  at: 2026-09-23
author: maintainer
---

# Do published p-value distributions show p-hacking to be widespread?

Recorded 2026-09-23 by the maintainer. This page is the maintainer's own view, not a finding of any source. For the dispute itself, see [[p-curve-as-evidence]].

## Verdict

On whether published p-value distributions show p-hacking to be widespread, I find Bishop and Thompson more persuasive than Head et al.: these distributions do not show that p-hacking is widespread.

## Reason

The decisive limit is that a surplus of p-values just below .05 cannot establish how many studies were p-hacked, because some forms of p-hacking produce no surplus at all and the size of any surplus depends on quantities that real data do not reveal [[bishop-2016]]. Head et al.'s surplus also changes under Hartgerink's defensible reanalysis of the same data, whose paper-level sampling is unclear [[hartgerink-2017]]. Head et al. report their result correctly and document misreported p-values [[head-2015]], but neither settles prevalence.

## What would change my mind

A reproducible analysis of focal, recalculated p-values, validated against known study-level analysis histories, showing that its signal reliably distinguishes widespread p-hacking from reporting and selection effects.
