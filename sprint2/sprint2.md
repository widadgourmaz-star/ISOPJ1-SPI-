

--<img width="598" height="22" alt="image" src="https://github.com/user-attachments/assets/a1895f09-8638-4652-a1b4-c152576d001b" />


<img width="1024" height="1024" alt="image" src="https://github.com/user-attachments/assets/bf95d2ad-1890-425d-b03d-b1a90e11aad8" />

<h1 style="color: pink;"> Sistemes de fitxers i particions </h1>
### Mida sector

El sector és la unitat física mínima del disc on es guarden dades. 
Mida Antiga (Obsoleta): 512 bytes.
Mida Moderna (Estàndard): 4096 bytes (4 KB), coneguda com a Advanced Format.


<img width="823" height="488" alt="image" src="https://github.com/user-attachments/assets/39a7bc4a-f293-4ebb-ac02-d8fa5ef3dbc9" />

### Mida block
El bloc és la unitat lògica mínima que utilitza el sistema de fitxers per guardar dades. Normalment un bloc ocupa 4096 bytes,

<img width="608" height="389" alt="image" src="https://github.com/user-attachments/assets/022fe613-398b-4af0-9442-782412c6e598" />

### Fragmentació interna 
Passa quan un fitxer no omple completament un bloc.Exctament quan L’espai queda desaprofitat.
### Fragmentació externaLa 
fragmentació externa es produeix quan un fitxer queda dividit en diferents parts dins del disc. Això passa quan no hi ha prou espai continu per desar-lo sencer.

### Tipus de formateig

#### baix nivell
crea els sectors físics i elimina totes les dades del disc.

#### mig nivell
esborra el sistema de fitxers i prepara els sectors per tornar-los a utilitzar. 

#### El d’alt nivell
crea un sistema de fitxers nou, i només esborra l’estructura, no les dades reals.

### Gesió de particions
Una partició és un tros lògic del disc físic on es pot instal·lar un sistema de fitxers. Permet tenir diferents sistemes operatius o organitzar millor les dades. Es pot gestionar amb eines com GParted, fdisk o parted.
#### Comandes:
Amb la comanda "fdisk -l" podem veure l'espai.

<img width="608" height="389" alt="image" src="https://github.com/user-attachments/assets/d3838397-2adf-47f9-8394-8eb7aedf911f" />

#### Gparted
GParted és una eina gràfica per gestionar particions en discs durs. Permet crear, esborrar, redimensionar, moure o formatar particions de manera segura i visual.

<img width="835" height="536" alt="image" src="https://github.com/user-attachments/assets/3c228c26-4a44-4ff0-969b-24bf6593f5ce" />

Podem realitzr-ho amb la comanada "fdisk"

<img width="835" height="536" alt="image" src="https://github.com/user-attachments/assets/f6a8e2b2-ce85-464b-a130-7e91d9697763" />

-Despres creem la particio.

<img width="600" height="392" alt="image" src="https://github.com/user-attachments/assets/846a8919-4d81-40c9-953c-fb87c8b93d93" />

Esta creat correctament. 

<img width="835" height="536" alt="image" src="https://github.com/user-attachments/assets/a6a80d82-58ce-4944-89b3-2251cc1645dc" />

-Amb la comanda "mkfs.ext4" podem canviar la mida del bloc

<img width="835" height="536" alt="image" src="https://github.com/user-attachments/assets/03601290-7413-42aa-94ab-5c2c843c3b7a" />

Amb "mkfs.ntfs" per reconeixer-ho windows 

<img width="835" height="536" alt="image" src="https://github.com/user-attachments/assets/b2df858b-8a2b-4b69-b286-4da207c8ce09" />

I al final vam entrar a GPARTED 

<img width="835" height="536" alt="image" src="https://github.com/user-attachments/assets/905dbf0c-aec6-4019-920c-537d33ab2bcc" />

### Muntatge
primer començem creant una carpeta a la ruta /mnt

<img width="835" height="536" alt="image" src="https://github.com/user-attachments/assets/90421a4e-5060-41dd-b3e9-6e12833375e7" />

Primer, utilitzem la comanda mount -t ext4 /dev/sdb1 /mnt/particio1 per muntar el disc temporalment; un cop fet, hi afegim un fitxer nou.

<img width="835" height="536" alt="image" src="https://github.com/user-attachments/assets/33989c77-8408-4673-8f49-a580e30cb641" />

