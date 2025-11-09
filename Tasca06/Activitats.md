# Aqui trobarem el video de DNS:

[Carpeta del video](https://drive.google.com/drive/folders/1j7e303m7YcG7aFf4nYoFpKtBzrLM6K8-?usp=drive_link-) 

# Fase Pràctica: Diagnosi de Noms (Auditoria amb CLI)**


## Comanda 1: Consulta Bàsica de Registre A**  
     
  Executa dig xtec.cat A  

<img width="566" height="368" alt="Captura de pantalla 2025-10-27 200946" src="https://github.com/user-attachments/assets/83447cc3-a578-4541-aefb-c3df46ecf475" />

	    
## Comanda 2: Consulta de Servidors de Noms (NS)**

	Executa dig tecnocampus.cat NS

<img width="590" height="189" alt="Captura de pantalla 2025-10-27 202342" src="https://github.com/user-attachments/assets/ba004cbd-2878-473d-a609-4b0cd26ac243" />


## Comanda 3: Consulta Detallada SOA**

	Executa dig escolapia.cat SOA

<img width="1013" height="439" alt="Captura de pantalla 2025-10-27 211841" src="https://github.com/user-attachments/assets/3046408c-33ec-4223-a78f-583470108d08" />


## Comanda 4: Consulta resolució inversa**

	Executa comanda dig \-x 147.83.2.135

<img width="615" height="178" alt="Captura de pantalla 2025-10-27 212143" src="https://github.com/user-attachments/assets/f050dd0e-2004-4cb0-9529-39aec4c95aeb" />


El registre que s’obté és de tipus **PTR**, utilitzat per la resolució inversa (IP → nom).


# Comprovació de Resolució amb nslookup (Multiplataforma)


## Comanda 1: Consulta Bàsica no Autoritativa**

<img width="302" height="271" alt="Captura de pantalla 2025-10-30 153302" src="https://github.com/user-attachments/assets/36fa9cbc-8eb8-49d4-92ba-4ed93f17a435" />


La informació prové directament del servidor de noms autoritatiu del domini (ns.tecnocampus.cat, per exemple).

## Comanda 2: Consultes autoritatives**

  * Escriure *server IP* i escriure la IP del primer servidor de noms del domini tecnocampus.cat que s’ha obtingut d’una consulta anterior. A continuació, indiqueu que voleu consultar registres de tipus A i del domini tecnocampus.cat  
  * Anàlisi: Quines diferències s’observen a la resposta obtinguda amb la comanda 1?

<img width="250" height="56" alt="Captura de pantalla 2025-10-30 165415" src="https://github.com/user-attachments/assets/2ec84e00-617c-4022-9fd8-55c93a649d7f" />


<img width="579" height="429" alt="Captura de pantalla 2025-10-30 165714" src="https://github.com/user-attachments/assets/2995bf3a-f2c8-438d-9feb-5e74c46944a7" />
