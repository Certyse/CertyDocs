---
title: Authentification
---
## Authentification avec Next.js et Axios

Dans une application Next.js, vous pouvez utiliser Axios et ses intercepteurs pour gérer l'authentification. Les intercepteurs vous permettent d'intercepter les requêtes ou les réponses avant qu'elles ne soient traitées. 

Voici comment vous pouvez configurer un intercepteur pour ajouter un token d'authentification à toutes les requêtes sortantes :

```javascript
import axios from 'axios';

// Créer une instance d'axios
const api = axios.create({
  baseURL: 'http://localhost:3000',
});

// Ajouter un intercepteur de requêtes
api.interceptors.request.use(async config => {
  // Obtenir le token de l'espace de stockage
  const token = sessionStorage.getItem('token');

  // Si le token existe, l'ajouter à l'en-tête d'autorisation
  if (token) {
    config.headers.Authorization = `Bearer ${token}`;
  }

  return config;
});

export default api;