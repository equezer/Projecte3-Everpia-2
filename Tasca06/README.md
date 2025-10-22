# T06: Fonaments del servei DNS

Com a membres cada cop més integrats de l'equip tècnic de la consultora **EverPia**, teniu davant un nou repte.  
El vostre client, una empresa de màrqueting digital (**DigiCore**), experimenta de tant en tant errors de connectivitat a certes aplicacions.  

El seu equip tècnic creu que la causa principal podria ser una **resolució de noms (DNS)** incorrecta o lenta.  
Se us ha encarregat realitzar una **auditoria teòrica i pràctica del servei DNS** per tal de formar el personal del client i oferir **eines de diagnosi ràpides**.

---

## 🧩 Producte final a entregar

1. Crear una carpeta al repositori anomenada `tasca06`.  
2. A l’arxiu `README.md`:
   - Copiar **l’enunciat de l’activitat**.  
   - Afegir una secció anomenada **Activitats**, on inclogueu:
     - 🔗 L’enllaç al **vídeo gravat** (pujat a **Drive** o al vostre **Office365** amb l’aplicació *Stream*).  
       > Assegureu-vos de donar permisos de reproducció.  
     - 📄 L’enllaç al document `guia.md` de la fase pràctica.

---

## 🧠 Fase Teòrica: Sessió formativa

Com a part d’aquesta formació, caldrà que **elaboreu un material formatiu** pel personal del client.  
Per assegurar la màxima qualitat dels continguts, els vostres directors tècnics han preparat unes **sessions prèvies** per tal que tingueu domini dels conceptes que després haureu d’explicar.

### 📘 Conceptes a treballar

#### 🔹 Jerarquia i Estructura
- Explicació de l'estructura en arbre del DNS:  
  **Root > TLDs > Segon Nivell**

#### 🔹 Procés de Resolució
- Diferència entre consulta **iterativa** i **recursiva**.  
- Què és un **servidor d'arrel (Root Server)** i un **servidor autoritatiu**.

#### 🔹 Tipus de Zones
- **Zona directa** i **zona inversa**.  
- **Zona primària** i **zona secundària**.

#### 🔹 Tipus de Registres Clau (Records)
- Funció dels registres **A**, **CNAME**, **MX**, **NS** i **TXT**.

#### 🔹 Conceptes Essencials
- **Resposta autoritativa:** què significa i com identificar-la.  
- **Time To Live (TTL):** funció i impacte en la propagació i el rendiment.  
- **Start of Authority (SOA):** informació essencial i importància.  
- **Reenviadors:** condicionals i incondicionals.  
- **Resolució local:** mecanismes de resolució sense servidor entre equips clients (protocol **mDNS**).

### 🎥 Activitat de la Fase Teòrica
Un cop domineu aquests conceptes, haureu de preparar una **píndola formativa** en format **vídeo** (entre **10 i 15 minuts**) que expliqui de forma breu però clara tots aquests conceptes.

---

## 💻 Fase Pràctica: Diagnosi de Noms (Auditoria amb CLI)

Heu de demostrar l'ús de les principals **utilitats de diagnosi DNS** en els diferents sistemes operatius que utilitza el client (**Linux/macOS** i **Windows**).

Per a cada eina, executeu les comandes indicades contra el domini especificat i **captureu/analitzeu els resultats**.

> 💡 Per fer aquesta demostració, caldrà utilitzar un equip **Zorin** amb dues interfícies:
> - Primera: **NAT**  
> - Segona: **Adaptador pont**  
> - IP configurada correctament segons indicacions dels responsables tècnics.

Al arxiu: [Activitats.md](Activitats.md) hi ha la solució de la Tasca6
