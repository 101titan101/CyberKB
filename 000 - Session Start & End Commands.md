# Start of Session (Pull)

- Navigate to CyberKB directory in Powershell
- ```powershell
  git pull --rebase
  ```

# End of Session (Push)

- Navigate to CyberKB directory in Powershell
- ```powershell
  function notes-push {
	  git add -A
	  git commit -m "notes: $(Get-Date -Format yyyy-MM-dd)"
	  git push}
  ```

# To Create 'notes-push' Function

- Open Powershell instance
```powershell
notepad $PROFILE
```
- Will open a new Notepad $PROFILE file which automatically runs when a new Powershell instance begins
- Import the following text:
function notes-push {
	git add -A
	git commit -m "notes: $(Get-Date -Format yyyy-MM-dd)"
	git push
}
- Saved and run to execute in the current session:
```powershell
. $PROFILE
```