# Tietokantasovellus
Julkinen repositorio tietokantasovellus kurssia varten

Aihe: Ruokalähetin varusteiden tilaamista varten tehty sovellus

Ideana on tehdä sovellus joka mahdollistaa lähettien varusteiden tilaamisen ilman että pitää ottaa yhteyttä itse asiakaspalveluun tai varastoon.
Sovelluksessa olisi 6 taulua:

  A. Lähettien yleinen tieto:
    1. Nimi
    2. Ajoneuvo
    3. Kaupunki
    4. Lähetti_ID
    
  B. Varasto_1 tilanne:
    1. Tuote
    2. Koko
    4. Määrä
    5. Tuote_ID
    
  C. Varasto_2 tilanne:
    1. Tuote
    2. Tuote_ID
    2. Koko
    4. Määrä
    
  D. Lähettien varuste tieto:
    1. Nimi
    2. Lähetti_ID
    3. Tuote_ID
    
  E. Aktiiviset pyynnöt:
    1. Pyyntö ID
    2. Lähetin ID
    3. Tuote ID
    
  F. Tuotteet:
    1. Tuote ID
    2. Nimi
    3. Koko
    
    
    Kutsu prosessi:
    
    1. Lähetti kirjautuu sisään
      Mitä tapahtuu: CP täyttää kirjautumistiedot, ja niitä verrataan kirjautumistietotaulukkoon.
      Mitä tietotaulukoita käytetään: lähetin kirjautumistaulukko
    
    2. Lähetti täyttää hakemuksen
      Mitä tapahtuu: Sovellus tarkistaa, ettei ole olemassa mitään virheitä aiheuttavia ongelmia, kuten että tuotteesta on jo maksimimäärä tai että pyyntö       on aktiivinen -> Sovellus tarkistaa CP:n sijainnin tunnuksen perusteella kirjautumistaulukosta -> tarkistaa tuotteen saatavuuden valitussa                 kaupungissa -> Jos tuote on saatavilla, sovellus lähettää pyynnön tekemällä uuden merkinnän pyyntöjen taulukkoon ja CP saa ilmoituksen.
  
      Mitä taulukoita käytetään: CP:n yleistietotaulukko, kaupungin varaston inventaariotaulukko, aktiiviset pyynnöt -taulukko, tuotetaulukko, CP:n               nykyiset tuotteet.      
    
