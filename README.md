# On GitHub
* create new repository ```test_repo```

# On local machine
* configure ssh access for github
* set up ```test_repo```

```bash
git remote add origin git@github.com:kleinee/test_repo
mkdir test_repo
cd test_repo
touch README.md
git add .
git commit -m"initial commit"
git push -u origin master
```
