

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

## Importància de les ACL a Ubuntu
 Les ACL a Ubuntu són importants perquè permeten controlar millor qui pot accedir als fitxers i carpetes.
Normalment, Ubuntu només permet definir permisos per a un usuari, un grup i la resta d’usuaris, cosa que és limitada. Amb les ACL pots donar permisos a diversos usuaris i grups diferents sobre el mateix recurs, sense haver de crear grups nous.
Això fa que la gestió dels permisos sigui més flexible, sobretot en sistemes amb molts usuaris, com servidors compartits o entorns d’empresa, on cada persona necessita accessos diferents.
A més, les ACL milloren la seguretat, perquè permeten aplicar el principi de mínim privilegi: cada usuari només té els permisos que realment necessita. També faciliten saber qui pot accedir a què, cosa molt útil per controlar i auditar els accessos.

<img width="727" height="222" alt="image" src="https://github.com/user-attachments/assets/6e4fe4a7-cb9c-49b0-a30c-b668d4f9e26b" />

<img width="727" height="222" alt="image" src="https://github.com/user-attachments/assets/b41694e5-c8e6-4294-880f-d9c31981e095" />

Primer, he hagut d'instal·lar les eines necessàries. Al principi la comanda setfacl no funcionava perquè no tenia el paquet acl, així que l'he instal·lat amb apt install.

Després, he preparat el fitxer de prova. He creat un fitxer anomenat numeros amb la comanda touch i li he donat permisos totals amb chmod 777 per comprovar que tothom hi tenia accés inicialment.

A continuació, he creat un usuari nou anomenat segon amb la comanda adduser per poder fer la prova de permisos.

