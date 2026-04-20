# ProiectTSC2026

# InkTime Smartwatch PCB


# Descriere generala

Proiectul consta in realizarea unei scheme electronice si a unui PCB pentru un sistem embedded compact, utilizand Autodesk Fusion 360 Electronics.

Scopul a fost integrarea componentelor hardware necesare (microcontroller, interfete de comunicatie, alimentare si periferice) pe o placa compacta, respectand constrangerile electrice, mecanice si regulile de good practice impuse in cadrul laboratorului.


# Pasii de implementare
!. Analiza cerintei si a schemei date
identificarea componentelor principale
intelegerea conexiunilor dintre module
2. Realizarea schemei electrice
conectarea corecta a tuturor componentelor
verificare ERC
3. Plasarea componentelor pe PCB
gruparea componentelor in jurul IC-urilor principale
respectarea constrangerilor mecanice
4. Rutarea PCB-ului
trasee de putere dimensionate corespunzator
evitarea unghiurilor de 90°
utilizarea via-urilor pentru zone aglomerate
5. Plan de masa (GND)
realizarea polygon-urilor pe ambele layere
conectarea prin via stitching
6. Verificare finala
DRC check
corectarea erorilor critice

# Diagrama bloc


#Componente principale:
Microcontroller (unitatea centrala)
Senzori / periferice
Modul comunicatie (SPI / I2C / UART)
Sistem alimentare
USB (alimentare + debug)

# Conectari:

I2C pentru senzori
SPI pentru periferice rapide
UART pentru debug
Alimentare distribuita prin regulator


# Functionalitate hardware

Microcontroller-ul gestioneaza toate interfetele si perifericele.

Comunicatia cu senzorii → I2C
Comunicatia cu periferice → SPI
Debug → UART

Alimentarea este realizata prin USB sau sursa externa si distribuita catre toate modulele prin circuitul de power.


# Layout PCB

# PCB-ul a fost realizat pe 4 layere:

TOP: componente + rutare principala + ground
BOTTOM: cablare componente
ROUTE2: -
ROUTE63: in principal cabluri pentru power

# Reguli respectate:
trasee de putere mai groase
trasee de semnal = 0.15 mm
fara unghiuri de 90°
condensatori de decuplare aproape de pini
verificare DRC
plasare componente strategic


# Probleme intampinate
erori DRC
spatiu limitat pentru rutare
trasee apropiate in zone aglomerate
dificultati in plasarea componentelor
dificultati in conectarea componentelor prin cablu
aglomerarea componentelor intr-un loc

Solutii aplicate
refacerea rutarii in zone critice
utilizarea via-urilor pentru escape routing
optimizarea plasarii componentelor
adaugarea planurilor de masa
modificarea pozitiei componentelor


# Decizii de design

Conform cerintelor proiectului, au fost luate urmatoarele decizii:

au fost acceptate unele zone unde traseele sunt apropiate de limita DRC
in zone aglomerate s-au folosit via-uri pentru a scoate semnale
unele rutari nu sunt ideale, dar respecta regulile de fabricatie
via stitching a fost aplicat doar in zone relevante
layout-ul a fost optimizat pentru spatiu, nu perfect simetric

Aceste decizii au fost necesare pentru a finaliza design-ul fara a compromite functionalitatea.

# Hardware

Schematicul si PCB2D


# Mechanical

Modelul 3D include:
PCB
baterie
display
carcasa


# Images

imagini ale placutei 2D si 3D plus poze cu componentele asamblate si exploded


#Concluzie

PCB-ul realizat respecta majoritatea regulilor de proiectare si cerintele impuse.

Design-ul este functional, verificat DRC si pregatit pentru fabricatie, chiar daca au fost necesare unele compromisuri in zonele aglomerate.
