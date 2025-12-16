# Règles de base 

#### Langue à utiliser : Français si possible sinon l'anglais.
#### Neutralité et Professionnalisme

- **Tolérance Zéro pour l'Humour "Privé" :** La documentation technique doit être intemporelle. Évitez les "inside jokes", les mèmes, les sarcasmes ou les commentaires informels (ex: _"Ce code est une poubelle"_ -> _"Ce code nécessite une refactorisation majeure"_). Imaginez qu'un auditeur externe ou un futur remplaçant lise cette note dans 2 ans.
    
- **Langage Factuel :** Évitez les opinions subjectives non étayées.
    
    - ❌ _"Je pense que l'aluminium est mieux."_
        
    - ✅ _"L'aluminium est recommandé ici pour son ratio résistance/poids supérieur à l'acier (voir analyse X)."_
#### Écrire pour les Autres (Empathie Technique)

- **Le "Bus Factor" :** Écrivez toujours comme si vous alliez être frappé par un bus demain. Si vous êtes le seul à comprendre votre note, elle est inutile à l'équipe.
    
- **Explicitez les Acronymes :** La première fois qu'un acronyme rare est utilisé dans une note majeure, définissez-le. Ne partez pas du principe que tout le monde sait ce que signifie "GSE" ou "TVC" (Thrust Vector Control).
    
- **Contexte Obligatoire :** Ne balancez jamais un chiffre ou un tableau sans explication. Ajoutez toujours une phrase d'intro : _"Voici les résultats du test de pression du 15 décembre :"_.
#### Rigueur Intellectuelle

- **Distinguer Faits et Hypothèses :** C'est la règle la plus dangereuse si elle est ignorée. Si vous n'êtes pas sûr d'une valeur, vous avez le _devoir_ de l'indiquer clairement (ex: _"Valeur estimée, à confirmer par test"_). Ne présentez jamais une supposition comme une vérité absolue.
    
- **Citer ses Sources :** Si une décision est prise basée sur une réunion ou une norme externe, mentionnez-le. _"Selon la norme ISO-XXXX..."_ ou _"Décision prise lors du meeting du 12 nov..."_.
#### Culture de la Critique Constructive

- **Commentaires Bienveillants :** Si vous annotez le travail d'un autre dans Obsidian (via des commentaires ou des callouts), soyez constructif. Attaquez le problème, pas la personne.
    
- **Ne pas Effacer sans Trace :** Si vous devez modifier radicalement le travail de quelqu'un d'autre (ex: changer les specs du moteur), ne supprimez pas simplement son texte. Archivez l'ancienne version ou notifiez la personne concernée. La documentation est un travail collaboratif, pas une guerre d'édition.
#### Responsabilité et Maintenance

- **La Règle du "Boy Scout" :** Si vous tombez sur une note mal formatée, avec une faute d'orthographe flagrante ou un lien mort : réparez-la immédiatement. Ne vous dites pas "ce n'est pas ma note". La qualité de la base de données est la responsabilité de tous.
    
- **Signer les Décisions Majeures :** Pour les choix critiques (ex: changement de matériau), il est bon d'indiquer l'auteur de la note et la date, pour savoir qui contacter si on a des questions plus tard.
#### Sécurité

- **Pas de Mots de Passe :** N'écrivez jamais de mots de passe, de clés API ou de données sensibles en clair dans la Vault, même si c'est "juste pour partager". Utilisez un gestionnaire de mots de passe sécurisé pour cela.


## Voici la structure de base de la vault Obsidian de Sirius :
## Sirius_Knowledge (root)
## Documentation du groupe
- Véhicule de lancement
  - Électrique
    - Sujets
  - Informatique
    - Sujets
  - Mécanique
    - Sujets
  - Propulsion
    - Sujets
- Équipement au sol (GSE)
  - Électrique
    - Sujets
  - Informatique
    - Sujets
  - Ingénierie des systèmes
    - Sujets
  - Mécanique
    - Sujets
- Projet
  - Systems Engineering
    - Sujets
(cette structure est sujet à changements)