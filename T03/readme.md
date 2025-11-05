# 🧩 T03: Gestió flexible de discos (LVM i Espais d’emmagatzematge)

## 📄 Breu descripció
Un cop superada la fase de formació, ja esteu preparats per afrontar el repte dels nostres clients.  
El bufet d’advocats **Garriga i Associats**, un dels més prestigiosos de la ciutat, ha requerit els serveis de la nostra consultora **Everpia**.  
Gestionen una gran quantitat d'informació legal sensible, per la qual cosa la **integritat**, la **disponibilitat** (alta redundància) i la **facilitat de gestió** del seu emmagatzematge són d'importància crítica.

La direcció de "Garriga i Associats" ha expressat la necessitat urgent de renovar els seus sistemes de servidors per garantir que la informació estigui protegida contra fallades de disc i que l'espai pugui ser ampliat sense interrupcions.

Com a tècnics d’Everpia, teniu l'encàrrec de dissenyar i documentar les solucions d'emmagatzematge que compleixin aquests requisits tant en **entorns Linux com Windows**.  
Aquest disseny permetrà presentar al client una proposta de solució.

L'objectiu principal és **dissenyar i documentar dues solucions d'emmagatzematge** (una per servidors Linux i una per servidors Windows) que compleixin amb els principis d'**alta disponibilitat**, **redundància** i **escalabilitat** per al client.  

Com que es tracta d’una **prova de concepte**, no treballareu amb servidors, sinó que, per facilitat, utilitzareu màquines virtuals amb sistemes operatius clients per documentar els procediments.

---

## 🐧 1. Part Linux: LVM amb Zorin OS

S'ha d'utilitzar la distribució **Zorin OS** (o una alternativa Linux compatible) per demostrar la utilitat del **Logical Volume Manager (LVM)**.

### 🔧 Requisits de la implementació i demostració
- **Configuració inicial:**  
  Crear un grup de volums (VG) i un volum lògic (LV) utilitzant **dos discos simulats de 10 GB**.  
  El volum ha d’estar **formatat i muntat automàticament** mitjançant `/etc/fstab`.

- **Alta disponibilitat:**  
  Implementar la configuració d’un **mirall (lvm_mirror)** que protegeixi la informació davant la fallada d’un disc.

- **Instantànies (snapshots):**  
  Afegir **dos discos de 10 GB**, crear un volum (`lvm_dades`), formatar-lo i muntar-lo.  
  Afegir arxius al volum i crear un **snapshot (`lv_snapshot`)** per documentar com restaurar-lo en cas de dany del volum original.

- **Escalabilitat:**  
  Demostrar el procés d’ampliació utilitzant l’espai lliure dins del grup de volums per **ampliar el volum `lv_dades`**.

---

## 🪟 2. Part Windows: Espais d’Emmagatzematge (Storage Spaces)

S'ha d'utilitzar **Windows 11** per demostrar les configuracions possibles amb **Storage Spaces**.

### 🔧 Requisits de la implementació i demostració
- **Configuració inicial:**  
  Crear un **Storage Pool** amb **tres discos de 10 GB** (simulats).

- **Estudi de configuracions:**  
  1. **Resiliència de Mirall (Mirroring):**  
     - Utilitzar dos discos.  
     - Comprovar que ofereix alta disponibilitat.

  2. **Resiliència de Paritat (Parity):**  
     - Utilitzar els tres discos.  
     - Explicar la seva eficiència d’espai comparada amb el mirall.

  3. **Resiliència de Mirall Triple:**  
     - Afegir els discos de 10 GB necessaris per aconseguir un mirall triple.

- **Gestió i demostració:**  
  Mostrar com es visualitza l’estat dels discos i del pool des de la **consola de gestió de Windows**, demostrant la facilitat de manteniment.

---

## 🤝 Com treballareu i què lliurareu

El treball serà **en grup**.  
- Primer, us dividireu en dos equips:
  - Un equip resol la gestió en **Linux (LVM)**.  
  - L’altre en **Windows (Storage Spaces)**.
- Cada membre prepararà **individualment el guió** de la tasca (comandes, passos, documentació).
- Cada parella realitzarà la seva **demostració pràctica**.
- Finalment, el grup revisarà i unificarà la documentació abans de pujar-la al repositori.

📁 La documentació dels dos casos s’ha de fer en **format Markdown**, amb **imatges, explicacions i exemples**, dins una carpeta anomenada `tasca03`.

La carpeta ha d’incloure:

├── README.md → Descripció general de la tasca

├── linux_lvm.md

└── windows_storage_spaces.md
