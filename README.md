# H3: Versionhallinta

z) Lue ja tiivistä artikkeli muutamalla ranskalaisella viivalla. Tässä z-alakohdassa ei tarvitse siis tehdä testejä tietokoneella.

[Commonmark contributors: Markdown Reference](https://commonmark.org/help/) (huomaa ainakin otsikot risuaidoilla, kappalejako tyhjällä rivillä, sisennys (tab) koodia, lista, linkki, kuva.

-Tiivistetty artikkeli Markdownin eri komennoista.

-Hyvin yksinkertainen, näyttää hyvältä joka laitteella.

-Ei mitään hienouksia kuten fontin koon, värin tai tyypin muuttamista.

## a) Pull first. Tee useita muutoksia git-varastoosi. Tee muutama muutos, jossa yksi commit koskee useampaa tiedostoa. Anna hyvä kuvaukset (commit message), yksi englanninkielinen lause imperatiivissa (määräysmuodossa) "Add top level menu to Foobar synchronizer"

Aloitin tekemällä uuden repon githubiin, jonka sitten kloonasin omalle virtuaalikoneelleni komennolla

		$ git clone git@github.com:Jimitesti/tehtava3.git

![Clone](https://github.com/Jimitesti/tehtava3/blob/main/Kuvat/2022-04-19.22-01-35.png?raw=true)

Lisäsin hakemistoon pari testitiedostoa nimeltä testi1 ja testi2. Jonka jälkeen puskin ne githubiin komennoilla

		$ git add .
		$ git commit
		
Committasin tekstillä "Add two testfiles for the assignment"

		$ git pull
		$ git push
![Github Push](https://github.com/Jimitesti/tehtava3/blob/main/Kuvat/2022-04-19.22-05-07.png?raw=true)

Jonka jälkeen kaikki tulokset näkyivät githubissa.
## b) Kaikki kirjataan. Näytä omalla git-varastollasi esimerkit komennoista ‘git log’, ‘git diff’ ja ‘git blame’. Selitä tulokset.
		$ git log
Näyttää repositoryn viimeisimmät lokitiedot

![Git Log](https://github.com/Jimitesti/tehtava3/blob/main/Kuvat/2022-04-19.22-39-17.png?raw=true)

		$ git diff
Ei tulostanut minulla yhtään mitään vaikka muutoksia tein.

		$ git blame
Näyttää yksittäisen tiedoston muutokset ja kuka sitä on muokannut.

![Git blame](https://github.com/Jimitesti/tehtava3/blob/main/Kuvat/2022-04-19.22-40-19.png?raw=true)
## c) Huppis! Tee tyhmä muutos gittiin, älä tee commit:tia. Tuhoa huonot muutokset ‘git reset --hard’. Huomaa, että tässä toiminnossa ei ole peruutusnappia.
Tein tyhmän muutoksen testi2 tiedostoon, ajoin komennon

		$ git reset --hard
Jolloin päädyin takaisin viimeisimpään committiin, eli muutoksia testi2 tiedostoon ei ollut tehty.

![Hard reset](https://github.com/Jimitesti/tehtava3/blob/main/Kuvat/2022-04-19.22-20-00.png?raw=true)
## d) Formula. Tee uusi salt-tila (formula, moduli, infraa koodina). Eli uusi tiedosto esim. /srv/salt/terontila/init.sls. Voit tehdä ihan yksinkertaisen parin funktion (pkg, file...) tilan, tai edistyneemmin asentaa ja konfiguroida minkä vain uuden ohjelman: demonin, työpöytäohjelman tai komentokehotteesta toimivan ohjelman. Käytä tarvittaessa ‘find -printf “%T+ %p\n”|sort’ löytääksesi uudet asetustiedostot.
Tätä varten tein yksinkertaisen tilan, joka pelkästään tarkistaa, että jokainen Linux-kone on päivitetty. Ja jos ei ole, niin päivittää sen.

![New State](https://github.com/Jimitesti/tehtava3/blob/main/Kuvat/2022-04-19.22-28-56.png?raw=true)

![Upgradestate](https://github.com/Jimitesti/tehtava3/blob/main/Kuvat/2022-04-19.22-33-05.png?raw=true)
