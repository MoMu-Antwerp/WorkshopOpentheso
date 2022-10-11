# Installatie

Opentheso is een webapplicatie. Dit wil zeggen dat de software op een server moet geinstalleerd worden alvorens deze beschikbaar is binnen je eigen webbrowser. Je kan wel lokaal, op je eigen pc een webserver simuleren, maar dat is niet zo eenvoudig als het installeren van 'gewone' software.

Om praktische redenen maken we in deze workshop gebruik van een vooraf ingerichte web-omgeving. Logingegevens worden op de dag zelf gegeven, de omgeving zelf zal nadien offline gehaald worden

Als je thuis, lokaal aan de slag zou willen, kan je proberen de officiële instructies op https://opentheso.hypotheses.org/3241 te volgen, maar deze zijn technisch vrij complex.

De makkelijkste manier is om gebruik te maken van een docker container, maar ook het installeren van Docker en het gebruik ervan, zeker binnen een Windows omgeving, is best wel een technische uitdaging...

Voor wie toch nog moed heeft, is hier een methode die relatief haalbaar is:

## Lokale (test)installatie

Een lokale test installatie opzetten kan het makkelijkst door gebruik te maken van bijvoorbeeld de dockerfile die meemoo op github heeft voorzien:
https://github.com/viaacode/opentheso2-docker

ALs je Docker al probleemloos hebt geïnstalleerd op Windows of Linux, kan je meteen naar stap 5 en zullen stap 7-8 overbodig zijn.
Als je Linux als operating system hebt, kan je stappen 1-3 overslaan en zal je het ip adres in stap 7 vervangen kunnen worden door localhost.

1. Virtualbox installeren https://www.virtualbox.org/wiki/Downloads
2. ubuntu server image (.iso) downloaden https://ubuntu.com/download/server
3. virtualbox machine met ubuntu opstarten

  ![settingsVirtualBox](https://github.com/MoMu-Antwerp/WorkshopOpentheso/blob/main/images/virtualbox_machine.bmp)

  ![settingsVirtualBox](https://github.com/MoMu-Antwerp/WorkshopOpentheso/blob/main/images/virtualbox_machine_bridgednetwork.bmp)

4. Start de virtuele machine en volg de installatieinstructie (commandline). Kies voor alles de default waardes en creëer een gebruiker/wachtwoord. Bij één van de laatste stappen krijg je de optie om onder andere Docker te installeren. Selecteer Docker, volg de laatste stappen en herstart de machine + log in.

  Wat verder volgt zijn commando's die je via commandline moet ingeven:

5. docker container downloaden ```git clone https://github.com/viaacode/opentheso2-docker```
  daarna veranderen naar de nieuwe directory
  ```cd opentheso2-docker```

  > voor gevorderden: Je kan indien gewenst de Dockerfile (opentheso versie), docker-compose.yml (poort en volume) en de preferences.properties (taal etc.) met een teksteditor (nano of vim) aanpassen naar eigen wens.

6. docker container uitvoeren ```docker compose up``` of als dat niet werkt ```docker-compose up```
  Normaal gezien worden nu alle installatie commando's uitgevoerd. Wacht tot dat dit is afgelopen.
7. ip adres van virtualbox achterhalen

  ```sudo apt install net-tools```

  ```ifconfig``` Eén van de ip adressen zal bereikbaar zijn via je browser, gebruik dit in de volgende stap. Alternatief: ```curl -4 icanhazip.com```

8. Surf naar deze url in je browser (vervang 'ipadres' door het ip uit vorige stap) http://ipadres/opentheso2 of http://localhost/opentheso2


Als alles goed verlopen is zie je nu het opentheso beginscherm.
Default Logingegevens zijn admin/admin

> volgende: [basis functionaliteiten](https://github.com/MoMu-Antwerp/WorkshopOpentheso/blob/main/basics.md)
