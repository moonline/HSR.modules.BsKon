============================
FS14 BsKon Repetitionsfragen
============================


Antworten zu den Repetitionsfragen
==================================
Falls vorhanden befinden sich diese im GitHub Repository. Ergänzungen oder ganze Antwortensets sind jederzeit herzlich willkommen. https://github.com/moonline/HSR.modules.BsKon



Symbolerklärung
===============
**[DP]**
Wissensfragen des Dozenten (Slides) für die Prüfung

**[EW]**
Wissensfrage, die über den Stoff der Vorlesung hinaus geht.



1 E-/A Treiber
==============

**1.0.1.**
[DP] Was sind die Aufgaben der E-/A Verwaltung?

**1.0.2.**
Erklären Sie den Unterschied bei der Kommunikation zwischen Anwenderprozess und Geräten für Rechner mit und ohne Betriebssystem. 


1.1 Standardisierte E-/A Schnittstelle
--------------------------------------

**1.1.1.**
Wie werden Geräte identifiziert?

**1.1.2.**
Welche Nutzungsarten existieren? Welche Konsequenzen hat dies auf mehrfachen Zugriff?

**1.1.3.**
Welche Nutzungsmodelle gibt es?

**1.1.4.**
Erklären Sie wie die Standardisierte Schnittstelle "Abstraktes Gerät als virtuelle Datei" funktioniert und aufgebaut ist.

**1.1.5.**
Was ist die Ausgabedatenbasis? Welche Informationen liefert sie? Woher stammen diese Informationen?

**1.1.6.**
Welche drei Schnittstellen befinden sich zwischen Anwendungsprozess und Hardware bei einem Rechner mit BS?

**1.1.7.**
Was ist die Treiberschnittstelle? Wo befindet sich diese? Machen Sie eine Skizze.

**1.1.8.**
Was ist die Hardware Schnittstelle? Welche Aufgaben übernimmt sie?

**1.1.9.**
[DP] Wo findet die Software das Peripheriegerät, bzw. deren Adressraum?

**1.1.10.**
Erklären Sie den Spezialfall Peripheriebus.

**1.1.11.**
Wozu dient die Treibertabelle? Was ist die Kanalnummer?

**1.1.12.**
Erklären Sie die Treiberhierarchie. [DP] Wo würden Sie den zusätzlichen Peripheriebustreiber einfügen, bei Anschluss über standardisierten Peripheriebus?

**1.1.13**
Welche Treibervarianten gibt es? Erklären Sie jede Kategorie und deren Aufgaben.

**1.1.14.**
Erklären Sie "Synchronität der E/A aus Anwendungssicht" und "Synchronität der E/A aus Betriebssystemsicht".

**1.1.15.**
Was ist eine Treiberinstanz? Skizzieren Sie einen Treiber, der von drei Anwendungsprozessen genutzt werden, die auf zwei Geräte zugreifen.

**1.1.16.**
Skizzieren Sie den Zugriffsverlauf bei E/A mit und ohne Interrupt sowie bei paralleler Ausführung mehrer Treiberroutinen.

**1.1.17.**
Was ist eine Nachbearbeitungsroutine?

**1.1.18.**
Was sind Portable Treiber und wie wird das realisiert?

**1.1.19.**
[DP] Nennen Sie fünf wesentliche Komponenten der Ein-/Ausgabe(E/A)-Architekturveines Betriebssystems

**1.1.20.**
[DP] Nennen Sie je einen Vor- und Nachteil einer standardisierten E/A-Schnittstelle

**1.1.21.**
[DP] Erklären Sie, welche Aufgaben die Treiber in einem Betriebssystem erfüllen und wie sie sich in das Betriebssystem einfügen

**1.1.22.**
[DP] Erklären Sie drei wesentliche Synchronisationsprobleme beim Einsatz von Treibern und ihre mögliche Behebung erklären

**1.1.23.**
[DP] Erklären Sie die Begriffe Treiberschnittstelle, Treiberhierarchie, Treiberinstanz und Prozess-/Unterbrechungskontext erklären

