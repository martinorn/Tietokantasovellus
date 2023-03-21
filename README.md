# Tietokantasovellus
Julkinen repositorio tietokantasovellus kurssia varten

Aihe: Ruokalähetin varusteiden tilaamista varten tehty sovellus

Ideana on tehdä sovellus joka mahdollistaa lähettien varusteiden tilaamisen ilman että pitää ottaa yhteyttä itse asiakaspalveluun tai varastoon.
Sovelluksessa olisi 6 taulua:
  A. Lähettien yleinen tieto
    1. Nimi
    2. Ajoneuvo
    3. Kaupunki
    4. Lähetti_ID
  B. Varasto_1 tilanne
    1. Tuote
    2. Koko
    4. Määrä
    5. Tuote_ID
  C. Varasto_2 tilanne
    1. Tuote
    2. Tuote_ID
    2. Koko
    4. Määrä
  D. Lähettien varuste tieto
    1. Nimi
    2. Lähetti_ID
    3. Tuote_ID
  E. Aktiiviset pyynnöt
    1. Pyyntö ID
    2. Lähetin ID
    3. Tuote ID
  F. Tuotteet
    1. Tuote ID
    2. Nimi
    3. Koko
    
    
    Request flow:
    
    1. CP logs in
      What happens: CP fills out login information and this is compared to the login data table
      Which data tables are used: CP login table
    2. CP fills out material request
      What happens: The application checks for any error causing issues such as already having max amount of a product or an active request -> 
                    The application checks the location of the CP by their ID from the login table -> checks for item availability in chosen city -> 
                    if the item is available the application sends a request by making a new entry in the requests table and CP is notified
      Which data tables are used: CP general info table, city warehouse inventory table, active requests table, product table, CP current products
      
    
