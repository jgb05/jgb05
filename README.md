# Practica 1 -  ALGORÍTMICA I COMPLEXITAT

## L'illa de les hormones
Joel Gallart i Unai Celaya


### Execució
python illa.py [fitxer_entrada] [fitxer_sortida]



## Característiques
Gestió d'entrada: El script llegeix dades des d'un fitxer proporcionat com a argument de línia de comandes o des de l'entrada estàndard.

Detecció de cicles: Identifica i gestiona els cicles en les relacions.

Càlcul de l'ordre: Determina l'ordre dels participants basat en les relacions d'enemics i amics.

Sortida: Imprimeix la solució a la sortida estàndard i, opcionalment, la guarda en un fitxer.
### Funcionament de la solució

El programa utilitza un algorisme per resoldre el problema de l'ordre de col·locació basat en les relacions d'enemics i amics. A continuació es detalla el funcionament pas a pas de la solució:

1. **Lectura de les Relacions**:
   El programa llegeix un conjunt de relacions, on cada línia conté tres noms: una persona, el seu enemic i el seu amic. Aquestes relacions es guarden en un diccionari anomenat `relations`.

2. **Cerca d'un Cicle**:
   A partir del primer nom de la llista de persones, el programa busca si existeix un cicle en les relacions. Això es fa seguint les relacions de les persones fins que es troba una persona que ja ha estat visitada. Quan es troba un cicle, es determina quin és el conjunt de persones implicades en aquest cicle.

3. **Comprovació de Consistència**:
   Un cop identificat el cicle, el programa comprova si el cicle compleix les regles de les relacions d'enemics i amics. Si alguna persona dins del cicle té alguna relació malament (per exemple, el seu amic o enemic no compleix la relació correcta), el programa descarta aquest cicle com a possible solució i busca altres.

4. **Construcció de l'Ordre**:
   Si el cicle és vàlid, es construeix l'ordre de col·locació a partir de la persona arrel seleccionada. El programa construeix l'ordre afegint les persones una a una, respectant les relacions entre enemics i amics. Si en algun moment no és possible col·locar una persona, el programa torna "impossible".

5. **Solució Final**:
   Si es troba un ordre vàlid, el programa imprimeix l'ordre de col·locació de les persones. Si no es pot trobar cap ordre vàlid, el programa retorna "impossible".

El procés es repeteix fins que es trobi una solució vàlida o es determini que no n'hi ha cap.





