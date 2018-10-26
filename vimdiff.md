# VimDiff

#### LOCAL | BASE | REMOTE | MERGED

- Local: Current branch file
- Base: Last commom ancestor
- Remote: File merging to current branch
- Merged: Resulting file

#### Selecting a version

- Move over to the top of the conflict in the MERGED file and type:

> ]c or [c              # To move between conflicts
> zR                    # To unfold any hidden code
> :diffg RE | BA | LO   # To get from REmote, BAse and LOcal respectively

#### Finishing

- Save and commit

> :wqa                  # Exit and save several files at once
> git commit -m "Solved conflict"
