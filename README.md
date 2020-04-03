## Programmering 2 - Google Drive Sync

Instruktioner för prog2-projektet Google Drive Sync (läsår 19/20). I detta dokument återfinns instruktioner och tips för hur du implementerar olika klasser som kommer ingå i applikationen. Informationen kommer uppdateras löpande under projektets gång.

### Designmönster Model-View-Controller 

Ett designmönster (design pattern) är ett standardrecept som kan användas för att lösa olika programmeringsproblem. Vi kommer att bygga vår applikation enligt MVC, vilket innebär att vi delar in programmets funktionalitet i tre övergripande kategorier:

  * Model - klasser som hanterar all data som applikationen behöver hantera (även konfiguration)
  * View - klass eller klasser som hanterar användargränssnitt, GUI
  * Controller - i regel en klass som fungerar som ett gränssnitt mellan model och view
  
  ![MVC](https://hackernoon.com/drafts/126z19ld.png)
  
Läs på mer om MVC här: [https://www.guru99.com/mvc-tutorial.html](https://www.guru99.com/mvc-tutorial.html)

### klassen FileObserver

FileObserver har som uppgift att bevaka en vald mapp (och dess underliggande mappar) efter förändringar i filsystemet. Klassen initieras med argumentet `target_directory` som är absolut sökväg till bevakad mapp. Ändringar tillhandahåller tre olika listor (datatyp Array) @changed_files, @new_files, @deleted_files. 
