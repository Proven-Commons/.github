# Proven Commons

Proven Commons rewrites widely used software libraries in [Lean](https://lean-lang.org/) and proves that the new code follows its written specification. It is a programme of Foundation-0, a non-profit organisation. It also trains future verifiers on live work: trainees learn by shipping real verified modules, with a mentor checking their work.

A finished project publishes four things: the library, the specification, a proof a computer can check, and a test report that compares the new code against the original on millions of inputs.

[Website](https://proven-commons.github.io/mission/) · [Mission and founding brief](https://github.com/Proven-Commons/mission) · [Open issues and decisions](https://github.com/Proven-Commons/mission/issues)

## The verified bar

A project may use the word verified in public only when all of these hold:

- The specification is public and was approved by a reviewer apart from the author.
- The build has no `sorry` or `admit`.
- `#print axioms` on each main theorem shows only the standard Lean axioms.
- Differential tests against the original ran, and the count, seed, and result are in the repo.
- The public page lists what is outside the proof: runtime, compiler, hardware, and any unverified code.
- A stranger can clone the repo, run one command, and re-check the proof.

## Repos

One repo per library, named for the software it verifies. Each carries its own proof check, releases, and page.

**Programme**

- [mission](https://github.com/Proven-Commons/mission): the README, the founding brief, the website, and the issues where targets and decisions are discussed.
- [site](https://github.com/Proven-Commons/site): an alternative build of the website that lays out the mission repo's documents.

**Pilot**

- [tar](https://github.com/Proven-Commons/tar): a tar (ustar) extractor with a proved rule that no file in an archive can be written outside the destination folder. Its README states what is proved, what is not proved, and the recorded test results.

**Started.** These repos are open. Work has not reached the verified bar yet, and none of them claims it.

| Area | Repos |
| --- | --- |
| Encodings | [codec](https://github.com/Proven-Commons/codec) (base64, hex, CRC-32), [utf](https://github.com/Proven-Commons/utf) (UTF-8), [bech32](https://github.com/Proven-Commons/bech32) (BIP 173, BIP 350), [punycode](https://github.com/Proven-Commons/punycode), [der](https://github.com/Proven-Commons/der) (ASN.1 DER element reader, X.690) |
| Data formats | [json](https://github.com/Proven-Commons/json), [toml](https://github.com/Proven-Commons/toml), [csv](https://github.com/Proven-Commons/csv) (RFC 4180), [cbor](https://github.com/Proven-Commons/cbor) (RFC 8949), [protobuf](https://github.com/Proven-Commons/protobuf) (wire format), [messagepack](https://github.com/Proven-Commons/messagepack), [bencode](https://github.com/Proven-Commons/bencode), [xml](https://github.com/Proven-Commons/xml) (safe subset, no document type declarations, no entities) |
| Archives and files | [zip](https://github.com/Proven-Commons/zip), [png](https://github.com/Proven-Commons/png) (chunks and CRC-32), [path](https://github.com/Proven-Commons/path) (lexical path cleaning) |
| Network protocols | [http](https://github.com/Proven-Commons/http) (RFC 9112 request line and headers), [websocket](https://github.com/Proven-Commons/websocket) (RFC 6455 frames), [dns](https://github.com/Proven-Commons/dns) (RFC 1035 header and question), [ip](https://github.com/Proven-Commons/ip) (addresses), [mqtt](https://github.com/Proven-Commons/mqtt) (MQTT 5.0 packet framing), [ntp](https://github.com/Proven-Commons/ntp) (wire packet parser), [dhcpv4](https://github.com/Proven-Commons/dhcpv4) (wire message parser), [clienthello](https://github.com/Proven-Commons/clienthello) (TLS ClientHello, RFC 8446), [ssh](https://github.com/Proven-Commons/ssh) (wire types and key blobs), [uri](https://github.com/Proven-Commons/uri) (reference resolution, RFC 3986), [hpack](https://github.com/Proven-Commons/hpack) (stateless part, RFC 7541) |
| Identifiers and versions | [uuid](https://github.com/Proven-Commons/uuid) (RFC 9562), [rfc](https://github.com/Proven-Commons/rfc) (RFC 3339 timestamps), [semver](https://github.com/Proven-Commons/semver), [pep440](https://github.com/Proven-Commons/pep440), [hostname](https://github.com/Proven-Commons/hostname) |
| Tokens | [jws](https://github.com/Proven-Commons/jws) (compact serialization parser and claim checks) |
| Wave 1 | [redis](https://github.com/Proven-Commons/redis) (RESP parser and small key-value store), [sqlite](https://github.com/Proven-Commons/sqlite) (file-format reader: header, pages, records), [cedar](https://github.com/Proven-Commons/cedar) (Cedar-style policy engine) |

Wave 1 is open, not planned: redis and sqlite have a first slice on main, and cedar has a repo. Most of the repos above have a first slice on main. These repos hold a plan and no Lean code on main yet: cbor, http, uri, cedar, jws, mqtt, ntp, dhcpv4, clienthello, xml.

Each project sends reusable lemmas to [CSLib](https://github.com/leanprover/cslib) and [Mathlib](https://github.com/leanprover-community/mathlib4), the shared libraries for computer science and mathematics in Lean. The shared library grows. The next project starts cheaper.

## Learn here

- Level 0, Reader: Lean basics and a small codec proof. Two weeks, open to all.
- Level 1, Apprentice: one lemma or parser function inside a live project. Eight weeks.
- Level 2, Verifier: own a module from specification to proof to public page.
- Level 3, Spec Lead and Mentor: write and review specifications, run a squad, teach Level 1.

Graduation at each level is merged work that a computer checked. That record is the proof of work an employer can check in minutes.

## Get involved

- [Introduce yourself](https://github.com/Proven-Commons/.github/discussions/new?category=human-intros), or [join the academy](https://github.com/Proven-Commons/.github/discussions/new?category=academy)
- [Propose a library to verify](https://github.com/Proven-Commons/.github/discussions/new?category=library-proposals)
- [Review a specification](https://github.com/orgs/Proven-Commons/discussions/categories/spec-review) or [challenge a claim](https://github.com/Proven-Commons/.github/discussions/new?category=claims-review)
- [Support the public factory](https://github.com/Proven-Commons/.github/discussions/new?category=sponsorship)

The [forum](https://github.com/orgs/Proven-Commons/discussions) is open to everyone. How the programme itself is
run is discussed, in public, on [mission's board](https://github.com/Proven-Commons/mission/discussions).
[FORUM.md](https://github.com/Proven-Commons/.github/blob/main/FORUM.md) has the rules.
