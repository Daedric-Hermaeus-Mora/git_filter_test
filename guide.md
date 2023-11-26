- Install the utility: `brew install git-filter-repo`
- Go to your local copy of the repo
- Execute the following command `git filter-repo --invert-paths --path PATH-TO-YOUR-FILE-WITH-SENSITIVE-DATA`
- Add the file to the `.gitignore` ad commit it
```bash
$ echo "YOUR-FILE-WITH-SENSITIVE-DATA" >> .gitignore
$ git add .gitignore
$ git commit -m "Add YOUR-FILE-WITH-SENSITIVE-DATA to .gitignore"
```

- Push force `git push origin --force --all` && `git push origin --force --tags`
- Ask people with access to the repo to do a rebase of their open branches
