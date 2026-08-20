# 🤦‍♂️ Common Mistakes & Fixes

### 1. Wrong .vcd Waveform Filename
* **Error:** Error opening .vcd file: No such file or directory
* **Fix:** Read the console output right after `vvp`:
  `VCD info: dumpfile <name>.vcd opened for output.`
  Run `gtkwave <name>.vcd` with the exact printed name.

---

### 2. GTKWave Signals Show All Zeros
* **Issue:** All signals display 0 at startup.
* **Fix:** Left-click on the timeline between 30 ns and 60 ns to see computed data away from reset (0 ns).

---

### 3. Accidental git add . in Downloads Folder
* **Issue:** Git stages heavy binaries (.exe, .tar.gz, apikey.txt).
* **Fix:**
  git reset HEAD~1
  git add *.v README.md *.md

---

### 4. Git Push Rejected (fetch first)
* **Issue:** [rejected] main -> main (fetch first)
* **Fix:**
  git push origin main --force

---

### 5. Missing "Add file" Button on GitHub
* **Issue:** Cannot find upload or create file buttons.
* **Fix:** Click the repository title at the top left to return to the root folder.