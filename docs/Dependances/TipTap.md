# TipTap Editor

## Pourquoi TipTap

TipTap est un éditeur de texte riche pour le web. Voici pourquoi nous avons choisi TipTap :

- **Flexibilité** : TipTap est hautement personnalisable. Vous pouvez ajouter ou supprimer des fonctionnalités, changer l'apparence, et plus encore.
- **Rapidité** : TipTap est construit sur ProseMirror, une bibliothèque d'édition de texte qui est rapide et performante.
- **Puissance** : TipTap supporte une grande variété de fonctionnalités d'édition de texte, y compris le formatage de texte, les listes, les tableaux, les images, et plus encore.

Nous avons entièrement personnalisé TipTap pour répondre à nos besoins spécifiques.

## Exemple d'utilisation dans Next.js

Voici comment vous pouvez utiliser TipTap dans un projet Next.js. Dans cet exemple, nous utilisons le composant `Editor` de la bibliothèque `tiptap`.

```jsx
import { useEditor, EditorContent } from '@tiptap/react';
import StarterKit from '@tiptap/starter-kit';

function MyComponent() {
  const editor = useEditor({
    extensions: [
      StarterKit,
    ],
    content: '<p>Hello World</p>',
  });

  return <EditorContent editor={editor} />;
}