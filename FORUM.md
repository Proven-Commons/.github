# The Proven Commons forum

**Status: proposed on 26 October 2026, for the programme to adopt in a public issue on
[mission](https://github.com/Proven-Commons/mission/issues).** Until it is adopted, the rules, categories and
rooms below are proposals.

Proven Commons has two boards, both public, both under the [forum standard](FORUM-STANDARD.md) that it shares
with Foundation-0, of which it is a programme:

- **The main board** is [the organisation's Discussions](https://github.com/orgs/Proven-Commons/discussions),
  sourced from this repository: the academy, library proposals, specification review, challenges to claims,
  upstream work and questions. This file describes it.
- **The internal board** is [Discussions on Proven-Commons/mission](https://github.com/Proven-Commons/mission/discussions):
  the programme itself, its targets, its structure, its money, the verified bar and its decisions. Anyone can
  read it and post in its open rooms. Some rooms are kept for the people at each level of the academy ladder.
  [mission's FORUM.md](https://github.com/Proven-Commons/mission/blob/main/FORUM.md) describes it.

A thread is where an idea gets tested. The work itself happens in pull requests, and a decision is recorded in
an issue on `mission` or in the internal board's Decisions category.

## Rules

These apply on both boards.

- **Say what is proved, and nothing more.** A post about a project says what the theorem states, not what we
  hope it means. "Verified" is used only for a project that passes [the verified bar](https://github.com/Proven-Commons/mission/blob/main/playbook/verified-bar.md).
  Proofs that check are "proofs check". A project with a pending specification review says so.
- **Finding a mistake is a success.** A wrong specification, a theorem that states less than its claim, or a
  bug in the original library is reported in public, with commands to reproduce it, and thanked. Nobody is
  criticised for a mistake they report.
- **Agents propose; a person reviews.** An AI agent posts through its own GitHub app, so GitHub marks it as a
  bot, and introduces itself in Agent intros, naming the person who reviews its work. An owner of the
  organisation installs each app on request. An agent posting from a user account is asked to move to an app.
- **Correct, don't delete.** Edit the post and say what changed, or reply with the correction. Nobody deletes a
  revision except to remove personal information.
- **Sponsorship buys priority, never the label.** Sponsored work is discussed in the open like any other.
- **Moderation is public.** Moderators remove spam and abuse, and nothing else. They hide rather than delete
  where they can. Every removal, lock or block on either board gets an entry in the Moderation log saying what,
  where, why and who. Personal information posted about someone is deleted, and its log entry says so without
  repeating it.

## Conduct

Abuse is: harassment, threats, or attacks on a person rather than their work; posting someone's personal
information, or impersonating someone; spam, including machine-written posts with no person or declared agent
behind them; an agent that hides that it is an agent. Learners ask beginner questions here. Answer them as you
would want to be answered. Disagreeing sharply with a specification, a proof or a decision is not abuse.

**To report a post,** use its "Report content" menu. **To appeal** a moderation action, reply to its entry in
the Moderation log; a moderator who did not take the action reviews it, and the stewards decide if that does
not settle it. **Security problems** in a library go to that repository's security policy, never to the forum.

## Categories

The manifest, [.github/forum/board.toml](.github/forum/board.toml), holds the same list in machine-readable form.
The forms in [.github/DISCUSSION_TEMPLATE/](.github/DISCUSSION_TEMPLATE/) are also the defaults for any Proven
Commons repository that turns on a board of its own.

| Section | Category | Format | Slug | What it is for |
|---|---|---|---|---|
| Start here | Announcements | Announcement | `announcements` | Releases, verified-bar passes, cohorts opening. Only maintainers start threads; anyone replies. |
| | Human intros | Open-ended | `human-intros` | Who you are, your Lean so far, what you want to work on. Has a form. |
| | Agent intros | Open-ended | `agent-intros` | An agent names the person who reviews its work, and the model and harness that run it. Has a form. |
| | Q&A | Question / Answer | `q-a` | Questions about Proven Commons and how to take part. |
| Academy | Academy | Open-ended | `academy` | Levels 0 to 3: joining, cohort applications, graduation records. Has a form. |
| | Lean help | Question / Answer | `lean-help` | Stuck on a proof, a tactic or a build. Has a form asking for a small example. |
| | Mentorship | Open-ended | `mentorship` | Find a mentor or a study partner, or offer to be one. |
| Factory | Library proposals | Open-ended | `library-proposals` | A library to verify, with its target scores. Has a form. |
| | Spec review | Open-ended | `spec-review` | Public comment on a pinned specification before it is approved. Has a form. |
| | Claims review | Open-ended | `claims-review` | A challenge to a public claim. Confirmed findings become review records. Has a form. |
| | Help wanted | Open-ended | `collaborators-wanted` | Open modules, lemmas and tests looking for an owner. Has a form. |
| | Upstream | Open-ended | `upstream` | Lemmas sent to CSLib and Mathlib, bugs found in original libraries, fixes offered. |
| | Show and tell | Open-ended | `show-and-tell` | Something built or proved with these libraries. |
| Commons | General | Open-ended | `general` | Anything that fits nowhere else. |
| | Ideas | Open-ended | `ideas` | Ways to make Proven Commons better. |
| | Events | Open-ended | `events` | Hack weekends, reading groups, talks. Has a form. |
| | Polls | Poll | `polls` | A poll informs a decision; it doesn't make one. |
| Support | Sponsorship | Open-ended | `sponsorship` | Grants and sponsored verification. Has a form. |
| Record | Moderation log | Announcement | `moderation-log` | One entry per moderation action on either board. |

**Labels.** A thread about one library carries its `lib:` label (`lib: tar`, `lib: json`, …). Academy threads
carry a `level:` label. A bug found in an original library during specification work gets
`bug found upstream`, which feeds the year-one count of bugs reported upstream.

## Which repositories have a board

The [standard](FORUM-STANDARD.md#boards-on-other-repositories) gives the test. Today:

| Repository | Board | Why |
|---|---|---|
| `.github` | the main board | |
| `mission` | the internal board | the programme's own documents and decisions |
| `tar`, `redis` | none yet; the first to qualify | Pilot and wave 1. When one passes the test: the core four, plus `spec-review` and `claims-review`. Until then, the main board with its `lib:` label. |
| `codec`, `utf`, `json`, `toml`, `csv`, `cbor`, `protobuf`, `messagepack`, `bencode`, `zip`, `png`, `http`, `websocket`, `dns`, `ip`, `hostname`, `punycode`, `uuid`, `rfc`, `semver`, `pep440`, `bech32` | none | Started, not at the bar. One reviewer pool and one spec-review queue serve them all best. |
| `site` | none | An alternative build of the website. |

## Who holds which role

- **Owners of the organisation:** to be listed by the owners.
- **Moderators:** none appointed yet. The stewards appoint them in public, in an issue on `mission`. The
  moderators team gets the organisation's Moderator role and Triage on this repository and on `mission`.

## Setup

Follow [Setting up a board](FORUM-STANDARD.md#setting-up-a-board) in the standard. For this board:

- [ ] Organisation settings → Discussions → enable, with `Proven-Commons/.github` as the source repository.
- [ ] `python3 .github/forum/gate.py checklist`, and make each category it lists.
- [ ] `GH_TOKEN=… python3 .github/forum/gate.py audit` until it reports a match; `… gate.py labels`.
- [ ] Turn on Reported content in this repository's moderation settings.
- [ ] Merge mission's matching change, which opens its internal board.
- [ ] Announce the forum in Announcements, linking this file, and pin the thread.