**1.1.24.**
In welchen Kontexten läuft eine ISR? Wovon ist die abhängig? Welche Eigenschaften haben die unterschiedlichen Kontexte.

**1.1.25.**
Was passiert mit den Daten eines Hardwarezugriffs, dessen aufrufender Prozess schlafen gelegt wurde weil der HW-Zugriff länger dauert und in der Zwischenzeit ein anderer Prozess mit seiner Arbeit begonnen hat? Was passiert, wenn der 2. Prozess eine höhere Priorität als der 1. hat? Was wenn umgekehrt?

**1.1.26.**
Was ist zu beachten bei der parallelen Ausführung von mehreren Prozessen, die alle das gleiche HW Device verwenden?

**1.1.27.**
Wozu benötigt es ISR Nachbehandlungsroutingen?

**1.1.28.**
Was sind portable Treiber? Wie werden Sie geschrieben?


2 Linux Treiber
===============

**2.0.1.**
Welche Methoden gibt es für den Hardwarezugriff? Wie funktionieren sie?

**2.0.2.**
Wie unterscheiden sich Kernelmode Treiber von User Mode Treibern?

**2.0.3.**
Wie ist die E/A Schnittstelle unter Linux aufgebaut?

**2.0.4.**
Was sind Gerätedateien?

**2.0.5.**
Was bietet udev? Welches Problem löst es?

**2.0.6.**
Was für Treibertypen gibt es? Welche Datengrössen werden normalerweise geschrieben / gelesen?

**2.0.7.**
Was sind dynamische Treiber?

**2.0.8.**
Wie werden Treibermodule geladen, entladen?

**2.0.9.**
Was sind Built-in Treiber?

**2.0.10.**
Warum wird immer eine Gerätedatei benötigt? Muss der Treiber diese anlegen? Wo befinden sich Gerätedateien?

**2.0.11.**
Wozu dient die Initialisierungs- und Terminierungsroutine eines Treibers? Wie wird sie registriert?

**2.0.12.**
Skizzieren Sie einem minimalen Treiber, der sich registriert und auch wieder deregistriert werden kann.

**2.0.13.**
Erklären Sie, wie die fünf typischen Treiberaufgaben am Bessten gelöst werden und wofür die Aufgabe jeweils gebraucht wird:

a) Fortlaufend HW Status abfragen
b) Blockierendes Warten bei E-/A
c) Plug & Play / Powermanagement
d) Asynchrone E-/A
e) Datenaustausch mit App

**2.0.14.**
Wie benutzen Sie interrupts und wie melden sie eine ISR an?

**2.0.15.**
Gegeben sind die Elemente "Anwendungsprozess", "Systembibliothek für E-/A", "E/A Verwaltung", Treiber mit "Read Funktion", "Tasklet" und "Treiber ISR" sowie "System-ISR" und die "Hardware".
Machen Sie eine Skizze, wie der Kontrollfluss bei der Interrupt gesteuerten E-/A abläuft und benutzen Sie die oben genannten Bausteine.

**2.0.16.**
Mit welchen Prioritäten laufen ISR's, SoftIRQ und Threads ab? Welche Konsequenzen hat deren Priorität jeweils auf andere Prozesse? Durch welche Prozesse sind sie jeweils selbst unterbrechbar?

**2.0.17.**
Wozu dienen die Befehle init_waitqueue_head(), interruptile_sleep_on(), ait_event_interruptible() und wake_up_interruptible()?

**2.0.18.**
Warum kann es bei interruptile_sleep_on() zu einem Deadlock kommen? Was ist die Lösung dagegen?

**2.0.19.**
Welche Aufgabe übernehmen copy_to_user() und copy_from_user()? Was gibt es bei deren Benutzung zu beachten?

**2.0.20.**
Wie werden Konfigurationsparameter für einen Treiber zur Verfügung gestellt?

**2.0.21.**
Welche Ansätze gibt es, Synchronisationsprobleme beim Zugriff auf HW zu vermeiden?

