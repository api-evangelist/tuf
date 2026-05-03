# The Update Framework (TUF)

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
