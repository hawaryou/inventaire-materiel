# inventaire-materiel
========================================================
SCANNER EAN-13 + GOOGLE FORMS
========================================================


OBJECTIF
--------

Cette application permet de scanner avec la caméra
d'un téléphone les numéros EAN-13 des équipements :

- Lit SN
- Potence SN
- Barrière SN
- Matelas à air SN

Le Lit est obligatoire.

Potence, Barrière et Matelas à air sont facultatifs.


========================================================
GOOGLE FORM
========================================================

Le formulaire utilisé est :

https://docs.google.com/forms/d/e/1FAIpQLSfe21uOKi4dTW2KQIdEnEFpxCsv6kwpwppbYRs9bVtykDYeCQ/viewform


IDENTIFIANTS DES QUESTIONS
--------------------------

Foyer :

entry.358264119

Nom :

entry.1190830405

Chambre :

entry.1451593184

Lit SN :

entry.2011644043

Potence SN :

entry.904645354

Barrière SN :

entry.426464072

Matelas à air SN :

entry.1812177639


========================================================
FONCTIONNEMENT
========================================================

1. L'utilisateur ouvre scanner.html.

2. Il renseigne :

   - Foyer
   - Nom
   - Chambre

3. Il appuie sur "Scanner" pour le Lit.

4. Le navigateur demande l'autorisation d'utiliser
   la caméra.

5. L'utilisateur présente le code EAN-13 devant
   la caméra.

6. Le numéro est automatiquement récupéré.

7. Il peut éventuellement scanner :

   - Potence
   - Barrière
   - Matelas à air

8. Il clique sur :

   "Continuer vers le formulaire"

9. Google Forms s'ouvre avec les réponses préremplies.

10. L'utilisateur vérifie les informations.

11. Il clique sur "Envoyer".

12. La réponse est enregistrée dans le Google Sheet
    associé au Google Form.


========================================================
HEBERGEMENT
========================================================

IMPORTANT :

NE PAS héberger scanner.html dans Google Apps Script
HTML Service si la caméra ne fonctionne pas.

Le scanner doit être accessible via HTTPS.

Une solution simple consiste à utiliser :

- GitHub Pages
- ou un autre hébergeur HTTPS


========================================================
TEST
========================================================

Avant utilisation réelle :

1. Ouvrir scanner.html avec Chrome ou Safari
   sur un téléphone.

2. Autoriser la caméra.

3. Scanner un véritable EAN-13.

4. Vérifier que les 13 chiffres apparaissent.

5. Cliquer sur "Continuer vers le formulaire".

6. Vérifier que les données sont correctement
   préremplies.

7. Envoyer le formulaire.

8. Vérifier la ligne correspondante dans Google Sheets.


========================================================
IMPORTANT
========================================================

Les codes sont validés avec le chiffre de contrôle
EAN-13.

Un code comportant 13 chiffres mais ayant un mauvais
chiffre de contrôle sera refusé.

La bibliothèque html5-qrcode est chargée depuis :

https://unpkg.com/html5-qrcode@2.3.8/html5-qrcode.min.js