**2.0.22.**
Welche Speziellen Anforderungen stellen Blockgeräte an einen Treiber? Was müssen sie anders implementieren bei einem Blockgerätetreiber?



3 Windows Treiber
=================

**3.0.1.**
Wie sieht die Windows Ein-/Ausgabe Architektur aus? Warum gibt es den "PnP manager" und den "User mode PnP Manager"? Wozu dient der I/O Manager? Wozu die WMI Services?

**3.0.2.**
Skizzieren Sie, wie WDM und WDF auf die Hardware aufbauen und welche Layer dazwischen sind.

**3.0.3.**
Wie wird die Peripherie abstrahiert?

**3.0.4.**
Erklären Sie den Unterschied zwischen WDM und WDF.


3.1 WDM
-------

**3.1.1.**
Wie funktioniert das WDM Objektkonzept? Was ist die Handletable und wie interagieren die Handletable, Dateiobjekt, Geräteobjekt, Treiberobjekt und Hardware? Was sind Auftagobjekte?

**3.1.2.**
Was ist ein Dateiobjekt? Wie ist es aufgebaut un wann wird es angelegt und entfernt? Was gibt es zurück?

**3.1.3.**
Was ist ein Dateiobjekt? Wie ist es aufgebaut und welche Daten enthält es?

**3.1.4.**
Was ist ein Ein-/Ausgabe-Anfrderungspaket IRP? Welche Informationen enthält es?

**3.1.5.**
Was ist ein Treiberobjekt? Was ist seine Aufgabe und welche Informationen enthält es?

**3.1.6.**
Skizzieren Sie den WDM Treiberstapel mit dem Auftragsdatenfluss.

**3.1.7.**
Wie ist die Plug-and-Play Hierarchie aufgebaut und wie funktioniert sie? Was ist ihre Aufgabe?


3.2 WDF
-------

**3.2.1.**
Was ist ein WDF Objekt?

**3.2.2.**
Wie ist das WDF Objektmodell aufgebaut? Welche Aufgaben übernimmt es?

**3.2.3.**
Wie ist ein Benutzermodustreiber aufgebaut? Wie interagiert er mit dem Kernmodus?

**3.2.4.**
Wie unterscheidet sich ein Kernmodustreiber von einem Benutzermodustreiber?

**3.2.5.**
Können Kernmodustreiber in C++ programmiert werden?

**3.2.6.**
Was für Standardbehandlungen stellt WDF zur Verfügung?

**3.2.7.**
Wie / ums was erweitert WDF WDM?

**3.2.8.**
Was sind FDO (Funktionales Geräteobjekt) und PDO (Physisches Geräteobjekt)

**3.2.9.**
Wie läuft die KMDF Auftragsverarbeitung ab?

**3.2.10.**
Wie ist ein minimler Treiber aufgebaut? Was muss er alles umsetzen?



4 Betriebsystemarchitekturen
============================

**4.0.1.**
In welchen Kontext wird das BS eher als Black Box und in welchem als White Box betrachtet?

**4.0.2.**
Welche Massnahmen wurden in der Vergangenheit unternommen um die Komplexität zu reduzieren?

**4.0.3.**
Nennen Sie einige Anforderungen an ein qualitatives gute BS.

**4.0.4.**
Was zeigt die statische Struktur eines BS? Welche Vorteile hat diese Ansicht?

**4.0.5.**
Was zeigt die dynamische Struktur eines BS? Welche Vorteile hat diese Ansicht?

**4.0.6.**
Nennen Sie drei Entwurfsregeln für BS.

**4.0.7.**
Erklären Sie den Unterschied zwischen "ungeregelten Aufrufbeziehungen" und "geregelten Aufrufbeziehungen" in einem BS.

**4.0.8.**
Nennen Sie drei mögliche Lösungen um die Probleme bei der Wahl einer guten Struktur zu lösen.


4.1 Architekturaspekte
----------------------

