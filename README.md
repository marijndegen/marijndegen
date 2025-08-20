- 👋 Hi, I’m @marijndegen
- 👀 I’m interested in gaming, coding, my friends, solving rubix cubes and parachuting.
- 🌱 I'm always interested to learn new stuff!
- 💞️ If you have any cool code I should check, let me know :D
- 📫 Reach me at marijndegen96@hotmail.com, view [my resume](http://marijndegen.nl)

**Note to self (and others) when recieving a new laptop**

Configure git aliasses (tested in powershell) 

1. Open with:

`code %USERPROFILE%\.gitconfig`

2. put this at the end of .gitconfig:

```
[alias]
	co = checkout
	br = branch
	ci = commit
	st = status
	check = "!sh -c 'dt=$(date +\"%Y-%m-%d %H:%M:%S\"); msg=\"$1\"; [ -z \"$msg\" ] && echo \"Error: No message provided for stash.\" >&2 && exit 1; git stash save -u \"at $dt $msg\" > /dev/null && git stash apply > /dev/null && git add -A > /dev/null && printf \"%0.s#\" {1..45} && echo && echo \"✔️   Game successfully saved! (Powered by github.com/marijndegen)\" && printf \"%0.s#\" {1..45} && echo && git status' -"
	sl = !git --no-pager stash list
	dm = diff -C HEAD^^ HEAD

	
```

Here for historical purposes:
```cmd
[alias]
  checknew = "!f() { date=\"\\$(date +'%Y-%m-%d %H:%M:%S')\"; message=\"\\$1\"; if [ -z \"\\$message\" ]; then echo 'Error: No message provided for stash.' >&2; exit 1; fi; git stash save -u \"at \\${date} \\${message}\" && git stash apply; }; f"
  checkOld = "!sh -c 'git stash save -u '\"$1\"' && git stash apply' #"
  checkNoMessageRequired2 = "!f() { date=\"$(date +'%Y-%m-%d %H:%M:%S')\"; message=\"$1\"; git stash save -u \"at ${date} ${message}\" && git stash apply; }; f"
```

```cmd
git config --global alias.checkOld2 "!sh -c 'git stash save -u '\"$1\"' && git stash apply' #"
git config --global alias.checkOld1 = "!sh -c 'git stash save -u '\"$1\"' && git stash apply' #"
git config --global alias.checkNoMessageRequired = "!f() { date=\"$(date +'%Y-%m-%d %H:%M:%S')\"; message=\"$1\"; git stash save -u \"at ${date} ${message}\" && git stash apply; }; f"
```

When using WSL2, put this in *.bashrc* to make sure windows git is used:

> alias git=git.exe

git config in `C:\Users\%USERNAME%\.gitconfig` should look like this:
```
[alias]
	co = checkout
	br = branch
	ci = commit
	st = status
	check = "!sh -c 'dt=$(date +\"%Y-%m-%d %H:%M:%S\"); msg=\"$1\"; [ -z \"$msg\" ] && echo \"Error: No message provided for stash.\" >&2 && exit 1; git stash save -u \"at $dt $msg\" > /dev/null && git stash apply > /dev/null && git add -A > /dev/null && printf \"%0.s#\" {1..45} && echo && echo \"✔️   Game successfully saved! (Powered by github.com/marijndegen)\" && printf \"%0.s#\" {1..45} && echo && git status' -"
	checkOld = "!sh -c 'git stash save -u '\"$1\"' && git stash apply' #"
	checkNoMessageRequired = "!f() { date=\"$(date +'%Y-%m-%d %H:%M:%S')\"; message=\"$1\"; git stash save -u \"at ${date} ${message}\" && git stash apply; }; f"
	sl = stash list
	checknew = "!f() { date=\"\\$(date +'%Y-%m-%d %H:%M:%S')\"; message=\"\\$1\"; if [ -z \"\\$message\" ]; then echo 'Error: No message provided for stash.' >&2; exit 1; fi; git stash save -u \"at \\${date} \\${message}\" && git stash apply; }; f"
	dm = diff --cached --find-renames

```

To make a tag in Git in cmd locally and push it to server:
> git tag vX.Y.Z -m 'short PR description' && git push origin vX.Y.Z

<!---
marijndegen/marijndegen is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
