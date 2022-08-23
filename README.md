# Find the commit in which a given file was added
```
git log --diff-filter=A -- <file name>
```
* **Documentation:**
```
--diff-filter=[(A|C|D|M|R|T|U|X|B)…​[*]]
```
>Select only files that are Added (A), Copied (C), Deleted (D), Modified (M), Renamed (R), have their type (i.e. regular file, symlink, submodule, …​) changed (T), are Unmerged (U), are Unknown (X), or have had their pairing Broken (B). Any combination of the filter characters (including none) can be used. When * (All-or-none) is added to the combination, all paths are selected if there is any file that matches other criteria in the comparison; if there is no file that matches other criteria, nothing is selected.

# List committed files
```
git show <commit_id> --name-only
```