**4.1.1.**
Erklären Sie die Eigenschaften folgender Systeme:

a) Monolithisches System
b) Geschichtetes System
c) Mikrokernsystem

**4.1.2.**
Erklären Sie das Prinzip der End-zu-End Argumente. Wo bewährt es sich seit Jahrzehnten?

**4.1.3.**
Wie sind Erweiterbare Systeme aufgebaut? Welche Vorteile und Probleme bringen sie mit sich?

**4.1.4.**
Was sind sichere Systemerweiterungen?

**4.1.5.**
Erklären Sie das Konzept von Typensicheren Sprachlaufzeitsystemen. Welche Vorteil bringt dies? Wie funktioniert das Konzet der Schutzdomänen bei typensicheren SLZS? Auf welche drei Säulen stützt sich die Typensicherheit?

**4.1.6.**
Welche Vor- und Nachteile bringen typensichere SLZS?

**4.1.7.**
Wie funktionieren typensichere Maschinensprachen? Welche Vor- und Nachteile bieten sie?

**4.1.8.**
Was ist Certified Code (PPC)? Was ist TAL?

**4.1.9.**
Nennen Sie zwei Anforderungen an sicheren Code.

**4.1.10.**
Welche potentiellen Sicherheitsprobleme bietet Certified Code?

**4.1.11.**
Erklären Sie das Konzept der Systemobjekte.

**4.1.12.**
Wie sind Systemobjekte aufgebaut? Welche Informationen enthalten sie?

**4.1.13.**
Wie/Wann werden Systemobjekte abgeräumt?

**4.1.14.**
Erklären Sie grob den konzeptionellen Aufbau eines Unix, eines Sun Solaris und eines Windows 7.


4.2 MSR Singualarity
--------------------

**4.2.1.**
Was ist das MSR Singularity?

**4.2.2.**
Vergleichen Sie das MSR S. mit einer konventionellen Betriebsystemarchitektur, was ist anders?

**4.2.3.**
Was sind SIPs und HIPs? Welche Kombinationen gibt es?

**4.2.4.**
Wie funktioniert sicherer Datenaustausche zwischen SIPs?

**4.2.5.**
Was ist der Singularity Kernel?

**4.2.6.**
Wie werden die folgenden Probleme in MSR S. gelöst:

a) IPC per Nachricht gilt als ineffizient
b) Reflection ermöglicht Code Generation zur Laufzeit -> Umgehen der Validation

**4.2.7.**
Wie werden in MSR S. Applikationen "betrachtet"?

**4.2.8.**
Was sind die Benefits von MSR S.? Was wurde erreicht?

**4.2.9.**
Wie sind Systemarchitketur und E-/A System aufgebaut?



5 Multiprozessor- und Verteilte Betriebsysteme
==============================================

**5.0.1.**
Skizzieren Sie die vier Rechnerstrukturen.

a) Uniprocessor
b) Shared Memory Multiprocessor
c) Message Passing Multicomputer
d) Wide Area Distributed System

**5.0.2.**
Was ist ein Netzwerkbetriebsystem? 

a) Wie ist es aufgebaut? 
b) Wie sind die Applikationen verteilt? 
c) Wozu wird es eingesetzt? 
d) Vor- und Nachteile?

**5.0.3.**
Nennen Sie Aufbau, CPU Verteilung, Ort des Gemeinsamen Speichers, Applikationsverteilung sowie Vor- / Nachteile eines Unabhängigen, AMP und SMP Multiprocessing BS.

**5.0.4.**
Wie funktioniert ein Message Passing Multicomputer? Welche Verbindungstechniken gibt es? Welche Messaging Ansätze gibt es?

**5.0.5.**
Was ist Ortstransparenz?

**5.0.6.**
Wie sind Verteilte Systeme aufgebaut? Was sind Knoten? Nennen Sie Vor- und Nachteile.

**5.0.7.**
Wie funktioniert ein verteiltes System auf Middle-Ware Basis?

