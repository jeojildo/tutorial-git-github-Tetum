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
