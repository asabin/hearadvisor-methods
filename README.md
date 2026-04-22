# HearAdvisor Methods

Public source for HearAdvisor's methodology documentation — the procedures we use to record, measure, and score hearing aids and earplugs. Every score, rating, and recording published on [HearAdvisor.com](https://www.hearadvisor.com) is produced in accordance with what's documented here.

**Canonical site:** [www.hearadvisor.com/methods](https://www.hearadvisor.com/methods)

## What's in here

The `docs/` tree is an [MkDocs](https://www.mkdocs.org/) project (Material theme) covering two product methodologies:

| Section | What it documents |
| --- | --- |
| [`docs/hearing-devices/`](docs/hearing-devices) | KEMAR manikin recordings, acoustic scene design, device fitting, and the metrics behind SoundScore (speech perception benefit, occlusion, music streaming quality, feedback). |
| [`docs/earplugs/`](docs/earplugs) | Perceptual loudness reduction and sound-quality evaluation for earplugs, using the same lab plus auditory-science models. |

Shared files of note:

- [`docs/changelog.md`](docs/changelog.md) — human-readable summary of every methodology change.
- [`docs/how-to-cite.md`](docs/how-to-cite.md) — recommended citation format (see also the [Citing](#citing) section below).
- [`docs/references.md`](docs/hearing-devices/references.md) in each section — full bibliographies.
- [`mkdocs.yml`](mkdocs.yml) — site configuration and navigation.

## Living document

This documentation is maintained as a living standard. Every change is committed to `main` and deployed automatically, so `git log` is the authoritative record of what changed and when. For a narrative summary, see the [changelog](docs/changelog.md); for upcoming work, the [public roadmap](https://github.com/users/asabin/projects/1).

Prior snapshots of the methodology were published as OSF whitepapers (see [How to Cite](docs/how-to-cite.md)) and are not updated — always refer to the canonical site for the current procedure.

## Contributing

We welcome questions and feedback from the hearing-care community:

- **Ask a methodology question:** [open an issue](https://github.com/asabin/hearadvisor-methods/issues/new?template=methodology-question.md)
- **Suggest an improvement:** [open an issue](https://github.com/asabin/hearadvisor-methods/issues/new?template=feedback.md)

Pull requests for typos, broken links, or clarifications are also welcome.

## Building locally

```bash
pip install mkdocs-material mkdocs-git-revision-date-localized-plugin
mkdocs serve
```

Then open `http://localhost:8000`. The site is deployed to GitHub Pages on every push to `main` via [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml); the public-facing canonical URL (`www.hearadvisor.com/methods`) embeds that build.

## Citing

See [How to Cite](docs/how-to-cite.md) for the full citation format and BibTeX entry. In short:

> Sabin, A., Taddei, S., & Bailey, A. *HearAdvisor methodology documentation.* HearAdvisor LLC. Retrieved [date], from https://www.hearadvisor.com/methods/

When citing, include the access date so readers can locate the version you referenced in the git history.

## Authors

- Andrew Sabin, Ph.D.
- Steve Taddei, Au.D.
- Abram Bailey, Au.D.

## License

Copyright © HearAdvisor LLC. All rights reserved.
