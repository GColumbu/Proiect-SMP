	Driving racing game

	Indiferent ca esti in metrou, in masina sau pe scarile facultatii asteptand nota la un examen important, intotdeauna putem
lua o mica pauza pentru a ne relaxa si a uita putin de probleme cu un joc interactiv si simplu. Desi acest lucru este cam greu de 
realizat in cadrul proiecului de fata din cauza componentelor hardware, scopul acestuia ramane neschimbat. Scopul jocului este de a 
manevra masina pentru a trece si a supravietuii cat mai mult in fata traficului care se apropie rapid. Aproape ca un pilot de formula 1,
jucatorul poate trece de pe o banda pe alta pentru a face acest lucru cu ajutorul unui buton care este special configurat pentru aceasta
functionalitate.

	Din cauza limititudinii componentelor hardware, grafica jocului este una cat se poate de simpla, in care masinile sunt reprezentate
cu # iar masina pe care utilizatorul o controleaza cu 0.

	Componente hardware:
	Arduino Uno:
		Arduino UNO constituie o platforma de procesare tip open-source, bazata pe un software si hardware flexibil construita in 
		jurul unui microcontroler ATMEGA 328P-PU capabila de a prelua date printr-o serie de senzori conectati la pinii placii si 
		de a actiuna asupra altor dispozitive ca LED-uri, motoarelor, servomotoare, sau alte tipuri de dispozitive mecanice pe baza 
		unor comenzi cuprinse in codul scris intr-un limbaj de programare, similar cu limbajul C++ incarcat in memoria 
		microcontrolerului.  
	LCD:
		LCD-ul poate sa afiseze 16  caractere pe 2 randuri, are backlight de culoare albastra, si dispune de un backpack I2C care
		permite conectare la Arduino folosind doar 2 fire. Dispune de 8 adrese distincte, ceea ce inseamna ca poti comanda pana 
		la 8 LCD-uri folosind doar doi pini Arduino. Iar pentru a se seta adresa, se seteaza cei trei jumperi de pe spatele placii
		(sau doar o parte din ei). 
	Rezistenta 10kOhm
	Push Button

	Implementare:

	Implementarea este una cu caracter simplist, de asemenea logica jocului nu este una complicata, pentru a pastra simplitatea si robustetea 
	jocului."Harta" jocului este reprezentata ori de stringul typea sau typeaa ambele avand acelasi numar de elemente, dar cel din urma o
	dificultate mai redusa. De asemenea vectorul de int typeA si typeAA ne ajuta sa tinem minte indexurile tuturor obstacolelor din stringul
	hartii.

	Urmeaza setarea si definirea pinilor, in functia setup() unde de asemenea suntem intampinati cu mesajul "Start Game". Functia loop()
	are rolul principal de a schimba afisajul lcd-ului, mutand elementele din harta (typea), pentru a imita caracterul fluid al jocului.
	De asemenea se tine cont si de pozitia jucatorului (pos), pentru a schimba corect si a trata cazurile in care jucatorul pierde sau 
	castiga. Aceste cazuri sunt tratate in functiile gameover() si winner.

	In final am mai implementat functia button_press, care are unicul rol de a prelua inputul de la utilizator prin apasarea push button-ului
	si de a printa caracterul 0 (masina) pe diferite linii ale lcd-ului.

	Concluzie:

	In concluzie, consider ca chiar daca logica si implementarea jocului nu este una de dificultate ridicata, scopul jocului este indeplinit,
	fiind un joc interactiv si distractiv, pentru a uita de stresul si problemele vietii de zi cu zi.