**5.0.8.**
Was ist GPGPU? Wo liegen Vor- und Nachteile?

**5.0.9.**
Was sind Hochleistungsrechner? Was bedeutet HPC und HTC?

**5.0.10.**
Was sind "Fluu Single System Solution" SSI?

**5.0.11.**
Was sind Cluster Systeme? Was zeichnet sie aus? Wie unterscheidet sich der Cluster vom SSI bezüglich Ortstransparenz?

**5.0.12.**
Was sind Mosix, Beowulf und Condor? Erklären Sie grob, nach welchen Prinzipien sie jeweils funktionieren.


5.1 Parallel Programmiermodelle
-------------------------------

**5.1.1.**
Erklären Sie, wie Shared Memory funktioniert. Probleme?

**5.1.2.**
Wie funktioniert Message Passing? Probleme?

**5.1.3.**
Was ist DSM? Wie wird es realisiert? Welchen Vorteil bringt die Replikation von entfernten Seiten? Welche Probleme bringt es mit sich? Wie wird die Seitengrösse ausgewählt?

**5.1.4.**
Was ist MPI? Wie funktioniert es? Welche Vor- und Nachteile bringt es mit sich?

**5.1.5.**
MPI Rechenbeispiel: Wie gross ist die Reduktion der Rechenzeit (ohne Overheadberücksichtigung) bei der Berechnung der Summe von 30 Zahlen auf 5 Prozessoren gegenüber 1 Prozessor?

**5.1.6.**
Was ist PVM? Wie funktioniert es? In welchen Umgebungen funktioniert es?

**5.1.7.**
Was ist OpenMP? Zeigen Sie, wie eine Schleife parallelisiert wird.


5.2 fos
-------

**5.2.1.**
Was ist fos? Was ist der Unterschied zwischen fos und einem klassischen BS?

**5.2.2.**
Wie wurde fos umgesetzt?

**5.2.3.**
Erklären Sie die Archiektur von fos.



6 Libraries
===========

**6.0.1.**
Was ist eine statische Bibliothek? Was eine Shared Library? Was eine dynamisch ladbare? Wo liegen die Vor- und Nachteile?


6.1 Linux Libraries
-------------------

**6.1.1.**
Wie sind externreferenzen auf Bibliotheken aufgebaut?

**6.1.2.**
Wie werden statische Biliotheken eingebunden?

**6.1.3.**
Wie weren statische Bibliotheken erzeugt?

**6.1.4.**
Wie sind datische Bibliotheken intern aufgebaut?

**6.1.5.**
Wie werden gemeinsame Bibliotheken erzeugt? Wie ist deren Namensschema aufgebaut?

**6.1.6.**
Wie werden Bibliotheken dynamisch gebunden?

**6.1.7.**
Wie sind gemeinsame Bibliotheken intern aufgebaut?

**6.1.8.**
Wie unterscheiden sich dynamsich ladbare Bibliotheken von gemeinsamen? Wie werden sie erzeugt?


6.2 Windows Libraries
---------------------

**6.2.1.**
Wozu werden DLL's unter Windows verwendet?

**6.2.2.**
Wie wird eine DLL erzeugt? Was passiert dabei und welche Inhalte werden generiert?

**6.2.3.**
Wie werden DLL's verwendet?

**6.2.4.**
Wie werden DLL's geladen wenn ein Programm gestartet wird, das eine DLL referenziert? Was passiert, wenn das Programm mehrfach gestartet wird?

**6.2.5.**
An welche Adresse werden DLL's geladen? Welche Probleme erzeugt dies? Wie wird das Problem zumindest ansatzweise gelöst?

**6.2.6.**
Was ist das DLL Rebasing?

**6.2.7.**
Wie werden DLL's implizit geladen? In welchem Pfad werden DLL's gesucht?

**6.2.8.**
Was ist die Exportliste und wie ist sie aufgebaut?

**6.2.9.**
Was ist die Importliste und wie ist sie organisiert?


7 Schedulingstrategien
======================

7.1 Posix Thread Scheduling
---------------------------