<img width="835" height="536" alt="image" src="https://github.com/user-attachments/assets/d3f1a466-6916-476e-82a3-00bfbb4a9e7e" />

## Gestió de processos
és la funció del sistema operatiu que controla tots els programes que s’estan executant, ja siguin visibles per l’usuari o interns del sistema. Un procés és un programa en execució, i el sistema operatiu s'encarrega de crear-lo, administrar-lo, assignar-li recursos com la memòria o el temps de CPU i finalment tancar-lo. La gestió de processos permet supervisar l’activitat del sistema, detectar errors, aturar programes que no responen i garantir que les aplicacions i serveis essencials funcionin de manera correcta i eficient. En sistemes com Linux o Windows, aquesta gestió inclou controlar serveis del sistema, processos en segon pla i processos iniciats pels usuaris.
## Les eines bàsiques de gestió
és una part essencial de l’administració d’un sistema operatiu, ja que permet controlar qui pot accedir al sistema i què pot fer. Cada usuari disposa d’un compte propi amb credencials i permisos associats, i els grups serveixen per agrupar usuaris que comparteixen funcions o necessitats similars. Aquesta gestió inclou crear i eliminar comptes, modificar contrasenyes, assignar usuaris a grups i definir quines accions poden dur a terme dins del sistema. Tant en Windows com en Linux existeixen eines específiques per fer aquesta administració, com User Management en Windows o les ordres useradd, usermod i groupadd en Linux.

## Gestió d’usuaris i grups i permisos 

### Tipus d'Usuaris 
Els tipus d’usuaris varien segons el nivell d’accés. Normalment existeixen els usuaris normals, que poden utilitzar el sistema però no fer canvis crítics; els usuaris avançats, amb alguns privilegis addicionals; i els administradors, que tenen control total sobre el sistema i poden instal·lar programari, modificar configuracions o accedir a qualsevol fitxer. En Linux, l’usuari amb control absolut és l’usuari root, mentre que en Windows és l’usuari Administrator o els membres del grup Administrators.
### Fitxers importants 
Quant als fitxers importants, en Linux hi ha directoris essencials com /etc, que conté els fitxers de configuració del sistema i dels serveis; /home, on es guarden els fitxers personals de cada usuari; i /var, que emmagatzema dades variables com registres, bústies de correu o fitxers temporals. En Windows, les carpetes essencials inclouen C:\Windows, que conté els fitxers del sistema operatiu; C:\Program Files, on s’instal·la la major part del programari; i Users, que guarda els perfils i documents dels usuaris. Aquests fitxers i directoris són fonamentals per al funcionament correcte del sistema i la seva gestió adequada és vital per a la seguretat i estabilitat del mateix.
   
   En la comanda /etc/passwd cada linia presenta un usauari 
   
<img width="778" height="517" alt="image" src="https://github.com/user-attachments/assets/c5db5876-1ebf-4f45-afcb-8201f2b8c847" />

El fitxer de configuració d'usuaris utilitza una estructura de set camps diferenciats per cada línia, on els dos punts (:) actuen com a separadors entre cada dada:

1.Identificador (nom_usuari): És l'etiqueta única que el sistema utilitza per reconèixer cada compte, com root o daemon. És el nom que escrivim per fer el login.

2.Referència de la contrasenya (x): Normalment hi trobem una x, que indica que la clau no és visible aquí sinó que està xifrada al fitxer /etc/shadow. Si el camp mostra un asterisc (*) o una exclamació (!), significa que el compte no pot entrar al sistema.

3.Codi d'usuari (UID): És el valor numèric que el sistema assigna a cada perfil. Per exemple, el número 0 sempre identifica l'administrador principal o root.

4.Codi de grup (GID): El número que vincula l'usuari amb el seu grup de treball principal dins del sistema.

5.Informació addicional (GECOS): Un espai dedicat a descripcions extres, com el nom real de la persona o el seu departament.

6.Ruta d'inici (directori_home): Defineix la ubicació de la carpeta personal on l'usuari té els seus documents (per al root sol ser /root).

7.Terminal de treball (shell): Especifica quin programa de comandes s'inicia per defecte. Si apareix nologin o false, el compte està restringit i no pot obrir una sessió interactiva.

    El fitxer /etc/shadow conté les contrasenyes xifrades dels usuaris i informació relacionada amb la seguretat dels comptes. Només l’usuari root pot llegir-lo, perquè és un fitxer crític per a la seguretat del sistema.
    
