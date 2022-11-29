## GitHub

### Multiple Github Accounts

```
vim ~/.ssh/config

Host github.com-office
    HostName github.com
    IdentityFile ~/.ssh/id_rsa.github_office

Host github.com-personal
    HostName github.com
    IdentityFile ~/.ssh/id_rsa.github_personal

Host * !github.com-company !github.com-personal
    ...
```

```
vim ~/.gitconfig

...

[includeIf "hasconfig:remote.*.url:git@github.com-office:**/**"]
    path = ~/.gitconfig.github_office
    
[includeIf "hasconfig:remote.*.url:git@github.com-personal:**/**"]
    path = ~/.gitconfig.github_personal
```

```
vim ~/.gitconfig.github_office

[user]
    email = office@example.com
    name = office
```

```
git clone git@github.com-office:organization/repository.git
```
