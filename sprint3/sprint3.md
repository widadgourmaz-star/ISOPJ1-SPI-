### Administració de Dominis i Seguretat

<img width="1024" height="1024" alt="image" src="https://github.com/user-attachments/assets/2131e7d9-ca4a-4d85-ad58-6492063f7d78" />


### Configuració LDAP - Servidor
primer en servidor canviem el hostname

<img width="883" height="177" alt="image" src="https://github.com/user-attachments/assets/86d572f8-eab2-4393-b6ae-a1859f25d8ac" />

he instalat el paquet ldap-utils i slapd.

<img width="565" height="53" alt="image" src="https://github.com/user-attachments/assets/bef987f8-750c-4905-93b3-d1f2ed08d380" />


<img width="716" height="276" alt="image" src="https://github.com/user-attachments/assets/4c2463ac-66e3-4426-8e69-535812736232" />

He configurat la IP a estatica en el servidor, perque sempre hem de tenir la IP fixa

<img width="707" height="366" alt="image" src="https://github.com/user-attachments/assets/3a3fdf38-8e33-4750-ac93-5f55bc2038cf" />


<img width="585" height="459" alt="image" src="https://github.com/user-attachments/assets/f6035c64-5b36-4edb-acc9-9187f7fcedf6" />

### Creació i configuració servidors

despres passem a la gestió de la configuració

<img width="708" height="518" alt="image" src="https://github.com/user-attachments/assets/96f53db8-5f42-4c50-9c74-21e168f8676a" />


<img width="551" height="412" alt="image" src="https://github.com/user-attachments/assets/0bef92fa-66a4-4468-b32a-bae8edea0785" />


<img width="597" height="433" alt="image" src="https://github.com/user-attachments/assets/7fb16774-491d-431d-be52-6c4ae6b4da7b" />

li diem que no volem que s'esborri la base de dades

<img width="605" height="110" alt="image" src="https://github.com/user-attachments/assets/dee714e2-100d-45c1-b97b-95fecf97f66a" />

he modificat el ou.ldif

<img width="768" height="688" alt="image" src="https://github.com/user-attachments/assets/73447ee5-ab13-4ff4-b427-972f39ba6cfe" />

### Població i Verificació del Directori LDAP
#### servidor

