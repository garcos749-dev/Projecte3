
# 🧩 INFORME TÈCNIC  
## T01 – Gestor de contrasenyes  

**Consultora:** EverPia  
**Autor:** Javier García  
**Data:** 21/10/2025  

---

## 1. Introducció i justificació  

La seguretat de la informació és un dels pilars fonamentals en qualsevol empresa tecnològica.  
Les contrasenyes constitueixen la primera línia de defensa per protegir els sistemes, serveis i dades corporatives.  

No obstant això, una de les causes més freqüents de vulnerabilitats és l’ús de **contrasenyes febles, simples o reutilitzades** en múltiples comptes.  
Aquest problema ha provocat nombrosos **ciberatacs** basats en tècniques com els **atacs de diccionari** o el **credential stuffing**, on els atacants proven combinacions de contrasenyes filtrades prèviament.  

Això pot provocar accessos no autoritzats, robatori d’informació, suplantacions d’identitat o, fins i tot, bloquejos dels sistemes interns.  

En el cas d’EverPia, la fuita d’informació recent ha demostrat que una contrasenya reutilitzada per un tècnic va ser l’origen de la bretxa de seguretat.  
Davant d’aquest incident, la Direcció Tècnica ha establert la implementació obligatòria d’un **gestor de contrasenyes** per a tot el personal tècnic.  

Un gestor de contrasenyes és una eina que permet **generar, desar i gestionar de manera segura totes les credencials d’un usuari**, garantint que cada compte tingui una contrasenya única, complexa i difícil d’endevinar.  
A més, aquests gestors eviten que les contrasenyes quedin exposades o s'emmagatzemin en documents o navegadors sense protecció.  

---

## 2. Comparativa tècnica de gestors de contrasenyes  

S’han analitzat dues eines principals per determinar quina és la més adequada per a EverPia:  

| **Característica** | **Bitwarden (Online / Núvol)** | **KeePassXC (Offline / Escriptori)** |
|--------------------|--------------------------------|--------------------------------------|
| **Tipus d’eina** | Núvol (online) | Local (offline) |
| **Model de seguretat** | Xifratge d’extrem a extrem (E2E), autenticació 2FA | Xifratge AES-256 del fitxer KDBX amb clau mestra |
| **Emmagatzematge** | Servidors al núvol de Bitwarden | Fitxer local KDBX guardat a l’equip o USB |
| **Accés** | Multidispositiu (web, app, navegador) | Escriptori (Windows, Linux, macOS) |
| **Codi font** | Open Source | Open Source |
| **Cost / Llicència** | Freemium (versió bàsica gratuïta, premium opcional) | Gratuït completament |
| **Portabilitat** | Requereix connexió a Internet | Totalment portàtil (fitxer exportable) |
| **Dependència del núvol** | Alta | Cap |
| **Risc de filtració externa** | Possible si hi ha bretxa al servei | Només si es perd o roba el fitxer local |

---

## 3. Avantatges i inconvenients dels models  

### **Bitwarden (Online)**  

**Avantatges:**  
- Sincronització automàtica entre dispositius.  
- Còpies de seguretat integrades.  
- Accessible des de qualsevol lloc.  

**Inconvenients:**  
- Depèn del núvol i d’una connexió a Internet.  
- Possible risc en cas de vulnerabilitat al servei extern.  
- Algunes funcions requereixen versió premium.  

---

### **KeePassXC (Offline)**  

**Avantatges:**  
- Control total de les dades (no depèn del núvol).  
- Eina open source i gratuïta.  
- Alta seguretat gràcies al xifratge AES-256 del fitxer KDBX.  
- Portabilitat senzilla amb memòries USB.  

**Inconvenients:**  
- No sincronitza automàticament entre dispositius.  
- Requereix còpies de seguretat manuals.  
- No disposa d’aplicació mòbil oficial.  

---

## 4. Recomanació final  

Després de l’anàlisi, es recomana la implementació de **KeePassXC** com a gestor de contrasenyes per al personal tècnic d’EverPia.  

### **Motivacions principals de la decisió:**  

- **Seguretat total i independència del núvol:**  
  KeePassXC emmagatzema totes les dades localment en un fitxer xifrat `.kdbx`, evitant exposar credencials a servidors externs.  

- **Cost zero:**  
  És una eina completament gratuïta i de codi obert, accessible per a tot el personal sense costos recurrents.  

- **Control i transparència:**  
  Permet a l’empresa tenir un control complet sobre la gestió i la ubicació dels arxius, afavorint polítiques internes de seguretat.  

- **Portabilitat:**  
  El fitxer de la base de dades pot guardar-se en dispositius xifrats (claus USB, discs externs) i obrir-se des de qualsevol ordinador de manera segura.  

- **Compliment de bones pràctiques de seguretat:**  
  KeePassXC permet generar contrasenyes fortes, llargues i úniques, minimitzant riscos d’atacs de força bruta o reutilització.  

Amb tot això, **KeePassXC** s’ajusta perfectament a les necessitats de la consultora EverPia, oferint una solució robusta, segura i controlada internament per evitar futurs incidents de seguretat.  

---

## 5. Conclusions  

La implantació d’un gestor de contrasenyes és una mesura essencial dins la política de seguretat d’EverPia.  
L’ús d’eines com KeePassXC permet reduir significativament el risc d’atacs derivats de contrasenyes febles o reutilitzades i millora la **ciberhigiene** del personal tècnic.  

Amb aquesta implementació, l’empresa:  
- Incrementa la protecció de dades internes i projectes en desenvolupament.  
- Millora la cultura de seguretat entre els empleats.  
- Redueix el risc de noves bretxes d’informació.  

L’ús responsable i la formació contínua en seguretat digital seran claus per mantenir la integritat i la confiança dins d’EverPia.  

---
## 📎 Annexos recomanats  

- **Fitxer d’instal·lació de KeePassXC:** [https://keepassxc.org/download](https://keepassxc.org/download)  
- **Guia d’ús tècnica:** (vegeu document `guia.md`)  
- **Referència:** [INCIBE – Gestores de contraseñas](https://www.incibe.es/protege-tu-empresa/blog/gestores-de-contrasenas)  
