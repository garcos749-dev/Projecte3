# T07: Instal·lant un servidor de noms

![imatge](img/foto1.png)

## 🧩 Breu descripció

Després de l’exitosa experiència a nivell de formació, els nostres clients de **Digicore** estan tan satisfets amb la nostra feina que ens encarreguen la **implantació des de zero dels seus serveis de DNS interns**.

Actualment, l’agència fa servir **adreces IP** per accedir als seus servidors de desenvolupament, bases de dades i eines de gestió interna. Aquest mètode és **ineficaç i propens a errors**:

* **Usabilitat deficient:** Els empleats han de memoritzar o buscar constantment adreces IP complexes (p. ex., `192.168.10.25`).
* **Manteniment feixuc:** Si un servidor canvia la seva IP, cal notificar i actualitzar manualment la configuració a tots els equips i aplicacions.
* **Manca de professionalitat:** En un entorn professional, tots els serveis haurien de ser accessibles mitjançant **noms fàcils de recordar**.

Per tant, la nostra missió és implementar un **Sistema de Noms de Domini (DNS)** intern robust.
L'objectiu és que els servidors i aplicacions de l’agència es puguin accedir utilitzant noms de domini **amigables**, com per exemple:

```
bbdd.digicore.lan
wiki.digicore.lan
```

---

## 🎯 El vostre repte

Com a consultora, la recomanació és utilitzar **BIND9**, l’estàndard de facto de servidor de noms a **Linux**, per la seva fiabilitat i flexibilitat.

La vostra missió serà:

* **Instal·lar i configurar un servidor DNS primari (màster)** amb **BIND9** en un sistema **Linux**.
* Crear una **Zona Directa (Forward Zone)** i una **Zona Inversa (Reverse Zone)** per al domini privat de DigiCore, garantint la resolució bidireccional (noms ↔ IPs).
* Per a la prova de concepte, utilitzeu el domini `digicore-XX.test`, on **XX** serà el vostre número de llista.

---

## ⚙️ Pas previ: configuració inicial

1. Configurar un **Ubuntu Server** amb:

   * 4 GB de RAM
   * 20 GB de disc
   * 2 interfícies de xarxa:

     * **Adaptador pont** (configurat segons les indicacions inicials del repte)
     * **Host-only**

2. Instal·lar els paquets necessaris:

   ```bash
   sudo apt update
   sudo apt install bind9 ssh
   ```

3. El servei **SSH** permetrà exportar els arxius de configuració al vostre **repositori de GitHub**.

---

## 🔧 Accions a realitzar

### 1. Configuració bàsica del servidor DNS

* Editar l’arxiu `named.conf.options` perquè:

  * Accepti **consultes recursives** de la xarxa local.
  * Utilitzi com a **reenviador** la IP `8.8.8.8`.
* Mostrar captura de pantalla de la configuració.
* Reiniciar el servei i comprovar l’estat:

  ```bash
  sudo systemctl restart bind9
  sudo systemctl status bind9
  ```

---

### 2. Configuració del client DNS

* Utilitzar una màquina **Zorin** (o similar).
* Canviar l’adaptador a **adaptador pont**.
* Assignar com a **DNS primari** la IP del vostre servidor.
* Comprovar la resolució a Internet:

  ```bash
  dig google.com
  ```

  o obrint una pàgina web al navegador.

---

### 3. Definició de zones DNS

Editar l’arxiu `named.conf.local` per definir:

* **Zona directa:** `digicore-XX.test`
* **Zona inversa:** corresponent a la xarxa local utilitzada a la prova de concepte.

---

### 4. Creació de la zona directa

1. Crear la carpeta de zones:

   ```bash
   sudo mkdir /etc/bind/zones
   ```

2. Crear l’arxiu de zona directa copiant el model:

   ```bash
   sudo cp /etc/bind/db.local /etc/bind/zones/db.digicore-XX.test
   ```

3. Configurar l’arxiu amb els següents **registres**:

   ```
   $TTL 604800
   @   IN  SOA  server.digicore-XX.test. admin.digicore-XX.test. (
            2025110601 ; Serial
            604800     ; Refresh
            86400      ; Retry
            2419200    ; Expire
            604800 )   ; Negative Cache TTL

       IN  NS      server.digicore-XX.test.
   server IN  A       [IP del servidor]
   dbserver IN  A     [IP del client]
   data IN  CNAME     dbserver
   ```

---

### 5. Creació de la zona inversa

1. Crear l’arxiu copiant el model:

   ```bash
   sudo cp /etc/bind/db.127 /etc/bind/zones/db.reverse-XX
   ```

2. Configurar-lo amb:

   * **SOA i NS** adients.
   * **Registres PTR** per al `server` i el `dbserver`.

---

### 6. Verificació

* Reiniciar el servei:

  ```bash
  sudo systemctl restart bind9
  ```
* Fer comprovacions des del client amb consultes directes i inverses:

  ```bash
  dig server.digicore-XX.test
  dig -x [IP del servidor]
  ```

---

### 7. Transferència de zona i DNS secundari

1. Editar `named.conf.local` per **permetre la transferència de la zona directa** als companys de l’equip.
2. Configurar una **zona secundària** amb el domini d’un altre company.
3. **Forçar la transferència** i comprovar el funcionament des del client.

---

## 🧠 Activitat d’avaluació del repte

Per demostrar la vostra competència tècnica, haureu de superar una **avaluació pràctica** al final del repte.

Durant aquesta prova:

* Només podreu utilitzar **un full manuscrit** amb les vostres anotacions.
* El full es **lliurarà en finalitzar** la prova.

---
