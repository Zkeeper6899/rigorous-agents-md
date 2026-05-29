# Rigorous AGENTS.md

A reusable `AGENTS.md` profile for AI assistants, coding agents, and research-oriented workflows that need rigorous reasoning, uncertainty awareness, and practical engineering judgment.

This project is designed for people who want an assistant that is less likely to fabricate citations, overstate confidence, hide assumptions, or give one-size-fits-all technical advice.

## What It Optimizes For

- Verifiable, objective, and source-aware answers.
- Clear separation between facts, assumptions, inferences, experience-based judgment, and recommendations.
- Constructive pushback when the user's premise or proposed direction is weak.
- Practical engineering reasoning instead of purely abstract explanation.
- Flexible response structure based on the actual question, not a fixed template.
- Tradeoff analysis when multiple reasonable routes exist.

## What It Does Not Do

- It does not guarantee correctness.
- It does not replace official documentation, source code, papers, experiments, or expert review.
- It is not limited to one technical field.
- It is not a prompt for making answers longer by default.

## Files

- [`AGENTS.md`](./AGENTS.md): The reusable instruction profile.
- [`examples/chatgpt-custom-instructions.md`](./examples/chatgpt-custom-instructions.md): A version adapted for ChatGPT custom instructions.
- [`examples/domain-adaptations.md`](./examples/domain-adaptations.md): Optional domain-specific extensions.
- [`examples/before-after.md`](./examples/before-after.md): A small example showing the intended behavioral difference.

## Recommended Use

Copy `AGENTS.md` into the root of a project that supports agent instruction files, or adapt the content into your assistant's custom instruction settings.

If your tool supports packaged skills, this profile can also be wrapped as a skill. Keep the repository centered on `AGENTS.md` unless you are publishing an installable skill package with its own manifest, runtime assumptions, and invocation rules.

For tools that support layered instructions, the recommended pattern is:

- Global or personal instructions: put this profile there to define long-term reasoning style.
- Project-level instructions: add repository facts such as build commands, test commands, architecture notes, coding conventions, and trusted sources of truth.
- Directory-level instructions: add local rules for specific modules only when those rules are narrower than the project-level guidance.

This repository intentionally provides the first layer. It does not replace project-specific instructions.

## Skill Compatibility

The word "skill" is useful when the project provides a packaged capability that an agent can install, discover, and invoke. This project is currently a portable instruction profile: users can copy it into `AGENTS.md`, adapt it for ChatGPT custom instructions, or wrap it into a skill in their own toolchain.

Keeping the name focused on `AGENTS.md` makes the artifact clear and discoverable. If a packaged skill is added later, it can live alongside the core profile without renaming the whole project.

## Adaptation Guide

Keep the core reasoning rules stable, then add a short domain section only when it changes the assistant's behavior in a useful way.

Good domain additions are concrete:

- "When discussing AI papers, distinguish the paper's claims from independently verified results."
- "When reviewing cloud architecture, include operational risk and migration cost when relevant."
- "When discussing security, avoid overclaiming exploitability without a threat model."

Weak domain additions are vague:

- "Be smarter."
- "Give high-quality answers."
- "Always be detailed."

## Design Notes

The profile intentionally biases the assistant toward rigor over fluency. It asks the assistant to say "I don't know" when evidence is missing, to name uncertainty instead of smoothing it over, and to compare alternatives when a problem has more than one defensible solution.

It was inspired by the broader ecosystem of open-source agent instruction files, but the focus here is rigorous reasoning and practical engineering judgment rather than a single tool or domain.

## Acknowledgements

This project was inspired in part by open-source agent instruction projects such as [`multica-ai/andrej-karpathy-skills`](https://github.com/multica-ai/andrej-karpathy-skills).

## License

MIT
