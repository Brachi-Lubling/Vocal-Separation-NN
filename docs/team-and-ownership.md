# Team and Phase Ownership

Status: **Draft — pending Nadav readiness review.**

This project is built by a two-person team. Commit attribution follows **phase ownership**:
each phase is owned by one teammate, and **all commits for that phase are authored and
committed under that teammate's identity** (attribution is per phase / area of responsibility,
not alternated commit-by-commit).

## Contributors

| Name             | Git name         | Email                    |
|------------------|------------------|--------------------------|
| Elisheva Kerbel  | `Elisheva-Kerbel`| `ch355739@gmail.com`     |
| Brachi Lubling   | `Brachi-Lubling` | `brachil5119@gmail.com`  |

> **GitHub credit note:** for the contribution graph to credit each teammate, her email above
> must be added to her own GitHub account (Settings → Emails). The commit author/committer is
> set correctly regardless, but GitHub links a commit to an account by verified email.

## Phase ownership (split by subsystem)

| Phase | Title                                   | Owner    |
|-------|-----------------------------------------|----------|
| 0     | Dockerized project skeleton             | Elisheva |
| 1     | AI benchmark harness                    | Elisheva |
| 2     | Backend domain + DB skeleton            | Brachi   |
| 3     | Auth / user account foundation          | Brachi   |
| 4     | Upload + private storage                | Elisheva |
| 5     | Queue + worker processing               | Brachi   |
| 6     | Result page + secure file access        | Brachi   |
| 7     | Quotas + coupons                        | Elisheva |
| 8     | My library                              | Elisheva |
| 9     | Public library                          | Brachi   |
| 10    | Admin RBAC + audit                      | Brachi   |
| 11    | Settings + account deletion             | Brachi   |
| 12    | QA hardening + release readiness        | Elisheva |

- **Elisheva (6):** 0, 1, 4, 7, 8, 12 — foundation, AI, upload, business & release.
- **Brachi (7):** 2, 3, 5, 6, 9, 10, 11 — backend/DB, auth, processing, secure access, sharing/admin/account.

Additional component ownership:

| Component | Owner |
|-----------|-------|
| FAST-DEMO local inference vertical slice | Brachi |
| VocalSplit Academy learning site | Brachi |

Areas of responsibility: Elisheva owns the foundation, AI, upload and
user-content/business tracks; Brachi owns the backend domain/DB, auth, processing,
security/access/admin and local demo/learning tracks.

The existing project history across `master` and `gh-pages` is attributed 22 commits
to each contributor. The distribution is by coherent component ownership, not alternating
authors commit-by-commit.

## How to commit under the right identity

Set author **and** committer per commit so both match the phase owner:

```bash
# Elisheva's phases
git -c user.name="Elisheva-Kerbel" -c user.email="ch355739@gmail.com" commit -F <msgfile>

# Brachi's phases
git -c user.name="Brachi-Lubling"  -c user.email="brachil5119@gmail.com" commit -F <msgfile>
```

Convenience aliases (configured locally in `.git/config`, not tracked):

```bash
git ce   # commit as Elisheva
git cb   # commit as Brachi
```

## Rules

- Commit messages are attributed **only** to Elisheva or Brachi (no other co-author trailers).
- One phase → one owner. Do not mix owners within a phase's commits.
- Follow `git-workflow.md` for commit cadence, size and message style.
- This mapping may be adjusted by the team; update this table if ownership changes.
