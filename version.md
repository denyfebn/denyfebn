#### Versioning Rules v4.0

- **If Alpha**  
  `Major.Quarter.Minor.Patch`

- **If Fixed, Beta, Pre-release**  
  `Major.Quarter.Minor.Patch-conditional`

**Rules:**

Major starts two digits year and only changes if it has stable/alpha version, even if the year has changed, the version still considers changed by a lot of updates.  
Quarter starts 0 and ends at 3. It depends on the quarter but when the major is still the same and the quarter has a different year, then it’s stuck at 3.  
Minor starts at 0 and will be reset to 0 if Major updates.  
Patch starts at 0000. Patch also resets if the major updates. It doesn’t care about quarter; even if the quarter changes, patch still considers the minor version.

**Patch:**  
0000

First digit is main patch. If it has double digit it will be `10`, and the last three digits is the number of patch itself. Patch only updates by fixing the code without releasing anything. Max patch = 999.

**-conditional**  
It considers patch version. If it's already fixed/beta/pre-release, then add `-beta`, like:

- `0.3.0012-beta`
- `21.1.1.0015-pre-release`

**Example:**

- **Alpha:**  
  `25.1.10.12003` → Major 2025, Quarter 1, Minor 10, Patch 12, Patch version 003

- **Beta:**  
  `25.3.10.15015-beta` → Major 2025, Quarter 3, Minor 10, Patch 15, Patch version 015

- **Alpha:**  
  `26.2.0.0002` → Major 2026, Quarter 2, Minor 0, Patch 0, version 002

- **Beta:**  
  `26.3.1.0004-fixed` → Major 2026, Quarter 3, Minor 1, Patch 0, version 004
