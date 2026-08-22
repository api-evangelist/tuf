# The Update Framework (TUF)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

TUF is a CNCF graduated framework for securing software update systems. It provides a
specification for how software repositories should be structured and how clients should
verify updates, protecting against key compromise, rollback attacks, freeze attacks, and
mix-and-match attacks. TUF is used by PyPI, Sigstore, and many other software distribution systems.

**Website:** https://theupdateframework.io

**APIs.yml:** https://raw.githubusercontent.com/api-evangelist/tuf/refs/heads/main/apis.yml

## Scope

- **Type:** Index
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- CNCF
- Cloud Native
- Graduated
- Security
- Software Supply Chain
- Software Updates
- Verification

## Specification

- **TUF Spec:** https://theupdateframework.github.io/specification/latest/
- **GitHub:** https://github.com/theupdateframework/specification

## Implementations

| Language | Repository | Package |
|---|---|---|
| Python (reference) | [theupdateframework/python-tuf](https://github.com/theupdateframework/python-tuf) | [PyPI: tuf](https://pypi.org/project/tuf/) |
| Go | [theupdateframework/go-tuf](https://github.com/theupdateframework/go-tuf) | — |
| JavaScript | [theupdateframework/tuf-js](https://github.com/theupdateframework/tuf-js) | — |
| Rust | [theupdateframework/rust-tuf](https://github.com/theupdateframework/rust-tuf) | — |

## Tools

| Tool | Description |
|---|---|
| [tuf-on-ci](https://github.com/theupdateframework/tuf-on-ci) | TUF repository signing via CI/CD |
| [tuf-conformance](https://github.com/theupdateframework/tuf-conformance) | Client conformance test suite |

## Schemas

### JSON Schema

| File | Description |
|---|---|
| [json-schema/tuf-root-metadata-schema.json](json-schema/tuf-root-metadata-schema.json) | Root metadata schema (trust anchor) |
| [json-schema/tuf-targets-metadata-schema.json](json-schema/tuf-targets-metadata-schema.json) | Targets metadata schema (file inventory) |
| [json-schema/tuf-snapshot-metadata-schema.json](json-schema/tuf-snapshot-metadata-schema.json) | Snapshot metadata schema (consistency) |
| [json-schema/tuf-timestamp-metadata-schema.json](json-schema/tuf-timestamp-metadata-schema.json) | Timestamp metadata schema (freshness) |

### JSON Structure

| File | Description |
|---|---|
| [json-structure/tuf-root-metadata-structure.json](json-structure/tuf-root-metadata-structure.json) | Root metadata field structure |
| [json-structure/tuf-targets-metadata-structure.json](json-structure/tuf-targets-metadata-structure.json) | Targets metadata field structure |

### JSON-LD

| File | Description |
|---|---|
| [json-ld/tuf-context.jsonld](json-ld/tuf-context.jsonld) | Linked data context for TUF metadata types |

## Examples

| File | Description |
|---|---|
| [examples/tuf-root-metadata-example.json](examples/tuf-root-metadata-example.json) | Example root.json metadata file |
| [examples/tuf-targets-metadata-example.json](examples/tuf-targets-metadata-example.json) | Example targets.json with software packages |
| [examples/tuf-python-client-usage-example.json](examples/tuf-python-client-usage-example.json) | Using python-tuf ngclient for updates |

## Vocabulary

| File | Description |
|---|---|
| [vocabulary/tuf-vocabulary.yml](vocabulary/tuf-vocabulary.yml) | TUF domain vocabulary and attack protection concepts |

## CNCF

TUF is a CNCF graduated project: https://www.cncf.io/projects/the-update-framework-tuf/

## Timestamps

- **Created:** 2026-03-16
- **Modified:** 2026-05-03

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
