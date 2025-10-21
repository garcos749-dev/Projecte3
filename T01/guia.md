# 🧩 GUIA D’ÚS TÈCNICA  
## T01 – Gestor de contrasenyes: Bitwarden  

**Consultora:** EverPia  
**Autor:** Javier García  
**Data:** 21/10/2025  

---

## 📑 Índex  

1. [Introducció](#1-introducció)  
2. [Instal·lació i configuració inicial](#2-instal·lació-i-configuració-inicial)  
3. [Generació de contrasenyes segures](#3-generació-de-contrasenyes-segures)  
4. [Exemples d’ús i emplenament automàtic](#4-exemples-dús-i-emplenament-automàtic)  
5. [Gestió de còpies de seguretat (Backup)](#5-gestió-de-còpies-de-seguretat-backup)  
6. [Resolució de problemes comuns](#6-resolució-de-problemes-comuns)  
7. [Conclusions i bones pràctiques](#7-conclusions-i-bones-pràctiques)  
8. [Annexos recomanats](#8-annexos-recomanats)  

---

## 1. Introducció  

Aquesta guia descriu el procés complet per instal·lar, configurar i utilitzar **Bitwarden**, el gestor de contrasenyes seleccionat per EverPia com a mesura de seguretat corporativa per al seu equip tècnic.  

Bitwarden és una eina **de codi obert, multiplataforma i basada en el núvol** que permet emmagatzemar, generar i compartir credencials de manera segura.  
Les dades s’emmagatzemen **xifrades d’extrem a extrem (E2E)**, de manera que només l’usuari pot desxifrar les seves contrasenyes.  

Aquesta solució facilita una gestió eficient i segura de les credencials, especialment per a equips distribuïts o amb treball remot.  

---

## 2. Instal·lació i configuració inicial  

### 2.1. Creació del compte i accés  

1. Accediu a la web oficial: [https://bitwarden.com](https://bitwarden.com).  
2. Feu clic a **“Get Started”** i creeu un compte amb una adreça de correu corporativa.  
3. Definiu una **contrasenya mestra robusta** (mínim 12 caràcters, amb majúscules, minúscules, números i símbols).  
4. Activeu l’opció **Two-Factor Authentication (2FA)** per afegir una capa extra de seguretat.  

### 2.2. Instal·lació de les aplicacions  

Bitwarden ofereix diverses opcions d’instal·lació:  

- **Aplicació d’escriptori:** [https://bitwarden.com/download](https://bitwarden.com/download)  
  - Disponible per Windows, macOS i Linux.  
- **Extensió de navegador:** per Chrome, Firefox, Edge, Opera o Brave.  
- **Aplicació mòbil:** disponible a [Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden) i [App Store](https://apps.apple.com/app/bitwarden-password-manager/id1137397744).  

Un cop instal·lada, inicia la sessió amb el compte corporatiu.  

### 2.3. Configuració inicial  

1. Accediu al tauler principal de Bitwarden.  
2. Creeu un **Vault** (volta) on es guardaran totes les credencials.  
3. Activeu l’opció **Autolock** perquè la sessió es bloquegi automàticament després d’un temps d’inactivitat.  
4. Configureu la **sincronització automàtica** entre dispositius.  

---

## 3. Generació de contrasenyes segures  

Bitwarden incorpora un **generador de contrasenyes integrat** que crea claus aleatòries, llargues i segures.  

### 3.1. Com generar una contrasenya  

1. Feu clic a **“Generator”** (icona de claus) dins de la interfície de Bitwarden.  
2. Trieu el tipus de contrasenya que voleu generar:  
   - **Password:** per contrasenyes normals.  
   - **Passphrase:** combinació de paraules aleatòries més fàcil de recordar.  
3. Ajusteu els paràmetres:  
   - Longitud recomanada: **mínim 16 caràcters**.  
   - Incloure **majúscules, minúscules, números i símbols**.  
4. Copieu i deseu la contrasenya directament al vostre **Vault**.  

---

## 4. Exemples d’ús i emplenament automàtic  

### 4.1. Desar una credencial de correu electrònic  

1. Feu clic a **“Add Item” → “Login”**.  
2. Introduïu:  
   - **Nom:** Compte de correu corporatiu.  
   - **Usuari:** la vostra adreça de correu electrònic.  
   - **Contrasenya:** enganxeu la generada amb l’eina anterior.  
   - **URL:** ex. `https://outlook.office.com`.  
3. Feu clic a **Save** per guardar la credencial.  

### 4.2. Desar una credencial d’una aplicació o servei web  

1. Creeu un nou element amb el nom del servei (ex: *GitHub – EverPia*).  
2. Introduïu l’usuari, la contrasenya i l’enllaç d’accés.  
3. Organitzeu les entrades dins de **carpetes** (ex: “Correu”, “Aplicacions”, “Serveis interns”).  

### 4.3. Emplenament automàtic amb l’extensió del navegador  

Bitwarden pot emplenar automàticament els camps de correu i contrasenya en pàgines web.  

1. Instal·leu l’extensió corresponent al vostre navegador.  
2. Inicieu sessió amb el vostre compte.  
3. Aneu a la pàgina d’inici de sessió d’un servei.  
4. Bitwarden detectarà l’URL i mostrarà les credencials disponibles.  
5. Feu clic a **“Autofill”** per emplenar automàticament els camps.  

---

## 5. Gestió de còpies de seguretat (Backup)  

Les còpies de seguretat són essencials per garantir que les credencials no es perdin.  

### 5.1. Còpies de seguretat automàtiques  

Bitwarden crea còpies de seguretat **xifrades al núvol** de manera automàtica.  
Aquestes còpies només poden ser desxifrades per l’usuari amb la seva contrasenya mestra.  

### 5.2. Exportació manual  

1. Accediu al **Vault**.  
2. Feu clic a **“Settings → Export Vault”**.  
3. Seleccioneu el format **.json** o **.csv** i guardeu-lo localment.  
⚠️ **Important:** assegureu-vos que el fitxer exportat estigui emmagatzemat en un dispositiu segur o dins d’un arxiu xifrat.  

### 5.3. Bones pràctiques  

- No deseu mai l’exportació sense xifrar en carpetes públiques o compartides.  
- Activeu la còpia de seguretat automàtica al núvol de Bitwarden.  
- Reviseu periòdicament la sincronització entre dispositius.  

---

## 6. Resolució de problemes comuns  

| **Problema** | **Possible causa** | **Solució** |
|--------------|-------------------|--------------|
| No recordo la contrasenya mestra | Error humà o oblit | Utilitzeu el sistema de **pista de contrasenya** o restabliu el compte (perdreu les dades actuals). |
| No es sincronitzen els dispositius | Connexió a Internet o retard de núvol | Reviseu la connexió i feu clic a **Sync Now** al tauler. |
| L’emplenament automàtic no funciona | Extensió no connectada | Torneu a iniciar sessió a l’extensió o reinicieu el navegador. |

---

## 7. Conclusions i bones pràctiques  

L’ús de **Bitwarden** millora significativament la seguretat i l’eficiència en la gestió de credencials corporatives.  
Aquesta eina permet centralitzar la informació de manera segura, reduint la probabilitat d’errors humans i millorant la productivitat de l’equip tècnic.  

### Bones pràctiques recomanades:  
- Utilitzar sempre **contrasenyes úniques i llargues**.  
- Activar **autenticació de dos factors (2FA)**.  
- No compartir la contrasenya mestra amb ningú.  
- Comprovar regularment la sincronització entre dispositius.  
- Revisar i eliminar credencials antigues o innecessàries.  

Amb la correcta implantació de Bitwarden, EverPia millora la seva cultura de seguretat i reforça la protecció dels seus projectes i dades sensibles.  

---

## 8. Annexos recomanats  

- [Web oficial de Bitwarden](https://bitwarden.com)  
- [Manual d’ajuda Bitwarden](https://bitwarden.com/help)  
- [Extensió de navegador Bitwarden](https://bitwarden.com/download/#browser)  
- [INCIBE – Gestores de contraseñas](https://www.incibe.es/protege-tu-empresa/blog/gestores-de-contrasenas)  
