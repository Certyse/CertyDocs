---
title: Axios
---
## Introduction

Axios est une bibliothèque JavaScript très populaire que vous pouvez utiliser pour effectuer des requêtes HTTP. Elle fonctionne à la fois dans le navigateur et dans Node.js. Voici quelques raisons pour lesquelles vous pourriez vouloir utiliser Axios :

## Avantages

1. **Support du navigateur et de Node.js** : Axios a un support universel. Vous pouvez l'utiliser pour envoyer des requêtes HTTP à partir du navigateur et de Node.js.
2. **Promesses** : Axios utilise des promesses pour le traitement asynchrone, ce qui conduit à un code plus propre et plus facile à comprendre.
3. **Interception de requêtes et de réponses** : Vous pouvez intercepter les requêtes et les réponses avant qu'elles ne soient traitées.
4. **Transformations de requêtes et de réponses** : Vous pouvez transformer les requêtes et les réponses avant qu'elles ne soient traitées.
5. **Annulation de requête** : Vous pouvez annuler les requêtes.
6. **Protection contre les attaques XSRF** : Axios a des mesures intégrées pour protéger contre les attaques XSRF.

## Exemples de code

Voici quelques exemples de la façon dont vous pouvez utiliser Axios :

```javascript
// Effectuer une requête GET
axios.get('/user?ID=12345')
  .then(function (response) {
    // traiter la réponse
    console.log(response);
  })
  .catch(function (error) {
    // traiter l'erreur
    console.log(error);
  });

// Effectuer une requête POST
axios.post('/user', {
    firstName: 'Fred',
    lastName: 'Flintstone'
  })
  .then(function (response) {
    console.log(response);
  })
  .catch(function (error) {
    console.log(error);
  });

