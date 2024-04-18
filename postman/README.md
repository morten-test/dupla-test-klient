# Documentation

## Generelt

Denne collection er til import i Postman og kan bruges til at teste
requests mod Dupla services med et JSON web token(jwt). Den kan bla.
bruges til at verificere hvordan et system skal kalde mod DUPLA.

Folderen Token indeholder ét request der giver et jwt der gemmes i en global parameter kaldet token. 
Dette token(jwt) kan bruges mod alle requests i denne collection.

Folderen Services indeholder subfoldere for hver service i Dupla med tilgængelige requests og API specifikation for hver service.

Hver request indeholder krævede og mulige parametre og headere.

## Opsætning

Installer [Postman](https://www.postman.com/) og opret et workspace (knappen New).

I det oprettede workspace importeres filen Vejledning.json.

For at benytte den importerede collection skal der tilføjes et VOCES certifikat. 
Alle benyttede aftaler er tilknyttet et offentligt tilgængeligt VOCES
certifikat fra [Nets](https://www.nets.eu/dk-da/kundeservice/nemid-tjenesteudbyder/NemID-tjenesteudbyderpakken/Pages/OCES-II-certifikat-eksempler.aspx).

Dupla stiller også et testcertifikat til rådighed, som forefindes i dette github repo: DUPLA-Test.p12. 

I settings i Postman vælges Certificates og derefter Add certificate.

I host skrives oces.billetautomat.tfe.skat.dk, vælg Select file ved PFX file og indsæt det downloadede certitikat, indtast t;Of.U3ILO09 i Passphrase og tryk på knappen Add.

Kald requestet Hent token i folderen Token og kald derefter det ønskede request for en service.
