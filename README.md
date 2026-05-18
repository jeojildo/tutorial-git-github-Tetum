# Tutorial Git no Github iha Lian Tetum (on Arch Linux)

Git : Plataforma version control system (VCS) hodi halo mudansa ba file iha projetu ruma. <br>
Github: Plataforma ida ne'ebe developer sira utiliza hodi rai (save), manega no fahe codigo programasaun.

## 1. Update system operativu lai ho komandu tuir mai:
```bash
sudo pacman -Syu
```

## 2. Instal Git ho komandu tuir mai:
```bash
sudo pacman -S git
```

## 2. Haree fali hodi garante katak Git instala duni ona iha ita nia makina:
```bash
git --version
```
no se susesu instala duni ona, sei mosu mensajen tuir mai:
```bash
git version 2.54.0
```
Ezemplu iha hau nia makina:
```bash
[jeojildo@archlinux ~]$ git --version
git version 2.54.0
```

## 3. Konfigura Git
Tau naran ho komandu turi mai:
```bash
git config --global user.name "Hakerek naran"
```
Tau e-mail ho e-mail ne'ebe uza hodi rejistu ba Github ho komandu tuir mai:
```bash
git config --global user.email "email@emailezemplo.com"
```
Hare'e fali katak susesu:
```bash
git config --list
```
Ezemplu hanesan tuir mai:
```bash
[jeojildo@archlinux ~]$ git config list
user.email=pereirajeojildo0717@gmail.com
user.name=jeojildo
```

## 4. Generate SSH Key
ls: hamosu konteudo folder (list files/directories)

Loke terminal pois hakerek komandu tuir mai: 
```bash 
ls ~/.ssh
```

Kria SSH Key:
```bash
ssh-keygen -t ed25519 -C "email@emailezemplo.com"
```
ka ezemplu hanesan:
```bash 
ssh-keygen -t ed25519 -C "pereirajeojildo0717@gmail.com"
```

Depois hanehan enter dala hirak nune'e pois halao (ka halo ativu) ssh-agent hanesan tuir mai:
```bash
eval "S(ssh-agent -s)"
```
Aumenta key hanesan:
```bash
ssh-add ~/.ssh/id_ed25519
```
Depois copy public key ho komandu:
```bash
cat ~/.ssh/id_ed25519.pub
```

## 5. Aumenta SSH key ba Github
Loke Github SSH Setting no click iha New SSH Key pois paste key ohin copy ne'e no Save.
Loke terminal pois hakerek komandu:
```bash
ssh -T git@github.com(mosu mensagen)
```
Ezemplu hanesan tuir mai:
```bash
[jeojildo@archlinux tutorial-git-github-Tetum]$ ssh -T git@github.com
Hi jeojildo! You've successfully authenticated, but GitHub does not provide shell access.
```
## 6. Kria Repository iha Github
```bash
mkdir tutorial-git-github-Tetum
cd tutorial-git-github-Tetum
```
Loke folder tutorial-git-github-Tetum liu husi terminal ho komandu:
```bash
cd tutorial-git-github-Tetum
```
Ezemplu hanesan komandu tuir mai: (code . : hodi edit file nia konteudu iha Visual Studio Code)
```bash
[jeojildo@archlinux Estudagithub]$ cd tutorial-git-github-Tetum/
[jeojildo@archlinux tutorial-git-github-Tetum]$ code .
```
VS code sei mosu, tuir mai kria file ho extensaun .md ho naran README.md ho hakerek komandu tuir mai:
```bash
# # Tutorial Git no Github iha Lian Tetum (on Arch Linux)
```
no bele kontinua tutorial ho linguajen markdown too kompletu.

## 7. Halo repository ho naran ne'ebe hanesan iha iha Github:
Repository name: tutorial-git-github-Tetum (ho naran ne'ebe hanesan ho makina local)


## 8. Connect ba Github
Kria repository name (depende), ezemplu:
tutorial-git-github-Tetum depois hakerek komandu:
```bash
git remote add origin git@github.com:jeojildo/tutorial-git-github-Tetum.git
```

## 9. Halo commit
Connect ona ho github, tuir mai halo commit:

```bash
git status
```
Aumenta file:
```bash
git add . 
```
Ka bele hakerek file nia naran hanesan:
```bash
git add README.md
```
Halo commit:
```bash 
git commit -m "Initial commit"
```
Depois push ba Github: 
```bash
git push origin main
```
Ezemplu hanesan tuir mai ne'e:
```bash
[jeojildo@archlinux tutorial-git-github-Tetum]$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
[jeojildo@archlinux tutorial-git-github-Tetum]$ git add README.md 
[jeojildo@archlinux tutorial-git-github-Tetum]$ git commit -m "update"
[main 3254c2f] update
 1 file changed, 38 insertions(+), 4 deletions(-)
[jeojildo@archlinux tutorial-git-github-Tetum]$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 640 bytes | 320.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:jeojildo/tutorial-git-github-Tetum.git
   c75e51a..3254c2f  main -> main
[jeojildo@archlinux tutorial-git-github-Tetum]$ 
```
Ka habadak komandu hanesan tuir mai ne'e:
```bash
git status
git add README.md
git commit -m "Initial commit"
git push origin main
```
Se susesu entaun file refere sei mosu iha Github

## 10 Git pull
```bash
git clone git@github.com:username/naran-repository.git
```

## 11. Ezemplu



