# 🧩 GUIA D’ÚS TÈCNICA  
## T01 – Gestor de contrasenyes: KeePassXC  

**Consultora:** EverPia  
**Autor:** Javier García  
**Data:** 21/10/2025  

---

### 1. Introducció  

Aquesta guia té com a objectiu explicar, pas a pas, com instal·lar, configurar i utilitzar **KeePassXC**, el gestor de contrasenyes escollit per la consultora EverPia per garantir una gestió segura i eficient de les credencials corporatives.  

KeePassXC és un programari **lliure, multiplataforma i de codi obert** que permet emmagatzemar totes les contrasenyes en una **base de dades local xifrada (.kdbx)** protegida amb una clau mestra o un arxiu de claus.  
A diferència d’altres gestors basats en el núvol, KeePassXC funciona **de manera completament local**, cosa que garanteix una seguretat i control total sobre les dades.  

---

### 2. Instal·lació i configuració inicial  

#### 2.1. Descàrrega i instal·lació  

1. Accediu al lloc web oficial: [https://keepassxc.org/download](https://keepassxc.org/download)  
2. Descarregueu la versió corresponent al vostre sistema operatiu (Windows, macOS o Linux).  
3. Executeu l’instal·lador i seguiu les instruccions fins a completar la instal·lació.  
4. Un cop instal·lat, obriu el programa **KeePassXC** des del menú d’aplicacions o l’escriptori.  

#### 2.2. Creació de la base de dades principal  

1. Feu clic a **“Nova base de dades” (New Database)**.  
2. Introduïu un **nom identificatiu** (per exemple, *Credencials_EverPia*).  
3. Seleccioneu el **nivell de seguretat del xifratge (AES-256 per defecte)**.  
4. Trieu una **contrasenya mestra robusta** (mínim 12 caràcters amb majúscules, minúscules, números i símbols).  
   - També podeu afegir un **fitxer de clau (key file)** com a segona capa de seguretat.  
5. Deseu la base de dades (`.kdbx`) en una ubicació segura de l’ordinador o una clau USB xifrada.  

---

### 3. Generació de contrasenyes segures  

KeePassXC incorpora un generador automàtic de contrasenyes que permet crear claus fortes i úniques per a cada compte.  

#### 3.1. Com accedir al generador  

1. A la barra d’eines, feu clic a **“Eines → Generador de contrasenyes”** o utilitzeu la drecera **Ctrl + G**.  
2. Seleccioneu els paràmetres de seguretat:  
   - Longitud recomanada: **16 caràcters o més**.  
   - Incloure: **majúscules, minúscules, números i símbols**.  
   - Evitar caràcters semblants (`O` i `0`, `l` i `1`) per facilitar-ne la lectura.  
3. Copieu la contrasenya generada i deseu-la directament dins de l’entrada corresponent al vostre compte.  

---

### 4. Exemples d’ús i emplenament automàtic  

#### 4.1. Desar una credencial de correu electrònic  

1. A la base de dades oberta, feu clic a **“Nova entrada” (Add New Entry)**.  
2. Introduïu:  
   - **Nom de l’entrada:** Compte de correu corporatiu.  
   - **Nom d’usuari:** el vostre usuari o adreça de correu.  
   - **Contrasenya:** enganxeu la contrasenya generada amb l’eina anterior.  
   - **URL:** adreça del servei (ex: `https://outlook.office.com`).  
3. Deseu els canvis amb **Ctrl + S**.  

#### 4.2. Desar una credencial d’una aplicació o servei web  

1. Creeu una nova entrada amb el nom de l’aplicació (ex: *GitHub – EverPia*).  
2. Introduïu usuari, contrasenya i enllaç.  
3. Podeu organitzar les entrades en **carpetes o grups** (ex: “Xarxes”, “Correu”, “Aplicacions internes”).  

#### 4.3. Emplenament automàtic amb l’extensió del navegador  

KeePassXC ofereix una extensió per a Chrome, Firefox o Edge anomenada **KeePassXC-Browser**.  
Per utilitzar-la:  

1. Instal·leu l’extensió des de la botiga del vostre navegador.  
2. Obriu KeePassXC i aneu a **Eines → Configuració → Integració del navegador**.  
3. Activeu l’opció corresponent al vostre navegador.  
4. Quan accediu a un lloc web, KeePassXC reconeixerà l’URL i us permetrà **emplenar automàticament l’usuari i contrasenya**.  

---

### 5. Gestió de còpies de seguretat (Backup)  

Fer còpies de seguretat regulars és essencial per no perdre la base de dades de contrasenyes.  

#### 5.1. Creació de còpia de seguretat  

1. Tanqueu la base de dades.  
2. Copieu el fitxer `.kdbx` a una ubicació segura.  
3. Es recomana crear **dues còpies xifrades** en llocs diferents:  
   - **Còpia local:** en un disc o clau USB protegida amb contrasenya.  
   - **Còpia remota:** dins d’un servei de núvol xifrat (com Tresorit, MEGA o OneDrive amb xifratge activat).  

#### 5.2. Bones pràctiques  

- No deseu mai la contrasenya mestra al mateix lloc que la base de dades.  
- Actualitzeu la contrasenya mestra cada 6-12 mesos.  
- Mantingueu KeePassXC actualitzat a la seva darrera versió.  

---

### 6. Resolució de problemes comuns  

| **Problema** | **Possible causa** | **Solució** |
|--------------|-------------------|--------------|
| No recordo la contrasenya mestra | Error humà o oblit | No és possible recuperar-la; cal restaurar una còpia de seguretat. |
| El fitxer `.kdbx` no s’obre | Fitxer corrupte o incomplet | Proveu d’obrir una còpia anterior o reparar-la amb l’opció “Recuperar base de dades”. |
| L’extensió del navegador no detecta KeePassXC | No hi ha connexió entre aplicació i extensió | Reviseu la configuració d’integració del navegador a KeePassXC. |

---

### 7. Conclusions i bones pràctiques  

L’ús de KeePassXC permet establir una política de seguretat sòlida dins d’EverPia, reduint significativament el risc d’exposició de credencials.  

Algunes **bones pràctiques essencials** per garantir-ne l’efectivitat són:  

- Utilitzar sempre **contrasenyes úniques i complexes**.  
- Fer **còpies de seguretat periòdiques** i guardar-les en llocs segurs.  
- No compartir mai la contrasenya mestra amb ningú.  
- Mantindre l’aplicació i el sistema operatiu **actualitzats**.  
- Reforçar la seguretat amb **autenticació multifactor (2FA)** quan sigui possible.  

Amb la correcta implementació d’aquesta eina, EverPia augmenta la seva resiliència davant amenaces i assegura una millor gestió de la seva informació crítica.  

---

### 📎 Annexos recomanats  

- [Manual oficial de KeePassXC (Documentació)](https://keepassxc.org/docs/)  
- [Extensió oficial KeePassXC-Browser](https://addons.mozilla.org/firefox/addon/keepassxc-browser/)  
- [INCIBE – Gestores de contraseñas: qué son y cómo pueden mejorar la seguridad de las empresas](https://www.incibe.es/protege-tu-empresa/blog/gestores-de-contrasenas)  
