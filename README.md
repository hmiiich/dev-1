LAB1Dev
Travaux Pratiques Android – TP1 : HelloToast 📱
Objectif du TP
Ce premier travail pratique a pour but de se familiariser avec l'environnement Android Studio et de créer une première application Android fonctionnelle. L'application réalisée permet d'interagir avec deux boutons : l'un pour afficher une notification temporaire (Toast), l'autre pour incrémenter un compteur visuel.

Vidéo de démonstration
📹


https://github.com/user-attachments/assets/4f7f2df4-2e7e-4c9f-a5c6-79d240bbbd96


 Toast.mp4 
Ce que fait l'application
L'interface principale contient trois éléments :

Un bouton TOAST en haut → affiche le message "Bonjour Kaoutar Menacera" pendant quelques secondes
Un grand chiffre au centre → représente le nombre de fois que le bouton COUNT a été pressé
Un bouton COUNT en bas → augmente le compteur de 1 à chaque pression
Le thème visuel de l'application utilise une couleur rose vif pour les boutons et la barre de navigation.

Environnement de développement
Outil	Version / Détail
IDE	Android Studio
Langage	Java
Émulateur	Pixel 6 Pro – API 33
Gradle Plugin	8.1.0
Durée du build	7 secondes
minSdk	24
targetSdk	34
Organisation des fichiers
HelloToast/
├── app/
│   └── src/
│       └── main/
│           ├── java/
│           │   └── com/example/hellotoast/
│           │       └── MainActivity.java
│           ├── res/
│           │   ├── layout/
│           │   │   └── activity_main.xml
│           │   └── values/
│           │       ├── strings.xml
│           │       └── themes.xml
│           └── AndroidManifest.xml
└── build.gradle
Extrait du code principal
public void showToast(View view) {
    Toast toast = Toast.makeText(this, "Bonjour Kaoutar Menacera", Toast.LENGTH_SHORT);
    toast.show();
}

public void countUp(View view) {
    mCount++;
    mShowCount.setText(Integer.toString(mCount));
}
Lancer le projet
1. Ouvrir Android Studio
2. File > Open > sélectionner le dossier HelloToast
3. Attendre la fin de la synchronisation Gradle
4. Démarrer l'émulateur Pixel 6 Pro
5. Appuyer sur Run ▶️
Résultat obtenu
Le build s'est terminé avec succès (BUILD SUCCESSFUL). L'application se lance correctement sur l'émulateur. Le compteur s'incrémente bien à chaque clic et le message Toast s'affiche comme attendu.
