# Résidence Henri Clérisse – maquette 3D (V2)

Le bâtiment, fidèlement modélisé depuis l'IFC du projet, dans son environnement, en style « maquette clay » :
- les 5 bâtiments mitoyens les plus proches viennent du relevé « CONTOUR 3D » de l'IFC (vraies volumétries) ;
- le reste du quartier (≈ 1 600 bâtiments, voirie, trottoirs, parkings, passages piétons) vient d'OpenStreetMap
  sur ~850 m, recalé sur les volumes IFC, sur un sol plat qui se fond dans le blanc ;
- la rampe d'accès au parking souterrain est creusée ;
- couche « Destinations » (option) : itinéraires routiers vers le centre-ville de Caen, la Porte de Bretagne
  (périphérique et A84) et la mairie de Bretteville, avec distance et temps en voiture (OSRM).

Interface : végétation, noms de rues, destinations, recentrer la vue.

- `bso.glb` : le bâtiment (≈ 0,5 Mo, compression meshopt)
- `world.glb` : environnement (mitoyens IFC, bâtiments et voirie OSM, itinéraires) (≈ 170 Ko)
- `env.json` : arbres, noms de rues, destinations

Version 1 (coupes, logements cliquables, plans de vente) : https://doktom.github.io/bso-maquette-3d/

Test local : `python -m http.server 8000` puis http://localhost:8000

Crédits : three.js (MIT) · © contributeurs OpenStreetMap (ODbL) · itinéraires OSRM · bâtiments mitoyens : IFC du projet (DND Architectes).

## Étages, lots et disponibilités

- `lots-geo.json` : les 30 lots (typologie, surfaces, pièces, orientation, emprise au sol), d'après les plans de vente indice 3.
- `plans/Axxx.pdf` (téléchargement) et `plans/Axxx.jpg` (visionneuse zoomable).
- `lots.json` : **disponibilité de chaque lot**, lue sans cache à chaque chargement. C'est ce fichier que le futur back-office devra écrire :

```json
{ "maj": "2026-11-12", "lots": { "A101": { "statut": "disponible" }, "A102": { "statut": "option" }, "A103": { "statut": "vendu" } } }
```

Statuts reconnus : `disponible` (vert), `option` (orange), `vendu` (rouge). Un lot absent ou au statut inconnu est affiché « Disponible ».
