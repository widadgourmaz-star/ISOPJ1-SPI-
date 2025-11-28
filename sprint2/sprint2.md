---
layout: default
title: "Sprint 2: Instal·lació, Configuració de Programari de Base i Gestió de Fitxers"
---


<img width="1024" height="1024" alt="image" src="https://github.com/user-attachments/assets/bf95d2ad-1890-425d-b03d-b1a90e11aad8" />


## Sistemes de fitxers i particions
### Mida sector
El sector és la unitat física mínima del disc on es guarden dades. 
Mida Antiga (Obsoleta): 512 bytes.
Mida Moderna (Estàndard): 4096 bytes (4 KB), coneguda com a Advanced Format.
<img width="823" height="488" alt="image" src="https://github.com/user-attachments/assets/39a7bc4a-f293-4ebb-ac02-d8fa5ef3dbc9" />

### Mida block
El bloc és la unitat lògica mínima que utilitza el sistema de fitxers per guardar dades. Normalment un bloc ocupa 4096 bytes,


### Fragmentació interna 
Passa quan un fitxer no omple completament un bloc.Exctament quan L’espai queda desaprofitat.
### Fragmentació externaLa 
fragmentació externa es produeix quan un fitxer queda dividit en diferents parts dins del disc. Això passa quan no hi ha prou espai continu per desar-lo sencer.
### Tipus de formateig
#### baix nivell: crea els sectors físics i elimina totes les dades del disc.

#### mig nivell: esborra el sistema de fitxers i prepara els sectors per tornar-los a utilitzar. 

#### El d’alt nivell: crea un sistema de fitxers nou, i només esborra l’estructura, no les dades reals.
### Gesió de particions
Una partició és un tros lògic del disc físic on es pot instal·lar un sistema de fitxers. Permet tenir diferents sistemes operatius o organitzar millor les dades. Es pot gestionar amb eines com GParted, fdisk o parted.
#### Gparted
GParted és una eina gràfica per gestionar particions en discs durs. Permet crear, esborrar, redimensionar, moure o formatar particions de manera segura i visual.
#### Comandes
## Gestió de processos
La gestió de processos permet controlar tots els programes en execució al sistema. Amb comandes com ps, top, kill o htop podem veure quins processos estan actius, el seu consum de CPU i memòria, i aturar-los si cal. Això ajuda a mantenir el sistema estable i eficient
## Gestió d’usuaris i grups i permisos 
## Copies de seguretat i automatització de tasques 
Les còpies de seguretat serveixen per protegir les dades davant errors o pèrdues. Es poden fer manualment amb comandes com cp, tar, rsync, o programar-les automàticament amb cron. Automatitzar tasques assegura que es repeteixin regularment sense intervenció humana.
## Quotes d`usuari
Les quotes d’usuari limiten l’espai de disc que pot utilitzar cada usuari. Això evita que un sol usuari ocupi tot l’espai disponible. Es configuren amb eines com edquota, quotaon i repquota dins de sistemes de fitxers compatibles.


