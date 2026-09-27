# Orchestrator templates

Live templates referenced from `CLAUDE.md`: load when writing, not as standing context.

## Assignment template
```
GOAL
<one sentence: what is different when you are done>

CONTEXT
- Repo/path: <where the work happens>
- Relevant files: <path:line, path:line>
- Conventions to follow: <existing pattern to copy, or "see <file>">
- Already tried / known dead ends: <or "nothing">

SCOPE
In scope:  <the change itself>
Out of scope: <files, refactors, cleanups you must not touch>

ACCEPTANCE CRITERIA
1. <checkable statement>
2. <checkable statement>
3. <exact command> passes, 0 failures, 0 skips

REQUIRED PROOF
Run <exact command> and paste the last 20 lines of output verbatim.
Do not summarize it, do not retype it.

RETURN FORMAT
Use the report template below. Nothing else, no essay.
```

## Report template the agent must return
```
STATUS: DONE | BLOCKED | PARTIAL

CHANGES
- <path:line> - <what changed and why, one line>
- <path:line> - <what changed and why, one line>

PROOF
$ <command>
<verbatim output, last relevant lines>

CRITERIA
1. <criterion> - met, proven by <which output above>
2. <criterion> - met, proven by <which output above>

NOT DONE
- <anything left out, plus the output that shows why> (or "nothing")

RISKS / UNCERTAIN
- <what you are not sure about> (or "none")
```

## REWORK template
```
VERDICT: REWORK

DEFECTS
1. <path:line> - <what is wrong>
   Expected: <the concrete state that ends this defect>
2. <path:line> - <what is wrong>
   Expected: <the concrete state that ends this defect>

UNCHANGED
Goal, scope and acceptance criteria stay exactly as assigned.

PROOF REQUIRED AGAIN
<exact command> plus verbatim output for every defect above.
```

## User-Report template
```
<one line: what state the work is in, failures first>

Done
- <result> (verified: <command or check you ran yourself>)
- <result> (verified: <command or check you ran yourself>)

Not done
- <item> - <cut by user | proven wall, evidence: ... | needs your decision>

Open
- <question, risk, or decision the user has to make>
```