**7.1.1.**
Erklären Sie die Strategie des Posix Thread Scheduling.

**7.1.2.**
Welche Freiheitsgrade (Parameter) besitzt Scheduling auf Single- und Multicore Prozessoren?

7.2 Java Thread Scheduling
--------------------------

**7.2.1.**
Wie funktioniert das Java Thread Scheduling? Welche Thread Prioritäten gibt es?

**7.2.2.**
Warum sollten Applikationen im Bedarfsfall von Round-Robin yield benutzen?

**7.2.3.**
Wie sieht das Thrad Zustandsmodell aus?


7.3 Windows Scheduling
----------------------

**7.3.1.**
Wie funktioniert das Scheduling unter Windows? Wie sind die Prioritäten aufgebaut?

**7.3.2.**
Warum sollten die Prioritätsklassen High und Real-Time mit Bedacht verwendet werden?

**7.3.3.**
Mit welchen Befehlen können Windows Prioritäten und Klassen gesetzt werden?

**7.3.4.**
Welche Thread Zustände gibt es unter Windows?

**7.3.5.**
Wie funktioniert die Zeitquantumverwaltung?

**7.3.6.**
Welche Automatismen zur Prioritäts- und Quantumanpassung gibt es?


7.4 Unix Scheduling
-------------------

**7.4.1.**
Wie funktioniert klassisches Unix scheduling? Welche Prozess Zustände gibt es?

**7.4.2.**
Wie ist das Prioritätsschema aufgebaut?

**7.4.3.**
Wann erfolgt eine dynamische Prioritätsanpassung?

**7.4.4.**
Wie funktioniert modernes Linux Scheduling?


7.5 Multi Prozessor Scheduling
------------------------------

**7.5.1.**
Welche zusätzlichen Scheduling Entscheidungen müssen getroffen werden?

**7.5.2.**
Wie unterscheiden sich lose gekoppelte MP Systeme von eng gekoppelten? Welche Scheduling Strategien werden angewandt?

**7.5.3.**
Wie ist MP Scheduling unter Linux und Windows implementiert?



8 Android
=========

**8.0.1.**
Skizzieren Sie grob die Architektur von Android.

**8.0.2.**
In welchem Kontext läuft eine App? Unter welchem User? Auf welche Daten darf sie zugreifen? 
Wann terminiert ihr Prozess?

**8.0.3.**
Die Libraries sind in C++ geschrieben. Wie kommuniziert Java mit den Libraries?

**8.0.4.**
Welche zusätzlichen Komponenten besitzt der Android Kernel gegenüber einem normalen Linux Kernel?

**8.0.5.**
Beschreiben Sie die VM, die auf Android läuft. Wie unterscheidet sie sich von der normalen JVM?

**8.0.6.**
Was passiert beim Starten von Android?

**8.0.7.**
Was passiert beim Starten einer App? Von welchem Prozess erben Apps?

8.1 Apps
--------

**8.1.1.**
Was enthält eine einfache App mindestens?

**8.1.2.**
Was steht im Manifest? Was sind Angaben wie "@string/app_name" im Manifest?

**8.1.3.**
Was sind Activities und Fractions?

**8.1.4.**
Wie eng sind Apps gekoppelt? Wie werden Daten ausgetauscht?

**8.1.5.**
Erklären Sie den Activity Livecycle. Bei welchem Event sollten Sie Daten persistieren, damit sie in jedem Fall persistiert wurden? Warum?

**8.1.6.**
Was ist der Back-Stack? Was passiert beim Starten einer neuen Activity? 
Was passiert beim drücken des Back-Buttons? Was beim Drücken des Home-Buttons?

**8.1.7.**
Wie übergeben Sie Resultatdaten von einer Activity an eine Andere?

**8.1.8.**
Was sind Shared Preferences?


8.2 Komponenten
---------------

**8.2.1.**
Was ist ein Intent und wie erzeugen sie einen neuen? Erklären Sie den Unterschied zwischen explizitem und implizitem Intent.

