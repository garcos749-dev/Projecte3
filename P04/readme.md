# P04: Documentació servidor DNS

## 🧩 Breu descripció

Benvinguts, consultors!
Com a membres de l’equip de **Sistemes d’EverPia**, us heu enfrontat al repte de configurar un **servidor de noms (DNS)** com a prova de concepte per al nostre client **DigiCore**.

Ara bé, el resultat de la vostra feina es troba dins d’una **màquina virtual**.
L’objectiu d’aquesta tasca és **publicar les configuracions a GitHub**, de manera que qualsevol persona pugui **replicar el servidor DNS** fàcilment, simplement descarregant els arxius i reiniciant el servei al seu servidor Linux.

Així assegurem:

* **Disponibilitat** de la configuració.
* **Repetibilitat** del procés.
* **Eficiència** en el desplegament de futurs servidors.

---

## ⚙️ Fase 1: Preparació de la connectivitat i extracció dels arxius

### 🔹 Pas 1.1: Configuració de la interfície *Host-Only*

1. A la configuració de la màquina virtual **Ubuntu Server**, afegiu una **segona interfície de xarxa** en mode **Host-Only**.
2. Configureu-la i **activeu-la** dins del sistema.
3. Comproveu la **connectivitat** des de la màquina física (host) mitjançant ordres com `ping` o `ssh`.

### 🔹 Pas 1.2: Còpia segura dels fitxers clau amb SCP

Un cop establerta la connectivitat, utilitzareu **SCP (Secure Copy Protocol)** —inclòs amb el servei SSH— per transferir els arxius de configuració a la màquina física.

**Fitxers a copiar:**

```
/etc/bind/named.conf.options
/etc/bind/named.conf.local
/etc/bind/zones/ (tots els arxius de zona)
```

**Exemple de comanda:**

```bash
scp usuari@ip_del_servidor:/etc/bind/named.conf.options .
```

> El punt (`.`) al final indica que l’arxiu es copiarà al **directori actual** del vostre ordinador host.

---

## 🧭 Fase 2: Integració a GitHub

### 🔹 Pas 2.1: Crear carpeta i arxiu `README.md`

1. Creeu una carpeta anomenada `producte04` al vostre repositori.

   * En GitHub, podeu fer-ho seleccionant **“New File”** i escrivint el nom complet:

     ```
     producte04/README.md
     ```
2. Dins el fitxer `README.md`, incloeu:

   * El **títol del producte** (`P04: Documentació servidor DNS`)
   * Una **breu descripció** del contingut i dels fitxers inclosos.

---

### 🔹 Pas 2.2: Pujar arxius

1. Pugeu els arxius del servidor DNS a la carpeta `producte04`.
2. Creeu prèviament una subcarpeta `zones` per a les zones DNS:

   ```
   producte04/zones/
   ```
3. Per facilitar la creació inicial, podeu afegir un fitxer temporal anomenat `zones/esborrar` i eliminar-lo un cop pujats els arxius reals.

---

## 🎯 Objectius específics de la tasca / Finalitat de la tasca

* **Utilitzar GitHub** per **documentar configuracions de servidors**.
* Valorar els avantatges de la **repetibilitat** en entorns tècnics.
* **Garantir la traçabilitat** i la **seguretat** de la configuració mitjançant control de versions.
* Afavorir la **col·laboració i reutilització** dels recursos dins l’equip tècnic.

---
