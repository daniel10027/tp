# TD 1 BD

# EXO 1 (CINEMA)
-- Question 1

>Titre des films dont la durée est supérieure ou égale à deux heures:
    SELECT Titre
   FROM Film
   WHERE Duree >= 2;
   
-- Question 2

>Nom des villes abritant un cinéma nommé « RIF »
  SELECT NomVille
  FROM VILLE 
  WHERE VILLE.CodePostal 
  IN (
        SELECT CodePostal 
        FROM CINEMA 
        WHERE NomCine='RIF'
        );
        
--Question 3

> Nom des cinémas situés à Meknès ou contenant au moins une salle de plus 100 places
 SELECT  NomCine  
 FROM  CINEMA  
 WHERE  CodePostal = ( SELECT  CodePostal FROM VILLE  
 WHERE  NomVille="Meknes") 
 OR  NumCine  IN 
     (SELECT  NumCine  FROM  SALLE  WHERE  Capacite >=100);

--Question 4

> Nom, adresse et ville des cinémas dans lesquels on joue le film « Hypnose » la semaine 18

  SELECT C.NomCine , C.Adresse , V.NomVille  
  FROM  CINEMA  as C, VILLE  as V 
  WHERE C.CodePostal = V.CodePostal 
  AND C.NumCine  
  IN (SELECT S.NumCine  FROM  SALLE  as S, FILM as F, PROJECTION  as P 
  WHERE P.NumExploit=F.NumExploit  
  AND P.NumSalle=S.NumSalle
  AND F.Titre="Hypnose" 
  AND P.NumSemaine =18)
  
  --Question 5
  
  > Les titres des films qui n'ont pas été projété
  
  SELECT  Titre  FROM  FILM  
  WHERE  NumExploit  NOT IN (SELECT  NumExploit  FROM  PROJECTION)
  
  # Exo2 (EMPLOYES)
  
  --Question 1
  > ecris une requête sql qui permet de selectionner tous les Employes
  SELECT * FROM Employes;
  
  --Question 2
  
  > Ecris une requête qui permet de récuperer toutes les informations de l'employé dont ENO est égale à 5
  
 SELECT *
 FROM Employes
 WHERE ENO = 5;
 
 --Question 3
 
 > Ecris une requête qui permet de récuperer toutes les informations des l'employés dont ENO est inférieur à 5
  SELECT *
 FROM Employes
 WHERE ENO < 5;
 
 # Exo3 (POPULATION)
 
  --Question 1
  >>
  --Question 2
  >>
  --Question 3
  >>
  --Question 4
  >>
  --Question 5
  >>
  --Question 6
  >>
  
  
  
    
