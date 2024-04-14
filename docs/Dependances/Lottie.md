# Lottie

## Introduction à Lottie
Lottie est une bibliothèque d’animation open-source créée par Airbnb qui a révolutionné la façon dont les animations sont utilisées dans les applications mobiles et web. Elle permet aux concepteurs de créer des animations complexes dans **Adobe After Effects** et de les exporter au format JSON à l’aide d’un plugin appelé **Bodymovin**. Ces fichiers JSON peuvent ensuite être utilisés dans votre application pour afficher des animations de haute qualité qui peuvent être contrôlées de manière dynamique avec du code.
L’un des principaux avantages de Lottie est qu’elle utilise le **rendu vectoriel** pour les animations. Cela signifie que **les animations peuvent être redimensionnées sans perte de qualité**, ce qui est parfait pour les applications qui doivent fonctionner sur une variété de tailles d’écran et de résolutions.
En outre, Lottie offre une grande flexibilité en termes de **contrôle des animations**. Vous pouvez démarrer, arrêter, boucler et même modifier la vitesse de l’animation de manière programmatique. Cela ouvre un monde de possibilités pour créer des **expériences utilisateur interactives et engageantes**.


## Pourquoi Lottie

Lottie est une bibliothèque qui permet de rendre des animations Adobe After Effects au format JSON. Voici pourquoi nous avons choisi Lottie pour les animations :

- **Flexibilité** : Lottie permet de contrôler les animations de manière programmatique, ce qui offre une grande flexibilité en termes de déclenchement, de vitesse, de boucle, et plus encore.
- **Compatibilité** : Lottie est compatible avec de nombreux environnements, y compris les applications web, mobiles et de bureau.
- **Qualité** : Les animations Lottie sont rendues en temps réel, ce qui signifie qu'elles peuvent être de haute qualité sans augmenter la taille du fichier.

## Exemple d'utilisation dans Next.js

Voici comment vous pouvez utiliser Lottie dans un projet Next.js. Dans cet exemple, nous utilisons le composant `Lottie` de la bibliothèque `react-lottie`.

```jsx
import { useEffect, useState } from 'react';
import Lottie from 'react-lottie';
import animationData from './animation.json';

function MyComponent() {
  const [isStopped, setIsStopped] = useState(false);

  useEffect(() => {
    const timer = setTimeout(() => setIsStopped(true), 5000);
    return () => clearTimeout(timer);
  }, []);

  const defaultOptions = {
    loop: true,
    autoplay: true, 
    animationData: animationData,
    rendererSettings: {
      preserveAspectRatio: 'xMidYMid slice'
    }
  };

  return <Lottie options={defaultOptions} isStopped={isStopped} />;
}
