# Radix UI

## Introduction

Radix UI est une bibliothèque de composants de bas niveau pour la construction d'interfaces utilisateur accessibles et personnalisables. Elle est idéale pour les développeurs qui souhaitent avoir un contrôle total sur le style et le comportement de leurs composants. Nous l'avons choisi afin de nous faciliter le travail de design et la rapidite de developpement.

## Pourquoi choisir Radix UI

- **Personnalisable** : Radix UI offre une grande flexibilité en termes de personnalisation. Vous pouvez modifier l'apparence et le comportement des composants pour répondre à vos besoins spécifiques.
- **Accessible** : Les composants Radix UI sont conçus avec l'accessibilité à l'esprit. Ils suivent les meilleures pratiques WAI-ARIA pour garantir que vos applications sont accessibles à tous les utilisateurs.
- **Performant** : Radix UI est optimisé pour la performance. Les composants sont légers et rapides, ce qui contribue à une expérience utilisateur fluide.

## Localiser les composants dans le code

Les composants Radix UI sont généralement importés et utilisés dans les fichiers de composants de votre projet. Par exemple, si vous utilisez le composant `Button` de Radix UI, vous pouvez le trouver dans votre code de la manière suivante :

```jsx
import { Button } from '@radix-ui/react-button';

function MyComponent() {
  return <Button>Click me</Button>;
}
