- 👋 Hi, I’m @marijndegen
- 👀 I’m interested in gaming, coding, my friends, solving rubix cubes and parachuting.
- 🌱 I currently did a research project with deeplearning (AI), also diving deeper into advanced web programming with C#. 
- 💞️ If you have any cool code I should check, let me know :D
- 📫 Reach me at marijndegen96@hotmail.com, view [my resume](http://marijndegen.nl)

**Note to self (and others) when recieving a new laptop**

Configure git aliasses (in windows cmd):

```cmd
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.check "!sh -c 'git stash save -u '\"$1\"' && git stash apply' #"
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
	check = "!sh -c 'git stash save -u '\"$1\"' && git stash apply' #"
```

<!---
marijndegen/marijndegen is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
