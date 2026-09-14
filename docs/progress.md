# Learning progress

Curriculum revision: 2026-09-13
Last completed session: 01.2 — paths, files, pipes, and redirection
Next session: 01.3 — users, groups, ownership, and permissions
Status: Session 01.2 lab and explain-back reviewed

## Session 01.1 — baseline
- Opened the existing repository in Ubuntu through WSL 2.
- Verified Git 2.43.0 and Python 3.12.3.
- Verified Docker client and engine 29.7.2 communication.
- Reviewed platform purpose and platform/developer ownership boundaries.
- Docker was initially unavailable in Ubuntu; starting Docker Desktop restored access.
- Reviewed staging, commits, and pushes.
- Baseline commit: 1082392; push verified against the remote main branch.

## Session 01.2 — Linux paths and text processing
- Practiced absolute and relative paths, pwd, ls, cd, and the parent directory (..).
- Explained why docs/progress.md is the wrong relative path when already inside docs.
- Used cat and a pipe to pass file contents to grep.
- Saved three matching Docker lines to docs/docker-report.txt.
- Created the synthetic docs/sample-service.log and filtered its two ERROR lines into docs/error-report.txt.
- Lab command: cat docs/sample-service.log | grep ERROR > docs/error-report.txt
- Explained that > creates or overwrites a file and >> appends or creates.
- Correctly predicted that appending the same three lines would produce six lines.
- Review correction: grep ERROR matches anywhere in a line; ^ERROR anchors the match to the start.
- Verification: saved reports matched the corresponding grep output exactly.
- AI help: guided examples, direct file verification, and correction of grep matching semantics.
- Navigation practice was learner-reported; report contents were inspected directly.

## Next session
- Session ID: 01.3
- First action: explain Linux users, groups, ownership, and read/write/execute permissions before a scoped lab.
- Lab: make and repair a deliberately unreadable synthetic file.
- Recall: resolve a relative path from the current directory.
- No cloud resources were created in these sessions.
