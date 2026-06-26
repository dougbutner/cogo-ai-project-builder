# Architecture

Default posture: **modular monolith** / vertical slices (matches `COGO.md`) unless scale demands otherwise. Patterns here: SaaS, realtime, AI surfaces, marketplaces — anchor boundaries on **domains**, keep deps acyclic.
