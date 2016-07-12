# Game of Trades Student Kit

Game of Trades stelt je in staat om op visuele en spelende wijze kennis te maken met algoritmen.  

## Inhoud

De student kit bestaat uit een Java Maven project met daarin een aantal folders:

* src/main/java - hierin moet de bron code komen van de door jullie te maken handelaar. Er staan al wat files voor je klaar. 
* src/test/java - hierin moet de bron code komen die de handelaar test. Sommige testen zijn al geschreven, doe er je voordeel mee!
* src/test/resources - hierin staan een aantal kant en klare kaarten om te gebruiken.
* pom.xml - dit is het bestand dat Maven vertelt hoe het project in elkaar zit en gebouwd moet worden.

## Voorbereiding

Om met Game of Trades mee te kunnen doen heb je een werkende Java ontwikkelomgeving nodig. 

Deze bestaat uit de volgende ingredienten:

* Java 8 Development Kit (JDK) 
* Apache Maven 3.3+
* IDE naar keuze (intelliJ, eclipse, netbeans)
* Git   

## Clonen van de Student Kit

```
> git clone https://github.com/gameoftrades/gameoftrades-student-kit.git

Cloning into 'gameoftrades-student-kit'...
remote: Counting objects: 87, done.
remote: Compressing objects: 100% (51/51), done.
remote: Total 87 (delta 13), reused 79 (delta 8), paRck-reused 0eceiving objects:  13% (12/87)
Receiving objects: 100% (87/87), 15.60 KiB | 0 bytes/s, done.
Resolving deltas: 100% (13/13), done.
Checking connectivity... done.
```

In de `gameoftrades-student-kit` folder staat nu de student kit, klaar om geimporteerd te worden in je IDE.

## Team Specifieke Aanpassingen

Omdat ieder team uniek is maar je net een algemene repository hebt gecloned is het _noodzakelijk_ om een aantal team specifieke aanpassingen te maken.

* In de `pom.xml` pas de waarde van de `artifactId` tag aan naar `got-teamNN` waarbij NN dan het team nummer (2 digits) is. Is het team nummer kleiner dan 10, plak er dan een 0 voor.
* In je ontwikkelomgeving, hernoem de package `studentNN`. Ook hier moet NN het team nummer worden. 
   
## Op te leveren artifacten voor beoordeling

Na het uitvoeren van een `mvn clean install` vindt je in de `target` folder 2 bestanden:

* got-teamNN-0.1.0.jar 
* got-teamNN-0.1.0.sources.jar  

Beiden bestanden moeten opgeleverd worden.

# FAQ / How to

## Hoe begin ik?

* Zorg eerst dat je een werkende ontwikkelomgeving hebt en de student-kit kunt bouwen.
* Rename het artifactId en de packagenaam naar die van je team.
* Run de WereldLaderTest in je IDE en zorg dat alle testen gaan slagen door de WereldLaderImpl.java aan te passen.
* Start de StudentUI en aanschouw de wereld.
* Implementeer nu opdracht 2, 3 en 4. 

## Bouwen van de Student Kit (vanaf de command line)

Bouwen zonder de testen uit te voeren:
```
> mvn clean install -DskipTests
```

Bouwen en wel de testen uitvoeren:
```
> mvn clean install
```

Alleen compileren:
```
> mvn compile
```

Uitvoeren van de testen:
```
> mvn test
```

## Starten van de visuele omgeving.

In de `src/test/java` folder, in de `nl.gameoftrades.ui` package staat een klasse `StudentUI`. Deze start de visuele omgeving.

Let op: De visuele omgeving is afhankelijk van jouw implementatie van Handelaar. Zonder WereldLader kan hij de kaart niet tonen!   
