# Oppimispäiväkirja: Hajautettu git

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