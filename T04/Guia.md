# GUIA LDAP

**Per Començar instal·lem LDAP**

![image](./img/1.png)


**Seguidament haurem de posar una contrasenya per l'usuari ADMIN**

![image](./img/2.png)


**Ara mirem el status**

![image](./img/3.png)


**Amb sudo slapcat comprovem que els directoris s'hagin creat amb el nom que volem**

![image](./img/4.png)


**Configurem LDAP**

![image](./img/6.png)


**Introduim el nom del domini DNS**

![image](./img/7.png)


**Posem el nom de la organtizació**

![image](./img/8.png)


**Posem la contrasenya de l'administrador**

![image](./img/9.png)


**Un cop acabem diem que si la següent pestanya**

![image](./img/10.png)


**També configurarem de forma correcte el hostname**

![image](./img/sudo%20nano%20etc%20hosts.png)

![image](./img/panel.png)


**A continuació instalarem el manager de comptes de LDAP**

![image](./img/13.png)


**Afegim usuaris i grups**

![image](./img/1..png)

![image](./img/2..png)


**Ara canviem la configuració**

![image](./img/3_users.png)

![image](./img/3_groups.png)


**Utilitzarem "ldapsearch"**

![image](./img/4..png)


**Afegim admin a la llista**

![image](./img/lam1.png)


**Ara ja podem entrar a la compte**

![image](./img/111.png)


**Crearem dos Grups i dos Usaris**

![image](./img/222.png)

![image](./img/333.png)

![image](./img/444.png)


**Ara configurem el nom del client**

![image](./img/555.png)


**Comprovem que els noms funcionen correctament**

![image](./img/777.png)^


**Ara instal·lem els moduls necessaris**

![image](./img/888.png)


**Ara els configurem**

![image](./img/999.png)

![image](./img/1000.png)

![image](./img/1001.png)

![image](./img/1002.png)

![image](./img/1003.png)

![image](./img/1004.png)

![image](./img/1005.png)


**Cambiem la configuració de l'arxiu /etc/nsswitch.conf**

![image](./img/1006.png)


**També modifiquem l'arxiu /etc/pam.d/common-password**

![image](./img/1007.png)


**I també modifiquem l'arxiu /etc/pam.d/common-session**

![image](./img/1008.png)
