## Script to create .gitkeep recursively
```
find . -type d -empty -not -path "./.git/*" -exec touch {}/.gitkeep \;
```
