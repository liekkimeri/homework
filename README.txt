Ohjelman on tehty k�ytt�en asp.net wep api ja entity framework

Luo homework niminen tietokanta ja luo siihen tarvittavat taulut ajamalla tietokanta skripti taulujenLuonti.sql

Avaa visual studio projektti Homework.sln

K�y muuttamassa tiedostosta Web.config connectionStringinst� data source vastaamaan sinun tietokanta instanssin nimi�.

Sitten ohjelma pit�isi olla k�ytt�valmis.

Rest serveri� toimintaa kannattaa testata Postman -nimesell� ohjelmalla, jonka voi ladata chrome web storesta.

Esimerki komentoja
 
DELETE  /api/DeletePlanet/3 --poista planetan id perustella
GET     /api/GetPlanet/2 --hakee planetaan tiedot id perustella
GET /api/GetPlanets --palauttaa kaikki planetat
POST /api/PostPlanet bodyn raw teksiksi {"Name":"unknown"} ja l�hetys muodoksi JSON --lis�� unkown nimisen planeetan
PUT /api/PutPlanet/4 bodyn raw teksiksi {"ID":4,"Name":"Yoda's land" } ja l�hetys muodoksi JSON -- muokkaa lajia, jonka ID on 4


DELETE  /api/DeleteSpecies/3 --poista lajin id perustella
GET     /api/GetSpecies/2 --hakee lajin tiedot id perustella
GET /api/GetSpecies --palauttaa kaikki lajit
POST /api/PostSpecies bodyn raw teksiksi {"Name":"testi", "Planet_ID":4} ja l�hetys muodoksi JSON --lis�� testi nimisen lajin joka asuu planeetalla jonka ID on 4
PUT /api/PutSpecies/4 bodyn raw teksiksi {"ID":4, Name":"Yoda's species", "Planet_ID" : 4 } ja l�hetys muodoksi JSON -- muokkaa lajia, jonka ID on 4