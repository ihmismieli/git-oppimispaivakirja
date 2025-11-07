# Oppimispäiväkirja: Git projektissa

__Mitä hyötyä voisi olla versionhallinnasta, jos kehität projektia yksin?__

Pystyn hallitsemaan eri versioita. Minulla voi olla projektin main ja sitten kehityshaara develop, jonka yhdistän aina mainiin. Näin minulla pysyy aina yksi ajantasalla oleva versio. Lisäksi versionhallinta antaa mahdollisuuden palata aiempiin versioihin, jos jokin menee pieleen.

__Mitä hyötyä voisi olla versionhallinnasta, jos projektissa on useita kehittäjiä?__

Versionhallinta mahdollistaa sen, että useampi henkilö voi työskennellä saman projektin parissa yhtä aikaa ilman, että heidän työnsä menevät sekaisin. Jokainen voi tehdä omia muutoksia omalla haarallaan ja lopuksi muutokset voidaan yhdistää yhteiseen develop -haaraan ja testata ennen main-haaraan viemistä. Näin vältetään päällekkäiset työt ja konfliktit ja koko tiimi pysyy ajan tasalla projektin etenemisestä.

__Miten järjestäisit projektitiimin versionhallinnan 3-4 hengen ohjelmistoprojektikurssilla? Laadi tiimiläisille lyhyt ohje, miten projektissa toimitaan.__

Luo GitHubiin yhteinen repositorio ja määritä selkeät haarat:

main – aina toimiva ja testattu versio

develop – kehityksen yhteinen haara

Jokaisella kehittäjällä oma feature/ -haara omille tehtäville

Toimintatavat:

- Jokainen kehittäjä tekee uuden haaran develop -haarasta oman tehtävänsä mukaan (esim. feature/login).

- Kun tehtävä on valmis, tehdään commit ja push omalle haaralle.

- Luodaan pull request GitHubissa, jotta muut voivat tarkistaa muutokset ennen yhdistämistä develop -haaraan.

- Kun kaikki toimii ja on testattu, develop yhdistetään main -haaraan.

__Kommenttini opintojaksosta, esim. sisällöstä, materiaalista, työmäärästä, hyödyllisyydestä, työmäärästä. Mitä toivoisit olevan enemmän, mitä vähemmän?__

Kurssin sisältö oli hyödyllinen ja käytännönläheinen. Versionhallinnan perusteet tulivat hyvin selviksi ja tehtävät opettivat konkreettisesti Gitin käyttöä. Työmäärä oli kohtuullinen. Työmaailmassa käytetään paljon rebasea siitä ei ollut tässä mitään, mutta tämä olikin aika perus Git-versionhallintaa.