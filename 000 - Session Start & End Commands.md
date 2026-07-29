- Execute in Powershell the 'CyberKD' directory.
# Start of Session (Pull)

  ```powershell
  git pull --rebase
  ```

# End of Session (Push)

  ```powershell
  notes-push
  ```

# To Create 'notes-push' Function

```powershell
notepad $PROFILE
```
- Paste the following into the Notepad document:
  ```powershell
  function notes-push {
	  git add -A
	  git commit -m "notes: $(Get-Date -Format yyyy-MM-dd)"
	  git push}
  ```

- Save and run:
```powershell
. $PROFILE
```
- Now, simply run 'notes-push' to update the Github repo.