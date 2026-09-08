# Objets pour Écran MJ

Dépôt d'images d'objets (vue de dessus, PNG transparent) lu par l'application **Écran MJ**
(panneau *Objets → Dépôt GitHub public → Synchroniser*).

## Organisation
- Un sous-dossier = une catégorie (`contenants/`, `mobilier/`, `camp/`… — libre).
- Formats acceptés : png, webp, jpg, gif, svg. Fond transparent conseillé, 256 à 512 px de côté suffisent.
- Le nom du fichier devient le nom de l'objet (`feu-de-camp.png` → « Feu de camp »).

## Taille en cases (5 pi)
Deux façons, la seconde a priorité :
1. Dans le nom du fichier : `table_2x1.png` (2 cases de long), `chaudron@0.75.png` (¾ de case).
2. Dans `objets.json` (optionnel) :
```json
{
  "mobilier/table.png": { "name": "Table", "size": 2, "cat": "Mobilier" }
}
```
La taille = le côté le plus long, en cases. Le ratio de l'image est conservé (une table 2:1 avec `size: 2` occupe 2 × 1 cases).

## Mise à jour
Ajoute, remplace ou supprime des fichiers, pousse sur la branche principale, puis clique **Synchroniser** dans l'app
(ou laisse « Synchroniser à l'ouverture » coché). Seules les images nouvelles ou modifiées sont retéléchargées ;
elles restent en cache dans le navigateur, donc l'app fonctionne ensuite hors ligne.
