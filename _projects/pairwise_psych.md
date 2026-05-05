---
layout: project
title: "pairwise_psych"
description: "Rubygem pairwise fork"
tech: [Ruby, YAML, Testing]
status: "🟢 Live"
link: "https://rubygems.org/gems/pairwise_psych"
featured: true
---

[Pairwise testing](https://en.wikipedia.org/wiki/All-pairs_testing) is a type of combinatorial testing that focuses on generating a smaller set of test cases than a fully exhaustive list of combinations, while still providing good coverage of the input space. It's based on the idea that most faults are caused by interactions between pairs of input parameters, rather than more complex interactions involving three or more parameters, so can get a reasonable amount of confidence by generating test cases that cover all possible pairs of input values.

pairwise_psych is just a fork of the original pairwise gem, updated for newer versions of Ruby.

Many ruby developers of a certain age will get debilitating flashbacks to the syck vs. psych yaml parser updates and that era is the root of my mild ongoing distaste for yaml as a format.