<img width="604" height="530" alt="image" src="https://github.com/user-attachments/assets/8ca47003-53f7-4054-a3f8-3bd7d4440fa2" />

/etc/group:
Aquest fitxer és fonamental per entendre la gestió d’usuaris i permisos, ja que els grups permeten organitzar els accessos als fitxers i serveis del sistema d’una manera més flexible i segura.

<img width="604" height="530" alt="image" src="https://github.com/user-attachments/assets/fc7db2ce-c492-48bf-a26e-50df90eb67e8" />

  /etc/geshadow 
  Conté la informació segura dels grups , cada linia 
  
<img width="604" height="530" alt="image" src="https://github.com/user-attachments/assets/9b38d1c9-2cf8-41a3-9fb7-69e51030cf52" />

### comandes bàsiques 
#### adduser 

<img width="604" height="530" alt="image" src="https://github.com/user-attachments/assets/cf48ffcd-e8e2-4d66-add5-f2380057490d" />

#### Userdel 
He eliminat el usuari.

<img width="692" height="143" alt="image" src="https://github.com/user-attachments/assets/0887e205-70f6-4031-9723-65f1e0de05dc" />
<img width="818" height="560" alt="image" src="https://github.com/user-attachments/assets/aa0143a3-36e1-4c5f-88da-8b01dd2ae403" />
  
  Aqui he bloquijat la contrasenya del'usuari i tambe he ficat Usermod -U per desbloquijar ho 
  
<img width="818" height="374" alt="image" src="https://github.com/user-attachments/assets/2573d74b-b6f7-460d-a04f-3bd4d75e2863" />

### Els permisos
són els drets que determinen què pot fer un usuari o grup amb un fitxer o directori. En sistemes Unix/Linux, cada fitxer té tres tipus de permisos principals (lectura, escriptura i execució) i aquests es poden assignar al propietari, al grup i als altres usuaris del sistema. Això garanteix la seguretat i evita que persones no autoritzades modifiquin fitxers importants o executin programes de manera indeguda. En Windows, els permisos funcionen mitjançant llistes de control d’accés (ACL), que permeten definir permisos més detallats per a cada usuari o grup.

<img width="550" height="243" alt="image" src="https://github.com/user-attachments/assets/9347fb71-705d-4c22-9be7-10290e421ce0" />

Significat:
r = read (llegir)
w = write (escriure)
x = execute (executar)

<img width="580" height="131" alt="image" src="https://github.com/user-attachments/assets/c30c79fb-21e1-4b55-a53d-2a6d0b1791db" />

Podem mirar la jerarquia dels permisos

<img width="557" height="114" alt="image" src="https://github.com/user-attachments/assets/6b937e9b-359d-4e96-8f8c-38e9f8461613" />

1- He utilitzat la comanda adduser cire paloma per crear l'usuari cire i, al mateix temps, vincular-lo al grup paloma.
2-Per protegir la carpeta i definir qui pot accedir-hi, he configurat els permisos amb la comanda chmod 750 palomes/. Amb aquesta configuració he establert el següent:
7 (Propietari): Jo, com a administrador o propietari, tinc control total (llegir, escriure i executar).
5 (Grup): Els membres del grup paloma (com l'usuari cire) poden veure els fitxers i entrar a la carpeta, però n
Finalment, he tornat a executar ls -l | grep palomes per comprovar que els canvis s'havien aplicat. He pogut observar que la carpeta ja apareixia amb la data de creació i els permisos actualitzats correctament al directori /var.o poden esborrar ni modificar res.

 <img width="646" height="171" alt="image" src="https://github.com/user-attachments/assets/e278c3ef-4d32-42e3-be24-f2f06c3d7534" />




## Copies de seguretat i automatització de tasques 
Les còpies de seguretat serveixen per protegir les dades davant errors o pèrdues. Es poden fer manualment amb comandes com cp, tar, rsync, o programar-les automàticament amb cron. Automatitzar tasques assegura que es repeteixin regularment sense intervenció humana.
## Quotes d`usuari
Les quotes d’usuari limiten l’espai de disc que pot utilitzar cada usuari. Això evita que un sol usuari ocupi tot l’espai disponible. Es configuren amb eines com edquota, quotaon i repquota dins de sistemes de fitxers compatibles.



