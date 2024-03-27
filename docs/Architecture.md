
## Explication des répertoires
```
app 
├── components
├── model 
├── viewModel 
└── styles
```


### Components

Le répertoire `components/` contient tous les composants réutilisables de l'application. Chaque composant a son propre fichier et est écrit comme une fonction JavaScript.

### Model

Le répertoire `model/` contient les définitions des modèles de données. Ces modèles définissent la structure des données que nous utilisons dans notre application.

### ViewModel

Le répertoire `viewModel/` contient les fichiers ViewModel. Un ViewModel est une abstraction du modèle qui est utilisée pour fournir des données à la vue. Il peut également contenir de la logique pour traiter les données avant qu'elles ne soient envoyées à la vue.

### Styles

Le répertoire `styles/` contient tous les fichiers de style de l'application. Nous utilisons CSS-in-JS pour nos styles, ce qui signifie que nos styles sont écrits en JavaScript et injectés dans notre application au moment de l'exécution.