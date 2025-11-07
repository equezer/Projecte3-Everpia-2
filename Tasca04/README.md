## T04: Serveis de directori. LDAP Implementació d’un Sistema d’Autenticació Centralitzada amb OpenLDAP

## Context

**Innovatech**, una start-up tecnològica emergent, està experimentant un ràpid creixement i pateix un **caos en la gestió dels seus usuaris i accessos**.  

Actualment, cada servei intern (servidor de fitxers, wiki de documentació, etc.) utilitza la seva pròpia base de dades d'usuaris i contrasenyes i, a més, als ordinadors clients s’usa **autentificació local**.  

Això genera diversos problemes crítics:

---

## Problemes Detectats

1. **Ineficiència Operativa:**  
   Cada cop que s'incorpora o marxa un empleat, l'equip tècnic ha de crear o eliminar el compte en múltiples sistemes.

2. **Risc de Seguretat:**  
   Els usuaris sovint acaben reutilitzant contrasenyes entre serveis per evitar l'oblit.

3. **Manca d'Escalabilitat:**  
   A mesura que Innovatech afegeix nous serveis, el problema es fa insostenible.

<img width="147" height="217" alt="image" src="https://github.com/user-attachments/assets/0e4e8392-455c-46e6-91e7-cfbc4fd6255b" />


## Solució Proposada

El **CEO d’Innovatech** ha contactat amb **EverPia** per tal d’implementar una **solució d’autenticació centralitzada**.  

La solució proposada és utilitzar **OpenLDAP (Lightweight Directory Access Protocol)** per ser una eina **robusta i de codi obert**, que s’alinea amb l’esperit d’Innovatech, ja que tots els ordinadors de l’empresa utilitzen **GNU/Linux**.

---

## Objectius de la Missió

La vostra missió serà **implementar el servei OpenLDAP en un servidor Linux**, cosa que implica:

Instal·lar el servei.  
Configurar el **domini base**.  
Crear la **jerarquia d'unitats organitzatives (OU)**.  
Integrar **usuaris i grups** que posteriorment s'utilitzaran per donar accés a altres serveis de xarxa.  
Configurar un **equip client** perquè utilitzi el directori per autenticar els usuaris.

---

## Documentació de Referència

S’ha redactat un document on s’especifica clarament la feina que s’ha de desenvolupar.  
El teniu disponible en el **plec de condicions tècniques** (també accessible al **Moodle de l’assignatura**).

a l'arxiu: [solucio.md](solucio.md) trobaras la solució a la tasca

[Torna a la pàgina principal](../README.md)
