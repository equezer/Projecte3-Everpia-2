# T03: Gestió flexible de discos (LVM i Espais d’emmagatzematge)


---

Configuració Inicial:

afegim dos disc durs de 10 GB

<img width="955" height="542" alt="Tasca03_projecte3_01_01" src="https://github.com/user-attachments/assets/1060ca48-254f-4bd5-afbd-1935fb544b90" />


instal·lem fdisk per mirar quins discos tenim.

<img width="637" height="347" alt="Tasca03_projecte3_01_02" src="https://github.com/user-attachments/assets/d857056f-5b2f-4834-bd1f-9098e956015a" />


i els comprovarem amb la comanda sudo fdisk -l

<img width="482" height="486" alt="Tasca03_projecte3_01_03" src="https://github.com/user-attachments/assets/17f4df4e-4dcb-4a04-8294-c87f2e7aef52" />


Ara cal crear els volums físics amb la comanda pvcreate (physical volume create) a partir de les particions desitjades.

<img width="398" height="96" alt="Tasca03_projecte3_01_04" src="https://github.com/user-attachments/assets/89e780c0-1106-43d4-a4f3-3af6d092f79c" />

Posteriorment es poden agregar o eliminar volums.

<img width="529" height="34" alt="Tasca03_projecte3_01_05" src="https://github.com/user-attachments/assets/9d4a98d1-1c59-4cfa-84e2-c241e456a8e2" />


Es poden agregar nous volums afegint la totalitat del seu espai o només una part.

<img width="466" height="22" alt="Tasca03_projecte3_01_06" src="https://github.com/user-attachments/assets/922ea9ce-222c-4958-ae4a-24ad591e9422" />


Amb vgdisplay veiem les característiques del grup.

<img width="519" height="395" alt="Tasca03_projecte3_01_07" src="https://github.com/user-attachments/assets/b90486b8-cfc1-4b08-b4ba-c378d6d346cb" />


Els volums lògics es creen a partir del VG indicant la mida, el VG i el nom que se li vol donar.

<img width="516" height="35" alt="Tasca03_projecte3_01_08" src="https://github.com/user-attachments/assets/c3ee4372-2a50-4080-abeb-ac74a451c98d" />


Si s'escriu la comanda vgdisplay s'observa ara com ja marca l'espai com utilitzat.

<img width="532" height="383" alt="Tasca03_projecte3_01_09" src="https://github.com/user-attachments/assets/7a19a5ab-81a1-496d-ace2-04e18c57e72d" />


Els volums lògics (LV) són com les particions, per tant, per utilitzar-se caldrà formatar-los amb un sistema d'arxius.

<img width="512" height="227" alt="Tasca03_projecte3_01_10" src="https://github.com/user-attachments/assets/4ce50e83-8fa8-4752-ba25-1dea07af225b" />


Per poder utilitzar el volum lògic cal utilitzar la comanda mount per muntar el volum cap la cerpeta creada abans:

<img width="532" height="28" alt="Tasca03_projecte3_01_11" src="https://github.com/user-attachments/assets/eb18c3ea-42bf-4dae-bd88-5aea90049fdb" />


cal editar l'arxiu /etc/fstab

<img width="370" height="17" alt="Tasca03_projecte3_01_12" src="https://github.com/user-attachments/assets/f9f84b77-fc0c-4eb7-ba60-50030eae9d05" />


Al fer l'extensió la mida s'indica amb el paràmetre -L:

<img width="757" height="350" alt="Tasca03_projecte3_01_13" src="https://github.com/user-attachments/assets/d6faaee2-b176-4cff-8ab4-607280ece6a6" />

Ara cal ampliar el sistema de fitxers per poder aprofitar aquesta mida extra amb resize2fs
i comprovem amb df -h.

<img width="834" height="127" alt="Tasca03_projecte3_01_14" src="https://github.com/user-attachments/assets/0c2f57e8-cbf7-4256-bcb2-32c31a859995" />


Aquesta comanda mostra els volums físics creats indicant si estan assignats algun grup de volums.

<img width="666" height="130" alt="Tasca03_projecte3_01_15" src="https://github.com/user-attachments/assets/a169300f-0442-4d1d-bc24-0b6ba45bae9e" />

Aquest comanda serveix per veure els grups de volums existents i indicant el nombre de volums físics que el formen.

<img width="505" height="159" alt="Tasca03_projecte3_01_16" src="https://github.com/user-attachments/assets/99a47ebb-dcc8-4ec9-bad1-772fc9340ee9" />


Crearem alguns arxius al lv01

<img width="387" height="76" alt="Tasca03_projecte3_01_17" src="https://github.com/user-attachments/assets/9e2de7a7-7e72-47b9-a1b0-6d45e7694ec7" />

Ara crearem la instantània (snapshot):

<img width="351" height="58" alt="Tasca03_projecte3_01_18" src="https://github.com/user-attachments/assets/b13e14f1-4b62-4ac2-a514-832b1247f9c8" />


Podem veure els dos LV creats i com la còpia apunta al volum original:

<img width="409" height="108" alt="Tasca03_projecte3_01_19" src="https://github.com/user-attachments/assets/2a61e44a-a83c-4ec5-9707-d890a10aff19" />

Muntem la còpia per veure el contingut:

<img width="594" height="35" alt="Tasca03_projecte3_01_20" src="https://github.com/user-attachments/assets/4b63723f-dd2a-4941-bbef-d50151f16166" />

Per fer aquesta demo, esborrarem els volums lògics i el grup de volums creat prèviament:

<img width="731" height="76" alt="Tasca03_projecte3_01_21" src="https://github.com/user-attachments/assets/51f70de3-f46f-4448-94d1-240518bae10c" />


Creem un grup de volums amb dos dels volums físics:

<img width="505" height="78" alt="Tasca03_projecte3_01_22" src="https://github.com/user-attachments/assets/40b6bacb-5a1c-4bb5-aec5-bed57ae4a359" />

Ara crearem el sistema de mirall (mirror) simple:

<img width="519" height="24" alt="Tasca03_projecte3_01_25" src="https://github.com/user-attachments/assets/2bff4da3-1b47-41c0-8959-9580bc7141e0" />