El pas més important ha estat fer servir les ACL (Llistes de Control d'Accés). He fet servir la comanda setfacl -m user:segon:--- numeros. Amb això, he aconseguit que, encara que el fitxer sigui obert per a tothom, l'usuari 'segon' no hi pugui fer absolutament res.

Finalment, he passat la comanda getfacl numeros per ensenyar que la configuració s'ha guardat bé. Si et fixes a la pantalla, ara surt la línia user:segon:---, que confirma que aquest usuari no té permisos.
## Umask
umask (user mask) és un valor del sistema que s'utilitza per establir els permisos per defecte que tindran els fitxers i les carpetes quan els creïs de nou.

<img width="480" height="270" alt="image" src="https://github.com/user-attachments/assets/5c9cd503-fd7e-4166-ada6-da07550d93e7" />

En aquesta part, he practicat amb el umask. He canviat el valor per defecte a 0004 per bloquejar el permís de lectura als usuaris que no siguin propietaris ni del grup. Després, he creat una carpeta i un fitxer i he demostrat amb ls -l que el sistema els ha assignat permisos automàticament restant aquest '0004', deixant el grup d'altres usuaris sense capacitat de llegir el contingut

<img width="833" height="465" alt="image" src="https://github.com/user-attachments/assets/83910a89-a7e4-4b0d-b297-f06a3a219980" />

<img width="815" height="539" alt="image" src="https://github.com/user-attachments/assets/9a27628b-be27-4e03-ab0f-543eb888af6f" />

## Gestió de processos

Els processos són els programes que s’estan executant en un sistema en un moment determinat. Cada procés té un PID, que és un número que el identifica de manera única, i està associat a un usuari que n’és el propietari. A més, un procés pot trobar-se en diferents situacions, com ara executant-se, esperant recursos o aturat.
El sistema operatiu s’encarrega de gestionar tots aquests processos i de distribuir el temps de CPU entre ells perquè funcionin de manera eficient.
Per administrar els processos, disposem de diverses eines bàsiques:

-ps, top i htop permeten consultar quins processos estan actius i veure informació com l’ús de CPU o memòria.

-kill i pkill serveixen per finalitzar processos, ja sigui indicant el seu PID o el seu nom.

-nice i renice permeten modificar la prioritat d’execució d’un procés, donant-li més o menys preferència.

-systemctl i service s’utilitzen per gestionar serveis del sistema, tot i que no s’entrarà en detall en aquest apartat.
### Ús de pstree
-p
Mostra informació d’un procés concret, indicant el seu PID.
👉 Serveix quan vols veure només un procés específic.

-u
Mostra els processos d’un usuari determinat.
👉 Útil per saber quins programes està executant un usuari.

-h
Amaga la capçalera de la sortida.
👉 Va bé quan vols un resultat més net o per usar-lo en scripts.

-n
Ordena o mostra la informació utilitzant valors numèrics en lloc de noms (per exemple, UID en comptes de nom d’usuari).
👉 Facilita comparacions i ordenacions.

-a
Mostra tots els processos, inclosos els d’altres usuaris.
👉 Permet tenir una visió global del sistema.

<img width="787" height="531" alt="image" src="https://github.com/user-attachments/assets/08bc92e0-7855-4a16-9c62-881ca354406a" />

he provat en root tambe 

<img width="787" height="531" alt="image" src="https://github.com/user-attachments/assets/abc3c6ee-3dcc-44d9-ac39-6353f48c6b65" />

he provat la comanda -h per filtrar resultat 

<img width="809" height="432" alt="image" src="https://github.com/user-attachments/assets/84a44638-3cca-41a9-a7d9-222dffac2d11" />

La comanda ps aux s’utilitza per veure tots els processos actius al sistema, amb informació detallada sobre cada un. Explicat pas a pas:

ps → mostra processos.

a → inclou processos d’altres usuaris, no només els del teu compte.

u → mostra informació de l’usuari que és propietari del procés i detalls com l’ús de CPU i memòria.

x → mostra processos que no estan associats a cap terminal (com els serveis que s’executen en segon pla).

<img width="716" height="536" alt="image" src="https://github.com/user-attachments/assets/e63b1110-c805-4af0-bbf0-6dc72e404c7d" />

La comanda grep usuari s’utilitza per filtrar informació i mostrar només les línies que contenen la paraula “usuari” (o el nom real d’un usuari).

<img width="720" height="124" alt="image" src="https://github.com/user-attachments/assets/f2ed729d-d7af-4d08-b545-d796a35dd8bf" />

aqui vaig fer un example per matar un proces utilitzant la comanda kill 

<img width="709" height="257" alt="image" src="https://github.com/user-attachments/assets/0e8534f7-d9b1-418a-865d-a8b29dfe426f" />

i tenim tambe la comanda top serveix per monitoritzar en temps real els processos del sistema i veure com utilitzen els recursos.
Amb top pots:

Veure quins processos consumeixen més CPU i memòria.

Observar informació com PID, usuari propietari, estat del procés, temps d’execució i ús de recursos.

Ordenar processos segons l’ús de CPU, memòria o altres criteris.

Interactuar amb els processos, per exemple, aturar-los o canviar la seva prioritat mentre la comanda està en execució.

<img width="809" height="432" alt="image" src="https://github.com/user-attachments/assets/73443f1a-79d6-4659-bcad-129393da44f2" />

<img width="809" height="432" alt="image" src="https://github.com/user-attachments/assets/39fce04f-af11-48c3-9586-4469adef1201" />

Amb la comanda renice serveix per canviar la prioritat d’execució d’un procés ja en funcionament.

<img width="531" height="83" alt="image" src="https://github.com/user-attachments/assets/f3c7d70f-aa9e-4cea-906c-c653b273d7e9" />

## Còpies de seguretat i automatització de tasques
Còpies de seguretat

Una còpia de seguretat és una duplicació de les teves dades que serveix per recuperar informació si es perd, es trenca, hi ha un error humà, un virus o qualsevol altre problema. Les còpies s’han de guardar en un lloc separat de les dades originals, com un altre disc, un servidor o al núvol.

Normalment, les còpies de seguretat segueixen unes regles o polítiques:

Quant temps es conserven

Quantes versions es guarden

Proves de restauració per assegurar que les dades es poden recuperar
Tipus principals de còpia de seguretat

1. Còpia completa

Guarda totes les dades cada vegada que es fa.

És la més segura i fàcil de restaurar, però també la més lenta i que ocupa més espai.

Exemple: si fas còpia completa dilluns, dimarts i dimecres, només necessites la còpia de dimecres per recuperar un fitxer perdut dijous.

2. Còpia incremental

Guarda només els canvis fets des de l’última còpia, sigui completa o incremental.

És ràpida i ocupa poc espai, però per restaurar cal la còpia completa inicial i totes les incrementals posteriors.

Exemple: còpia completa dilluns, incremental dimarts i dimecres → per recuperar dijous, necessites la de dilluns + dimarts + dimecres.

3. Còpia diferencial

Guarda els canvis fets des de l’última còpia completa.

És més ràpida que la còpia completa i ocupa menys espai que repetir una completa cada dia.

Exemple: còpia completa dilluns, diferencial dimarts i dimecres → per recuperar dijous només necessites la còpia completa de dilluns i l’última diferencial (dimecres).
RAID i emmagatzematge

Els sistemes RAID combinen diversos discs per millorar rendiment i seguretat, depenent del tipus:

RAID 0: combina discs per més velocitat i capacitat, sense protecció. Si un falla, es perden totes les dades.

RAID 1: còpia mirall dels discs. Si un falla, l’altre segueix funcionant.

RAID 5/6: reparteix dades i paritat entre discs, equilibrant velocitat i seguretat.

RAID 10: combina velocitat del RAID 0 amb seguretat del RAID 1.

Imatge de disc

Una imatge de disc és una còpia exacta d’un disc o partició, incloent sistema operatiu, programes i dades.

Serveix per clonar equips o restaurar tot el sistema ràpidament.

Requereix molt espai i temps, però permet restaurar un ordinador complet molt fàcilment.

Snapshot

Un snapshot és una captura ràpida de l’estat del sistema o disc en un moment concret.

Guarda només els canvis a partir d’aquell moment, així és molt ràpid de crear.

Serveix per tornar enrere ràpidament o fer proves.

Resum

Còpia de seguretat: protegeix les dades guardant-les en un lloc segur.

Imatge de disc: copia tot el sistema exactament com està en un moment determinat.

Snapshot: permet tornar enrere ràpid, però no protegeix contra fallades del mateix disc.

Millor combinació: snapshots per recuperacions ràpides + còpies externes per desastres.

Eines per fer còpies

cp: còpia simple de fitxers localment. Molt fàcil, però no optimitza res.

rsync: còpia intel·ligent que només transfereix fitxers modificats. Pot ser local o remot via SSH.

dd: clona discs o particions sector a sector. Tot i que és complet, no és intel·ligent (copia tot encara que no hagi canviat).
### cp (Copy)

Funció: Copia fitxers o directoris d’una ubicació a una altra.

Característiques principals:

És molt senzilla d’utilitzar.

Només transfereix fitxers de manera directa, sense comprovar si han canviat o optimitzar l’operació.

És útil per fer copiats ràpids locals, però en projectes grans o amb molts fitxers no és eficient.

Exemples:

<img width="714" height="373" alt="image" src="https://github.com/user-attachments/assets/4e6cbfee-9db1-4db5-815d-2900d4077b94" />

Avantatges:

Molt ràpid i fàcil de recordar.

No necessita configuració.

Desavantatges:

No detecta fitxers modificats, sempre copia tot.

No sincronitza directoris.

Només funciona localment (a menys d’utilitzar muntatges com NFS o Samba).

### rsync (Remote Sync)

Funció: Sincronitza fitxers i directoris intel·ligentment, transferint només els canvis.

Característiques principals:

Detecta fitxers nous, modificats o eliminats i només copia els necessaris.

Pot fer còpies locals o remotes via SSH.

Permet compressió, preservació de permisos, propietari, dates i enllaços simbòlics.


Exemples:

<img width="718" height="332" alt="image" src="https://github.com/user-attachments/assets/7558dcbb-6084-441e-9cfc-59c743af5ae5" />


Molt eficient en transferència de dades grans.

Manté permisos, propietats i dates correctes.

Ideal per còpies de seguretat incrementals.

Desavantatges:

Més complex que cp per als principiants.

Requereix una mica més de temps per calcular què s’ha modificat (tot i que compensa en còpies grans).

### dd (Data Duplicator / Disk Dump)

Funció: Clona discs o particions sector a sector.

Característiques principals:

Copia tot exactament, incloent sistemes de fitxers, sectors buits i espais no utilitzats.

Molt útil per crear imatges completes de discs, clonar discs senceres o fer backups de baix nivell.

Exemples:

<img width="724" height="457" alt="image" src="https://github.com/user-attachments/assets/fe835e20-a88e-4790-8bbc-cb3d5230937a" />

<img width="724" height="457" alt="image" src="https://github.com/user-attachments/assets/73842ad8-6615-4699-9a66-c928897251cf" />

if= → input file (fitxer o dispositiu d’entrada)
of= → output file (fitxer o dispositiu de sortida)
bs= → block size, mida dels blocs que copia alhora

Avantatges:

Còpia exacta de tot, incloent sectors sense format.

Ideal per recuperacions forenses o migració de discs.

Desavantatges:

No és intel·ligent: sempre copia tot, encara que no hagi canviat res.

Requereix molt espai i temps.

Pot ser perillós si s’escriu sobre el dispositiu equivocat (pot esborrar dades).
## Quotes d`usuari
Les quotes d’usuari limiten l’espai de disc que pot utilitzar cada usuari. Això evita que un sol usuari ocupi tot l’espai disponible. Es configuren amb eines com edquota, quotaon i repquota dins de sistemes de fitxers compatibles.



