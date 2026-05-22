RAPPORT DE LABORATOIRE – HELLO TOAST
Titre	HelloToast : Manipuler les composants et les événements
Cours	Programmation Mobile : Android avec Java
Plateforme	MLIAEdu
Étudiant	hmich mohammed-amine
Date	[Date de réalisation]
1. Objectif du lab
L’objectif de ce premier laboratoire est de :

Créer un projet Android simple.

Concevoir une interface utilisateur avec des boutons et des éléments TextView.

Gérer les événements clics sur les boutons.

Afficher des messages temporaires (Toast).

Mettre à jour dynamiquement le contenu d’un TextView.

2. Travail réalisé
2.1 Création du projet
Un nouveau projet Android a été créé avec Empty Activity.

Nom du projet : HelloToast.

Langage : Java.

SDK minimum : API 21 (Android 5.0).

2.2 Conception de l’interface (layout)
Fichier modifié : activity_main.xml.

Composants ajoutés :

Un TextView central pour afficher le compteur.

Un bouton “Afficher Toast”.

Un bouton “Incrémenter”.

Disposition : ConstraintLayout ou LinearLayout.

2.3 Logique Java (MainActivity.java)
Les actions suivantes ont été implémentées :

Composant	Action	Comportement
Bouton “Afficher Toast”	onClick	Affiche un Toast avec le message “Hello Toast !”
Bouton “Incrémenter”	onClick	Incrémente le compteur et met à jour le TextView
TextView	setText()	Affiche la valeur actuelle du compteur
Extrait de code clé :
java
Button toastButton = findViewById(R.id.button_toast);
Button countButton = findViewById(R.id.button_count);
TextView countText = findViewById(R.id.text_count);

toastButton.setOnClickListener(v -> {
    Toast.makeText(MainActivity.this, "Hello Toast !", Toast.LENGTH_SHORT).show();
});

countButton.setOnClickListener(v -> {
    int count = Integer.parseInt(countText.getText().toString());
    count++;
    countText.setText(String.valueOf(count));
});
3. Résultats obtenus
✅ Application compilée et exécutée avec succès sur émulateur/périphérique physique.

✅ Clic sur “Afficher Toast” → message contextuel apparaît.

✅ Clic sur “Incrémenter” → le compteur augmente et s’affiche à l’écran.

✅ Interface simple et réactive.

Capture d’écran (optionnel)
(Insérer ici une capture de l’application en cours d’exécution)

4. Difficultés rencontrées et solutions
Difficulté	Solution
Oubli de déclarer les IDs des composants dans le layout	Vérification et ajout manuel des attributs android:id
Erreur de conversion du texte du compteur	Utilisation de Integer.parseInt() avec valeur par défaut 0


https://github.com/user-attachments/assets/4f7f2df4-2e7e-4c9f-a5c6-79d240bbbd96


