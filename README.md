# Git-oppimispaivakirja

Tämä on kurssin Git-versionhallinta - SOF013AS2A-3001 oppimispäiväkirja.
Tekijä Heidi Ahlgren.
Tässä repositoriossa on Git-versionhallinta kurssin oppimispäiväkirja, joka sisältää osat 1-3.


# Oppimispäiväkirja 1: Paikallinen git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?__

Helppoa oli peruskomennot kuten git init, git add , git commit, git status. Vaikeaa oli revertin käyttö, kun en ensiksi huomannut että pitää olla commit-tunniste. Branchien käyttö taas oli tuttua, koska olen käyttänyt niitä paljon työelämässä.

Oppimista tuki harjoitusten tekeminen, kun sai tehdä komentoja itse. Jos en onnistunut, palasin lukemaan ohjeita tai katsoin mitä virheviestit sanovat.

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| --------| ------ |
| git status | Näyttää tiedostojen tilan |
| git add . | Lisää kaikki muutokset |
| git reset <tiedosto> | Poistaa tiedoston staging-alueelta, mutta säilyttää muutokset työtilassa |
| git reset . | Poistaa kaikki tiedostot staging-alueelta (ei poista muutoksia työtilasta) |
| git restore <tiedosto> | Palauttaa tiedoston viimeisimpään commit-versioon ja poistaa paikalliset muutokset |
| git restore . | Palauttaa kaikki työtilan tiedostot viimeisimpään commit-versioon |
| git commit -m "viesti" | Tallentaa staging-alueen muutokset commitiksi versionhallintaan |
| git log | Näyttää commit-historian |
| git revert <commit-id> | Luo uuden commitin, joka kumoaa annetun commitin muutokset |
| git switch - | Vaihtaa takaisin edelliseen haaraan |
| git branch | Näyttää olemassa olevat haarat ja kertoo, mikä haara on aktiivinen. |
| git branch <nimi> | Luo uuden haaran annetulla nimellä. |
| git switch <nimi> | Siirtyy olemassa olevaan haaraan. |
| git merge <haara> | Yhdistää annetun haaran nykyiseen aktiiviseen haaraan. |
| git push -u origin <haara> | Työntää muutokset etärepositorioon/originille (GitHubiin) ja luo seurantayhteyden kyseisen haaran ja etähaaran välille. |

# Oppimispäiväkirja 2: Hajautettu git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?__

Helppoa oli luoda repositorio Githubiin, lisätä Githubista sinne uusi tiedosto, katsoa Githubissa luotua sisältöä lokaalisti. Unohdin git pullin tai git merge origin/master, jolloin en ensiksi saanut tuotua muutosta lokaalihaaraan. Oppimista auttaa tehtävät ja hyvät materiaalit.

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| --------| ------ |
| git clone https://github.com/ihmismieli/gitHarjoitus5.git | Kloonaa etärepositorion paikalliselle koneelle. |
| git init | Alustaa uuden paikallisen Git-repositorion. |
| git add . | Lisää kaikki muutokset kommitoitaviksi. |
| git commit -m "first commit" | Tallentaa muutokset paikalliseen historiaan. |
| git push -u origin main | Lähettää muutokset etärepositorioon GitHubiin. |
| git fetch | Hakee uusimmat muutokset etäreposta ilman yhdistämistä. |
| git checkout origin/main | Siirtyy tarkastelemaan etärepositorion main-haaraa (detached HEAD -tilassa). |
| git switch main | Palaa takaisin paikalliseen main-haaraan. |
| git pull | Hakee ja yhdistää muutokset etäreposta paikalliseen haaraan. |
| git status | Näyttää haaran ja tiedostojen tilan. |

# Oppimispäiväkirja 3: Git projektissa

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
