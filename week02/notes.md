Paridhi Garg Coding Cafe Assignment 1 L1P1

1. pwd printed /Users/paridhigarg, which is my home directory.

2. ls -a showed hidden files that plain ls doesn't, like .zshrc and .zsh_history. Any file starting with a . is hidden by convention, usually config or settings files.

3. The first column shows the file type and permissions. d means it's a directory, and the next nine characters (rwx r-x r-x) show read/write/execute permissions for the owner, group, and everyone else, in that order.

4. coding-cafe/week02 worked without cd because it's a relative path it doesn't start with /, so it's read relative to wherever I'm currently standing. It worked because I was in my home folder, which is exactly where coding-cafe lives.

5. mv did two jobs,first it moved README-backup.md into the week01/ folder and then it renamed it to old-readme.md.Whether mv moves or renames depends on whether the destination given is a folder or a new filename.

6.My $PATH has 14 folders, separated by :.The shell searches through them in order and stops at the first match it finds.

7. My python3 lives at /opt/anaconda3/bin/python3.

8. My answer was the same as the person next to me, both our python3 paths pointed to the same Anaconda install location, likely because we have similar setups.

9. zsh: command not found: pyton3. This happens because the shell searched every folder listed in $PATH, in order, looking for a program called pyton3.

10. .venv didn't show with plain ls because it starts with a dot, and dotfiles/folders are hidden from ls by default — only ls -a reveals them.

11. My prompt changed from (base) paridhigarg@... to (.venv) (base) paridhigarg@... — .venv appeared in front, showing it's now layered on top of the previously active conda base environment.

12. No, it's a different path — it changed from /opt/anaconda3/bin/python3 to /Users/paridhigarg/coding-cafe/.venv/bin/python3. This shows that activate doesn't just change the prompt cosmetically; it edits $PATH itself, putting .venv/bin at the very front so the shell finds it before anaconda's or the system's python.

13. The first pip list only had pip itself. The second had five new packages: requests and its dependencies (certifi, charset-normalizer, idna, urllib3) — all installed only inside this venv, without touching the system or conda Python.

14. After running deactivate, which python3 pointed back to /opt/anaconda3/bin/python3 — same as before venv was ever activated. deactivate removed .venv/bin from the front of $PATH, so the shell falls back to finding conda's python first again.

15. ls -h, when combined with -l, makes file sizes human-readable — instead of raw byte counts, it shows sizes with unit suffixes like K, M, G, rounded to keep the numbers short and easy to read.

16. Ctrl+C sent a keyboard interrupt, shown by the KeyboardInterrupt message — it stopped whatever was running but kept me inside the Python shell. Ctrl+D, on the other hand, signaled that there was no more input coming, which caused Python to exit the interactive shell entirely and return me to my normal terminal prompt.
