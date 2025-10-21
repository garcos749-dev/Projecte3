# 🧩 INFORME TÈCNIC  
## T01 – Gestor de contrasenyes  

**Consultora:** EverPia  
**Autor:** Javier García  
**Data:** 21/10/2025  

---

## 📑 Índex  

1. [Introducció i justificació](#1-introducció-i-justificació)  
2. [Comparativa tècnica de gestors de contrasenyes](#2-comparativa-tècnica-de-gestors-de-contrasenyes)  
3. [Avantatges i inconvenients dels models](#3-avantatges-i-inconvenients-dels-models)  
4. [Recomanació final](#4-recomanació-final)  
5. [Conclusions](#5-conclusions)  
6. [Annexos recomanats](#-annexos-recomanats)  

---

## 1. Introducció i justificació  

La seguretat de la informació és essencial per a qualsevol empresa tecnològica. Les contrasenyes actuen com la primera línia de defensa davant accessos no autoritzats i, per tant, la seva correcta gestió és clau per protegir dades corporatives, serveis i sistemes interns.  

En els darrers anys, l’ús de **contrasenyes febles o reutilitzades** ha estat un dels principals factors que han permès **ciberatacs i filtracions de dades**.  
Mitjançant tècniques com **els atacs de diccionari** o **el credential stuffing**, els atacants aconsegueixen accedir a comptes corporatius reutilitzant credencials robades en altres plataformes.  

Aquest tipus de vulnerabilitats va provocar recentment una **bretxa de seguretat a EverPia**, després que un tècnic utilitzés una contrasenya reutilitzada.  
Davant d’aquest incident, la Direcció Tècnica ha ordenat la implantació obligatòria d’un **gestor de contrasenyes corporatiu** per a tot el personal tècnic.  

Un gestor de contrasenyes permet **emmagatzemar i generar credencials de manera segura**, amb contrasenyes úniques, llargues i difícils d’endevinar.  
A més, garanteix que els usuaris **no hagin de recordar múltiples contrasenyes**, reduint la probabilitat d’errors humans i augmentant la seguretat general de l’organització.  

---

## 2. Comparativa tècnica de gestors de contrasenyes  

S’han comparat dues opcions principals: **Bitwarden**, com a alternativa en línia (núvol), i **KeePassXC**, com a solució local (offline).  

| **Característica** | **Bitwarden (Online / Núvol)** | **KeePassXC (Offline / Escriptori)** |
|--------------------|--------------------------------|--------------------------------------|
| **Tipus d’eina** | Núvol (online) | Local (offline) |
| **Model de seguretat** | Xifratge d’extrem a extrem (E2E), autenticació 2FA | Xifratge AES-256 del fitxer KDBX amb clau mestra |
| **Emmagatzematge** | Servidors al núvol de Bitwarden | Fitxer local KDBX guardat a l’equip o USB |
| **Accés** | Web, aplicació d’escriptori, mòbil i extensions de navegador | Només aplicació d’escriptori |
| **Codi font** | Open Source | Open Source |
| **Cost / Llicència** | Freemium (versió gratuïta i opció premium) | Gratuït completament |
| **Portabilitat** | Accessible des de qualsevol dispositiu amb Internet | Portàtil mitjançant fitxer exportable |
| **Dependència del núvol** | Sí | No |
| **Còpies de seguretat** | Automàtiques al servidor xifrat | Manuals (cal copiar el fitxer localment) |
| **Sincronització** | Automàtica entre dispositius | No disponible |
| **Autenticació multifactor (2FA)** | Inclosa | Limitada a l’accés local |

---

## 3. Avantatges i inconvenients dels models  

### 🟩 Bitwarden (Online / Núvol)  

**Avantatges:**  
- Sincronització automàtica entre tots els dispositius (ordinador, mòbil, navegador).  
- Interfície moderna, intuïtiva i fàcil d’utilitzar.  
- Xifratge d’extrem a extrem (E2E): només l’usuari pot desxifrar les seves dades.  
- Possibilitat d’activar **autenticació multifactor (2FA)**.  
- Còpies de seguretat automàtiques i sistema de recuperació segura.  
- Compatible amb navegadors i plataformes mòbils (Android/iOS).  

**Inconvenients:**  
- Depèn d’una connexió a Internet.  
- En entorns molt crítics, confiar en un proveïdor extern pot ser vist com un risc.  
- Algunes funcions avançades (com compartir grups o auditories) requereixen la versió premium.  

---

### 🟦 KeePassXC (Offline / Local)  

**Avantatges:**  
- Total control sobre la base de dades i les credencials.  
- Funciona sense connexió a Internet.  
- Programari 100% gratuït i de codi obert.  
- No depèn de cap servidor extern.  

**Inconvenients:**  
- No disposa de sincronització automàtica entre dispositius.  
- Les còpies de seguretat s’han de fer manualment.  
- Interfície menys intuïtiva i sense aplicació mòbil oficial.  

---

## 4. Recomanació final  

Després d’analitzar les dues alternatives, es recomana la implementació de **Bitwarden** com a gestor de contrasenyes corporatiu a EverPia.  

### 🧠 Motivacions principals de la decisió:  

- **Sincronització i accessibilitat:**  
  Bitwarden permet accedir a les credencials des de qualsevol dispositiu, cosa que és essencial per a un equip tècnic distribuït o amb teletreball.  

- **Xifratge avançat i seguretat zero-knowledge:**  
  Totes les dades estan protegides amb **xifratge d’extrem a extrem**, i només l’usuari posseeix la clau per desxifrar-les. Ni tan sols Bitwarden pot accedir a les contrasenyes.  

- **Eficiència operativa:**  
  Els tècnics poden compartir credencials d’equip o projectes de manera segura, sense haver d’intercanviar contrasenyes per correu o missatgeria.  

- **Gestió centralitzada i còpies automàtiques:**  
  Les còpies de seguretat s’executen de forma automàtica al núvol, garantint que cap dada es perdi.  

- **Compatibilitat total:**  
  Bitwarden és multiplataforma i funciona en navegadors, aplicacions d’escriptori i dispositius mòbils, adaptant-se a qualsevol entorn de treball.  

- **Autenticació de dos factors (2FA):**  
  Afegeix una capa addicional de seguretat per protegir l’accés als comptes.  

Amb tot això, **Bitwarden** és l’opció més equilibrada entre seguretat, comoditat i eficiència per a EverPia.  

---

## 5. Conclusions  

La implantació de **Bitwarden** com a gestor de contrasenyes corporatiu suposa un pas fonamental per millorar la seguretat i la productivitat a EverPia.  

Gràcies a aquesta eina, l’empresa:  
- Redueix dràsticament el risc d’ús de contrasenyes febles o repetides.  
- Centralitza la gestió de credencials de manera segura i eficient.  
- Millora la col·laboració entre equips tècnics amb credencials compartides de forma xifrada.  
- Garanteix l’accés segur des de qualsevol dispositiu amb connexió a Internet.  

En conclusió, **Bitwarden** ofereix una solució moderna, escalable i de confiança per garantir la seguretat de les credencials corporatives, reforçant la ciberseguretat d’EverPia i minimitzant els riscos de futures bretxes d’informació.  

---

## 📎 Annexos recomanats  

- **Web oficial de Bitwarden:** [https://bitwarden.com](https://bitwarden.com)  
- **Guia d’ús tècnica:** (vegeu document [`guia.md`](guia.md))  
- **Referència:** [INCIBE – Gestores de contraseñas](https://www.incibe.es/protege-tu-empresa/blog/gestores-de-contrasenas)  
