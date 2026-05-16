# Tutorial Git no Github iha Lian Tetum (on Arch Linux)

Git : Plataforma version control system (VCS) hodi halo mudansa ba file iha projetu ruma.
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
`` `


Git nudar plataforma VCS hodi halo mudansa ba ficheiro projetu ruma.

## 2. Halo installasaun ba Git
Atu bele detallu haree iha website official Git ninian

## 3. Konfigura Git

```bash
git config --global user.name "ita nia naran"
git config --global user.email "email@example.com" 

```

## 4. Continua ho etapa seluk
### 4.1 Upload...---

## 5. Loke terminal iha arch linux no hakerek code tuir mai
```bash
git init -b main
```
## 6. Pois hakerek code tuir mai atu hatudu file ida ne'ebe ita halo ona mudansa ou altera ruma
```bash
git status
```

## 7. 