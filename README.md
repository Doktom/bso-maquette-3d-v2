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
