# T01: Gestor de contrasenyes

## Alerta!!

**EverPia ha estat atacada per ciberdelinqüents.**  
La consultora on esteu de becaris ha patit una **fuita d’informació (data breach)** i **informació confidencial sobre un projecte que està en fase de desenvolupament** està ara en mans de delinqüents que **amenacen amb publicar-la si no es paga un rescat**.

Òbviament, això ha causat una **gran alarma dins la companyia** i s’ha creat un **comitè de crisi** per gestionar la situació.  

La investigació interna ha revelat que un dels **comptes tècnics** va ser compromès a causa de **l'ús d'una contrasenya feble o reutilitzada.**

---

Com a resposta a aquesta crisi, la **Direcció Tècnica** ha emès una directriu:  
Tot el personal tècnic ha de començar a utilitzar un **gestor de contrasenyes validat** per garantir l'ús de **credencials úniques i robustes**.  

Se us encarrega la tasca d'**avaluar les opcions** i **crear la documentació necessària per a la formació del personal.**

# Fase 1: Anàlisi i Justificació (Document d'Informe)

Heu de redactar un **informe** que justifiqui tècnicament la decisió de la Direcció i comparin les opcions.  
Aquest informe ha d'incloure:

---

## 🧩 Introducció i Justificació

Explicació de **per què les contrasenyes febles o reutilitzades són un risc crític** per a l'empresa  
  (exemples: **atac de diccionari**, **credential stuffing**, etc.).  
La **funció crucial d'un gestor de contrasenyes** per mitigar aquests riscos.

---

## ⚙️ Comparativa Tècnica

Realitzeu una **taula comparativa detallada** entre:

### 🔹 Bitwarden (Alternativa Online / Núvol)
Analitzeu:
La **sincronització**  
El **model de seguretat** (xifratge end-to-end)  
La **facilitat d'accés** des de múltiples dispositius  
El **cost / model freemium**

### 🔹 KeePassX / KeePassXC (Alternativa Offline / Escriptori)
Analitzeu:
L'**emmagatzematge local** de l'arxiu (KDBX)  
La **independència del núvol**  
El **model open source**  
La **portabilitat de l'arxiu**

---

## ⚖️ Avantatges i Inconvenients

Resumiu els principals **pros i contres** de cada model (**online vs. offline**) des del punt de vista de:
**Seguretat**
**Usabilitat**
**Continuïtat del negoci**

---

## ✅ Recomanació

Concloeu l'informe **escollint l'eina més adequada** per al **personal tècnic de l'empresa**  
i **justifiqueu la vostra elecció** amb criteris tècnics i operatius.


# Fase 2: Guia d'Ús Tècnica (Manual Operatiu)

Utilitzant l'eina que heu seleccionat a la **Fase 1** (Bitwarden, KeePassX, o similar), heu de crear una **Guia d'Ús per a l'Equip Tècnic**.  
Aquesta guia ha de ser **clara** i basada en **captures de pantalla** i **instruccions pas a pas**.

---

## 📘 Contingut Obligatori de la Guia

### 🔧 Instal·lació i Configuració Inicial
Descàrrega i instal·lació de l'eina seleccionada.  
Creació de la **BBDD principal** o **compte mestre**.

---

### 🔐 Generació de Contrasenyes Segures
Explicació de com utilitzar el **generador de contrasenyes** de l'eina.  
Indicació dels **paràmetres recomanats**: longitud, ús de caràcters especials, nombres i majúscules/minúscules.

---

### 💼 Exemples d'Ús i Emplenament Automàtic
Incloeu exemples pràctics sobre com:
**Desar una credencial** d’un compte de correu electrònic.  
**Desar una credencial** d’una aplicació o servei web.  
**Fer servir l’extensió del navegador** per emplenar automàticament les dades d’accés.

---

### 🗂️ Gestió de Còpies de Seguretat (Backup)
Explicació detallada de com **fer una còpia de seguretat** de l'arxiu de contrasenyes:  
  - **KDBX** en el cas de KeePass.  
  - **Exportació** en el cas de Bitwarden.  
Recomanació de **bones pràctiques** per emm
agatzemar la còpia de seguretat de forma segura:
  - **Clau USB xifrada**  
  - **Emmagatzematge xifrat al núvol**

 A l'arxiu [informe.md](informe.md) hi ha la tasca1

[Torna a la pàgina principal](../README.md)