primer intallem libnss-ldap libpam-ldap nscd -y i verifequem que s`hagi creat correctament


<img width="720" height="471" alt="image" src="https://github.com/user-attachments/assets/66dca740-1659-485b-a520-102d62472a66" />

<img width="669" height="411" alt="image" src="https://github.com/user-attachments/assets/87e4b8c8-a1ad-49e3-81b2-2bdd216a6b13" />

<img width="697" height="531" alt="image" src="https://github.com/user-attachments/assets/13254b0b-3b40-4a25-b3e7-2d94629af84e" />

<img width="698" height="497" alt="image" src="https://github.com/user-attachments/assets/1c7b9f27-3e06-4b55-9c01-e6c4031bf190" />

<img width="687" height="344" alt="image" src="https://github.com/user-attachments/assets/e0d4f4da-96aa-46cc-a0ff-6bc9857e456f" />

<img width="675" height="353" alt="image" src="https://github.com/user-attachments/assets/7c2c12e3-0044-4406-a778-0a9994d260ff" />

<img width="554" height="246" alt="image" src="https://github.com/user-attachments/assets/d580f430-9bf3-4654-a903-92d476a95ef9" />

<img width="668" height="316" alt="image" src="https://github.com/user-attachments/assets/a91fd8b1-ad47-4413-a6e0-5ebe6122347f" />

### Configuració de Clients i Proves d’Autenticació LDAP

Un cop el servidor ja està operatiu i amb les dades carregades, el següent pas és configurar el sistema d’autenticació perquè aquest mateix servidor —o altres equips clients— puguin identificar i validar els usuaris que es troben al directori LDAP.
Per fer aquesta integració amb els mecanismes d’autenticació del sistema (NSS i PAM), cal instal·lar els paquets corresponents: libnss-ldapd, libpam-ldapd i nscd. Aquests paquets permeten que el sistema consulti el servidor LDAP quan necessita informació d’usuaris o processos d’autenticació.

<img width="734" height="219" alt="image" src="https://github.com/user-attachments/assets/1352cb8b-45d6-4e49-b7f5-996c4b977ff4" />

<img width="708" height="386" alt="image" src="https://github.com/user-attachments/assets/8d7004e0-9d9c-418b-bd6a-8849aff65a3a" />

<img width="717" height="330" alt="image" src="https://github.com/user-attachments/assets/9e35484c-a2f6-41c2-a521-952750f4cd8d" />

<img width="707" height="279" alt="image" src="https://github.com/user-attachments/assets/b9a642e0-4859-4602-ac66-d968b70a65bb" />

<img width="704" height="314" alt="image" src="https://github.com/user-attachments/assets/b5297554-93b8-4569-80c0-c2343dad2f26" />

<img width="660" height="234" alt="image" src="https://github.com/user-attachments/assets/2f813cb6-546f-4c5b-8d0e-f5b9bf960d45" />

<img width="574" height="279" alt="image" src="https://github.com/user-attachments/assets/c77aa4fd-71db-4f3c-9995-8c9d32cdbde4" />

<img width="690" height="263" alt="image" src="https://github.com/user-attachments/assets/f0ee6e7c-bf40-4f5d-84bf-34d53625e3e6" />

<img width="704" height="425" alt="image" src="https://github.com/user-attachments/assets/c969db70-0177-4be8-8d65-a4964ed1a5ed" />

<img width="730" height="431" alt="image" src="https://github.com/user-attachments/assets/695c40b7-59b4-47ac-a300-989091fa69df" />

<img width="1000" height="441" alt="image" src="https://github.com/user-attachments/assets/d24b1dca-f7d8-43ac-ac5c-7363e35e40e7" />

<img width="995" height="441" alt="image" src="https://github.com/user-attachments/assets/8ee8089e-5a4e-4963-af20-95b59d76ab24" />

<img width="817" height="175" alt="image" src="https://github.com/user-attachments/assets/18496735-237d-44d8-8495-8f96de08dfdf" />

<img width="635" height="77" alt="image" src="https://github.com/user-attachments/assets/232965da-1f57-45fa-9e17-1c3604e4d837" />

<img width="336" height="63" alt="image" src="https://github.com/user-attachments/assets/faf27ef3-f27d-4a3d-8e93-7075255e2720" />

### Entorn Gràfic
Per a configurar LDAP en un entorn gràfic tenim moltes opcions com ara:

- phpldapadmin
- apache directory stdio
- jxplorer
- ldap account manager (LAM)
  ### Requeriments Prèvis

<img width="910" height="559" alt="image" src="https://github.com/user-attachments/assets/6cd336be-14f1-4bf2-9676-454647cc4938" />

<img width="899" height="146" alt="image" src="https://github.com/user-attachments/assets/77946ccb-6123-4ff8-b094-3fd0237bc794" />

<img width="1406" height="498" alt="image" src="https://github.com/user-attachments/assets/226aff1e-ca05-40d0-ba07-54587595068b" />

<img width="1452" height="899" alt="image" src="https://github.com/user-attachments/assets/b0c59b21-5515-4ba7-9bd0-dc81a6b4cce1" />

<img width="1219" height="644" alt="image" src="https://github.com/user-attachments/assets/d14d1a7e-1468-416f-b5e3-3fdade0558e4" />

<img width="1044" height="308" alt="image" src="https://github.com/user-attachments/assets/fa770edf-8ec7-4636-8ec7-ccad7bef39bb" />

<img width="600" height="372" alt="image" src="https://github.com/user-attachments/assets/61b46382-f638-408f-98eb-d593339ec5c1" />

<img width="1534" height="447" alt="image" src="https://github.com/user-attachments/assets/79ee1934-3d0e-47e7-b0d3-c0f3c77e4649" />

### creacio de una nova OU
Pprimer hem d'anar a "Tools" i "OU Editor".

<img width="1184" height="280" alt="image" src="https://github.com/user-attachments/assets/f37d7242-5139-4d35-90e5-6692836126da" />

<img width="1205" height="410" alt="image" src="https://github.com/user-attachments/assets/2321e264-bb3b-4d64-82e6-02062172f35d" />

ja tenim creada 

<img width="1091" height="293" alt="image" src="https://github.com/user-attachments/assets/470b3ffb-16a1-4a21-9106-98433096cd91" />

### creació d'un nou grup
per a crear un nou grup primer hem d'anar a "Accounts" i "Groups2.

<img width="1075" height="191" alt="image" src="https://github.com/user-attachments/assets/13d8352e-2182-41e6-a984-e565fb6cea00" />

<img width="1651" height="334" alt="image" src="https://github.com/user-attachments/assets/6bfc4d4b-cf34-4396-89aa-5d0193b09fc8" />

I aqui anirem a "New Group"

<img width="1651" height="334" alt="image" src="https://github.com/user-attachments/assets/2f35de6b-801c-4254-9eaf-adcba9ab9ded" />


<img width="1449" height="367" alt="image" src="https://github.com/user-attachments/assets/26ee6815-c080-4111-a54c-646064b41753" />


























### Configuració Samba
#### Què és Samba?

Samba és un programari lliure que permet compartir fitxers i recursos en una xarxa. Facilita la comunicació entre sistemes Linux i Windows, permetent que un servidor Linux actuï com un servidor de fitxers compatible amb Windows.

Samba permet gestionar usuaris, contrasenyes i permisos, i és molt utilitzat en entorns educatius i empresarials amb sistemes operatius mixtos.
primer instalem samba 

<img width="796" height="501" alt="image" src="https://github.com/user-attachments/assets/b66856cd-f7b0-4d38-a718-81645f888a24" />


Comprovem la instal·lació , i despres editem el fitxer de configuració /etc/samba/smb.conf per definir el grup de treball i els recursos compartits.

<img width="589" height="132" alt="image" src="https://github.com/user-attachments/assets/1c82f5e6-de91-4507-938f-5d52d9171305" />


<img width="596" height="355" alt="image" src="https://github.com/user-attachments/assets/e21b003d-d7ac-42cb-9761-7c5837d496c2" />

Definim la configuració global i els recursos compartits, assegurant els permisos adequats.

<img width="595" height="329" alt="image" src="https://github.com/user-attachments/assets/dce8e1fd-5720-4402-a84a-65ae4c74512d" />


<img width="596" height="326" alt="image" src="https://github.com/user-attachments/assets/2b24effd-8370-4685-958d-31b1b43e2ae7" />


<img width="600" height="409" alt="image" src="https://github.com/user-attachments/assets/619f52cf-2e51-46ee-84fe-411776ed4fb9" />


<img width="838" height="513" alt="image" src="https://github.com/user-attachments/assets/a480d13c-759a-4011-a223-455cddc17560" />


<img width="643" height="512" alt="image" src="https://github.com/user-attachments/assets/304098e7-c25a-4379-9c78-18583a9ed15f" />


<img width="851" height="469" alt="image" src="https://github.com/user-attachments/assets/6f1218f8-cd44-41de-b033-4d627e2d006d" />