**8.2.2.**
Wie geben sie einem Intent Daten und Extras mit?

**8.2.3.**
Welche Prozesse werden als erstes Beendet, wenn der Speicher knapp wird?

**8.2.4.**
Was ist AsyncTask? Wie starten sie einen Task?

**8.2.5.**
Was sind Services? Wie registrieren und erzeugen sie einen neuen Service?

**8.2.6.**
Was ist der Unterschied zwischen gebundenen und ungebundenen Services?

**8.2.7.**
Wie sieht der Service Livecylce aus?

**8.2.8.**
Was ist ein Intentservice?

**8.2.9.**
[DP] Wie erhält eine Activity das Resultat von einem Service?

**8.2.10.**
Was ist der Broadcast receiver? Wie registrieren und empfangen sie Messages?

**8.2.11.**
Auf welche Arten können sie Daten persistieren? Nennen Sie die Vor- und Nachteile der einzelnen Varianten.

**8.2.12.**
Was sind Content Provider und was können sie damit machen?



9 Windows Phone
===============

**9.0.1.**
Sind WP7 Apps unter 8 lauffähig obwohl 8 einen neuen Kernel bringt? Warum? Laufen WP8 Apps unter WP7?

**9.0.2.**
Sind WP8 Apps unter Win8 einsetzbar? 

**9.0.3.**
Was sind Tiles? Was können sie?

**9.0.4.**
Welche Möglichkeiten gibt es um Apps zu schreiben?

**9.0.5.**
Wie unterscheidet sich das Memory Management von Win8 und 8.1?

**9.0.6.**
Was beinhaltet das Manifest?

**9.0.7.**
Skizzieren Sie den Livecylce einer App.

**9.0.8.**
Bei welchem Event sollten sie Daten persistieren?

**9.0.9.**
Warum müssen auch bei der App Deaktivierung Daten persistiert und zusätzlich der UI State gesichert werden?

**9.0.10.**
Was ist der App Zustand Dormant? Was ist Tombstoned?

**9.0.11.**
Was pasiert beim Aktivieren einer App?

**9.0.12.**
Was ist das State Directory?


9.1 Navigation
--------------

**9.1.1.**
Auf welche zwei Arten kann ein Page Wechsel umgesetzt werden?

**9.1.2.**
Welche Events werden ausgelöst, wenn die Page geladen oder verlassen wird und wenn der Back-Button gedrückt wird?


9.2 Persistenz
--------------

**9.2.1.**
Was sind local storage und isolate storage?

**9.2.2.**
Was ist das Application Settings Directory? Wie laden und speichern sie Daten?

**9.2.3.**
Was ist der Runtime Storage?


9.3 Launcher & Chooser
----------------------

**9.3.1.**
Was sind Launcher? Machen Sie ein Paar Beispiele.

**9.3.2.**
Was sind Chooser? Kann eine App direkt auf das Telefonbuch zugreifen?


9.4 Asynchrone Ausführung
-------------------------

**9.4.1.**
Wie können sie mit async und await eine Funktion asynchron ausführen?


9.5 MVVM
--------

**9.5.1.**
Erklären Sie das MVVM Pattern. Welchen Vorteil bietet es?



10 iOS
======




11 Firefox OS
=============

**11.0.1.**
Erklären Sie die Architektur von Firefox OS. Erklären Sie die Aufgaben der einzelnen Layer.

**11.0.2.**
Was für Prozesse werden von Firefox OS gestartet? Wann werden neue Prozesse gestartet? 
Wie wird kommuniziert?

**11.0.3.**
Wie werden Threads priorisiert/verwaltet?

**11.0.4.**
Was ist die WebAPI? Was stellt sie zur Verfügung? Wie ist der Zugriff auf die API's geregelt?

**11.0.5.**
Erklären Sie das Security Konzept von FxOS.

**11.0.6.**
Was sind Web Activities?

**11.0.7.**
Wie wird eine App UI für FxOS geschrieben?






