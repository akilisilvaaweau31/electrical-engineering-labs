# A practical project workflow

## Five terms

| Term | Meaning here |
| --- | --- |
| Repository | One versioned collection of related files |
| Commit | A named snapshot of the changes you chose to save |
| Push | Send local commits to the remote repository |
| Branch | An isolated line of work within the repository |
| Pull request | A reviewable proposal to combine a branch's changes into another branch |

Saving a file in the editor does not create a commit. Creating a local commit does not upload it. Pushing does not prove a project works; your evidence does that.

## A short work session

1. **Choose an outcome.** Example: “Explain why a 12-bit converter has 4,096 codes.”
2. **Read the current project note.** Check the next step, assumptions, and evidence already collected.
3. **Work on one small change.** Save the source and the relevant observation.
4. **Check it.** Recalculate, compile, simulate, or measure only as appropriate to the task.
5. **Review the diff.** A diff shows the exact lines changed. Remove accidental edits and private content from the proposed commit.
6. **Commit and push.** Give the commit a concrete name such as `Explain ADC bin width and endpoint convention`.
7. **Leave a handoff.** Record what changed and one useful next step.

## GitHub Desktop route

Use your existing installation. Select the correct repository, fetch current remote changes, inspect the list of changed files, select only the intended files, write the commit summary, commit, then push. If a conflict or an unexpected repository state appears, stop the merge and inspect it before deciding which content should win.

For ordinary personal notes, a small reviewed commit on your working branch is enough. For a project change that affects behavior, use a short branch and pull request so the diff, purpose, and verification stay together.

## Command line route

These commands assume you are already inside the intended local repository:

```bash
git status
git diff
git diff --cached
```

When the working tree is understood, a new task branch can be created with:

```bash
git switch -c lab/adc-quantization
```

Stage exact paths after reviewing them. Substitute your real project path:

```bash
git add -- c-programming/adc-quantization/README.md
git diff --cached
git commit -m "Document ideal ADC quantization model"
git push -u origin lab/adc-quantization
```

Do not copy a command containing a path you have not checked. Avoid `git add .` when unrelated files or private notes might be present. Do not use force pushes, hard resets, or history rewriting as routine cleanup.

## Useful commit sizes

A commit should tell one story: add an analysis; implement a function; fix a bug and explain the failure; or record a measurement. It can contain several files when they support the same result.

Good: `Record RC step response calculation and assumptions`.

Weak: `stuff`, `update`, or `final final`.

## At the end

Record:

- Current branch and latest commit, when useful.
- Files changed.
- What was checked and what happened.
- Anything still unverified.
- The next concrete action.

The [session handoff template](../../templates/session-handoff.md) is short enough to use without turning every session into paperwork.
