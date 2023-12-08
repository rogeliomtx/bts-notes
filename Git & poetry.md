
## General dependencies

**Install pipx**
```sh
# mac only
brew install pipx
pipx ensurepath
```

Other installations:
https://pipx.pypa.io/stable/installation/

**Install poetry**
```sh
pipx install poetry
```

## Github

**Download the repository**
```sh
git clone {your-repository}
```

In case you have 2FA activated or using HTTPS git clone, you must create a personal token
https://github.com/settings/tokens?type=beta

![[Screenshot 2023-12-04 at 10.11.10 a.m..png]]

### Key commands
**cheat sheet**
https://about.gitlab.com/images/press/git-cheat-sheet.pdf

**git pull** https://git-scm.com/docs/git-pull
Pull updates from remote brach.
```sh
git pull
```

**git add** https://git-scm.com/docs/git-add
Add update to your local brach.
```sh
# git add .
git add {directory|file}
```

**git commit** https://git-scm.com/docs/git-commit
Commit an update to your local brach.
```sh
# git commit -m "ref(general): Update endpoints"
git commit -m "{message}"
```

**git push** https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository
Push your commit to a remote brach.
```sh
# git push origin main
git push REMOTE-NAME BRANCH-NAME
```

**git status** https://git-scm.com/docs/git-status
Check local brach status.
```sh
git status
```

**check git local user config** https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration
```sh
git config user.email
```

```sh
git config user.name
```

**update local user config** https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration
```sh
git config user.email "la_maquina_mas_veloz_de_tote_italie@bts.tech"
```

```sh
git config user.name "Francesco Virgolini"
```

**configure local (global) user** https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration
In case you want to set an user configuration globally (for all your git repositories).
Good option if you only use git for BTS. Bad idea if you work with different projects.

```sh
git config --global user.email "la_maquina_mas_veloz_de_tote_italie@bts.tech"
```

```sh
git config --global user.name "Francesco Virgolini"
```

## In the repository

**Install the repository dependencies**
```
poetry install
```

**Activate the virtual environment**
```sh
poetry shell
```

**Exit the virtual environment**
```sh
exit
```

**Run Fast API in development mode (with hot reload)**
```
poetry shell

cd bdi_api
uvicorn app:app --reload
```

**Run Fast API prod (probably)**
```
poetry shell

cd bdi_api
python bdi_api/app.py
```
