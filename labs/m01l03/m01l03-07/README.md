# m01l03-07 · Ask your own interpreter what it is

**Lesson:** [What Python Is, And Where It Came From](https://learnsome.tech/learn/python-course/m01l03) (lesson 1.3, module 1: Before You Write Code) · Free  
**Check:** Graded

## Goal

You can describe what kind of language Python is, place its origin and the two versus three split in time, read a Python version number, and ask your own interpreter which version, platform and implementation you are running.

## Files

- [`starter/shell-ask-your-own-interpreter-what-it-is.py`](starter/shell-ask-your-own-interpreter-what-it-is.py): the listing from the lesson
- [`expected.txt`](expected.txt): the output the check compares with
- [`check.json`](check.json): how `./check` runs and checks this lab

## Steps

1. Go to the starter: `cd labs/m01l03/m01l03-07/starter`
2. Read `shell-ask-your-own-interpreter-what-it-is.py`.
3. The session types these lines at the `>>>` prompt, in order:

   ```python
   import sys
   sys.version_info
   sys.version_info.major
   sys.platform
   sys.implementation.name
   ```
4. Run it: `python3 -i < shell-ask-your-own-interpreter-what-it-is.py`.
5. Check it from the repository root: `./check m01l03-07`.

## Expected output

```text
sys.version_info(major=3, minor=14, micro=7, releaselevel='final', serial=0)
3
'linux'
'cpython'
```

## How to check

`./check m01l03-07` copies `starter/` into a scratch directory and runs `python3 -i < shell-ask-your-own-interpreter-what-it-is.py` there, the way the site's lab sandbox does: that directory is the working directory and `HOME`, `LANG=C.UTF-8`, `TZ=UTC`, a limit of 10 seconds and 256 KiB of output per stream.

It passes when the output matches `expected.txt` by the site's rules, within the limits. The session is typed into Python's interactive prompt line by line, as in the lesson, and what Python answers is compared with the answers recorded in the session (its `#   ` comment lines, collected into `expected.txt`): line by line, spaces at the end of a line and blank lines at the end do not count, and errors are compared with their traceback frames set aside. A pass here is a pass on the site.

---

[Open the lesson on LearnSome.tech](https://learnsome.tech/learn/python-course/m01l03) · [All labs of this lesson](../README.md) · [Course README](../../../README.md)
