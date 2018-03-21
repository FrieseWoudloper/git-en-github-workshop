Je gaat nu een nieuwe repository aanmaken. Dit gaat in twee stappen.   
Eerst maak je de remote repository aan op GitHub. Vervolgens maak je een lokale kopie op je computer.     
Wijzigingen voer je eerst door op je lokale kopie en 'push' je dan naar de remote repository op GitHub.

## Stap 1: GitHub repository aanmaken
   
Ga naar https://github.com/jouwGebruikersnaam
   
Zorg er voor dat je bent ingelogd op GitHub.
   
Klik op het plus-teken in de rechter bovenhoek.  
Kies in het menu voor **New repository**.  
   
<img alt="New repository" src="images/new-repo-menu.png" width="300" />
   
Geeft de nieuwe repository een naam en omschrijving.  
Maak de repository openbaar (**public**).  
Vink de volgende optie aan: **Initialize this repository with a README**.  
Klik vervolgens op **Create repository**. 
   
   
<img alt="Create a new repository" src="images/new-repo-config.png" width="600" border="1" />
   
   
Je hebt zojuist je eerste GitHub repository aangemaakt :-)
   
   
<img alt="My first repo" src="images/my-first-repo.png" width="600" border="1" />
   
   
## Stap 2: Lokale kopie aanmaken

Open Git Bash in Windows of open een Terminal op je Mac.  
Navigeer naar de map waar je de repository wilt opslaan.   
Gebruik hiervoor het commando `cd`.   

Bijvoorbeeld:
`$ cd "D:/Jouw map naam"` (Windows)
`cd ~/jouw_map_naam` (MacOS)

Check de hyperlink naar de remote repository die je in de vorige stap hebt aangemaakt op GitHub.   
Die hyperlink is als volgt opgebouwd: https://github.com/jouwGebruikersnaam/jouwRepositorynaam.git.   
Je kunt de hyperlink eenvoudig kopiëren in de webpagina van jouw GitHub repository.   
Klik op **Clone or download** en kopieer de hyperlink die vervolgens getoond wordt.   

<img alt="Copy to clipboard" src="images/new-repo-url.png" width="300" />
   
   
Ga terug naar de command line (Git Bash of Terminal).   
Kopieer de remote repository naar je lokale computer met het volgende commando:   

`$ git clone https://github.com/jouwGebruikersnaam/jouwRepositorynaam.git`   

NB de git commando's zelf zijn identiek in Git Bash en in Terminal.
   
<img alt="Clone my first repo" src="images/new-repo-clone.png" width="400" />

## Stap 3: Wijzigingen doorvoeren in de repository

Je kunt nu de lokale repository aanpassen.   
Je kunt mappen aanmaken en bestanden toevoegen.   
Hiervoor kun je gewoon de Verkenner of andere programma's gebruiken.   

Het is ook slim om de README.md aan te passen.   
De inhoud van dit bestand wordt namelijk getoond aan bezoekers van de webpagina van je GitHub repository.   
Dan is het handig als de README.md wat meer informatie bevat over de inhoud van de repository.   

README.md is een Markdown bestand.   
Markdown is net als HTML een taal voor het opmaken van webpagina's, maar dan een stuk eenvoudiger.   
Klik hier voor een [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).   

Open de README.md in een teksteditor en pas de inhoud aan.   
Voeg eventueel een map en wat nieuwe bestanden toe aan je lokale repository.  

Ga terug naar de command line.   
Navigeer naar de lokale repository.   

`$ cd "D:/Jouw map naam/Jouw repository naam"`

Vraag een overzicht op van de veranderingen in de repository ten opzichte van de vorige commit.   
Dit doe je met behulp van het volgende commando:

`$ git status`
   
   
<img alt="Status before commit" src="images/new-repo-status.png" width="400" />

In het rood zie je de wijzigingen.
Zorg er voor dat alle wijzigingen worden klaargezet voor de commit:
    
`$ git add -A`
   
Voer nogmaals het `git status` commando uit om te verifiëren dat alle wijzigingen worden meegenomen in de commit.
   

<img alt="Status after add" src="images/new-repo-status-after-add.png" width="400" />   
   
    
Voer nu een commit uit. Hiermee maak je de wijzigingen definitief.   
Geef tussen de aanhalingstekens een korte beschrijving van de aard van de wijzigingen.
   
`$ git commit -m "Mijn eerste aanpassingen"`
   

<img alt="Commit" src="images/new-repo-commit.png" width="400" />   
   
    
Voer nogmaals het `git status` commando uit.   
Merk op dat je nu een melding krijgt dat je lokale repository voorloopt op de remote.
   

<img alt="Status after commit" src="images/new-repo-status-after-commit.png" width="400" />   
      
   
Je kunt nu nog meer bestanden aanpassen of toevoegen.   
Vergeet niet om iedere keer een `git add` en `git commit` commando uit te voeren om de wijzigingen definitief te maken en klaar te zetten voor de remote repository!
 
Als je zo ver bent, kun je alle commits van de lokale repository naar de remote repository op Github pushen:
   
`$ git push`
   

<img alt="Push" src="images/new-repo-push.png" width="400" />   

Voer nog een laatste maal het `git status` commando uit.   
Merk op dat de lokale en remote repository weer met elkaar synchroon lopen.
   

<img alt="Status after push" src="images/new-repo-status-after-push.png" width="400" />    
   

Controleer of de remote repository op Github is aangepast.

[Volgende](4-bijdragen-aan-een-repository-van-een-ander.md)
