# Oppimispäiväkirja: Paikallinen git

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