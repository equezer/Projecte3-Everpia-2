# 

# **T04: Serveis de directori. LDAP**

1. Requeriments d'Infraestructura Inicial



2. ### **Tasques d'Implementació i Configuració del Servidor LDAP**



3. #### **Gestió i Administració (LAM)**

 
—



—



### **4\. Integració de Client (Client Ubuntu Desktop)**




Comprovar la connectivitat amb el servidor fent una consulta **ldapsearch** des del client.

- Modificar els arxius de configuració del client necessaris. S'han de mostrar **clarament els canvis realitzats** en el codi dels arxius.

Configurem l'arxiu **nsswitch.conf** per indicar que s'usarà Idap per usuaris i grups.



  
A l'arxiu /etc/pam.d/common-password, eliminem a la línia el terme use\_authtok.



Ara editem l'arxiu **/etc/pam.d/common-session** i afegim la línia indicada per crear els perfils.





reiniciem el servei amb la comanda **systemctl restart nscd**



Comprovem que veu els usuaris LDAP



ara editem l’arxiu **/etc/pam.d/gdm-launch-enviroment**



Ara canviem d’usuari a **manager01** amb la contrasenya assignada anteriorment al admin de Lam que en el meu cas es: **1234**



Un cop iniciem sessió, comprovem com se li ha creat la carpeta personal i comprovem l'usuari.

