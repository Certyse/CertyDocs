# Lottie

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