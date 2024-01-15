# Formalisation

## Compréhension du Problème

Le problème concerne la maximisation du taux d'occupation des salles de cours dans une école, avec les contraintes suivantes :
- Heures d'ouverture : de 8h à 20h.
- Réservation des salles : créneaux de 2 heures.
- Nombre d'étudiants (N) répartis en G groupes.
- Chaque groupe suit un ensemble d'enseignements spécifique.
- Nombre de professeurs (P) : chaque professeur peut enseigner 4h en continu et 8h par jour, et est qualifié pour certains enseignements.
- Nombre de salles (S) : chaque salle peut accueillir un groupe.

## Formalisation Mathématique

**Variables:**
- \( X_{g, t, s, p} \) : variable binaire indiquant si le groupe \( g \) a un cours dans la salle \( s \) avec le professeur \( p \) au créneau horaire \( t \).

**Contraintes:**
1. Contrainte de disponibilité des salles :
   \[ \sum_{g, p} X_{g, t, s, p} \leq 1, \quad \forall s, \forall t \]

2. Contrainte de disponibilité des professeurs :
   \[ \sum_{g, s} X_{g, t, s, p} \leq 1, \quad \forall p, \forall t \]

3. Contrainte de durée maximale d'enseignement pour les professeurs :
   \[ \sum_{g, s, t} X_{g, t, s, p} \leq 4, \quad \forall p, \text{ pour 4 heures consécutives} \]
   \[ \sum_{g, s, t} X_{g, t, s, p} \leq 8, \quad \forall p, \text{ pour la journée} \]

4. Contrainte de qualification des professeurs (à spécifier selon les qualifications).

**Fonction Objectif:**
- Maximiser le taux d'occupation des salles :
  \[ \text{Maximiser} \sum_{g, s, p, t} X_{g, t, s, p} \]

## Conclusion

Cette formalisation mathématique présente un cadre pour aborder le problème de planification des salles de cours dans une école. Elle doit être adaptée et éventuellement étendue en fonction des besoins spécifiques et des contraintes supplémentaires du problème réel.
