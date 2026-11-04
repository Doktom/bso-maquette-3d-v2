# Résidence Henri Clérisse – maquette 3D (V2)

Le bâtiment, fidèlement modélisé depuis l'IFC du projet, dans son environnement, en style « maquette clay » :
- terrain et 5 bâtiments mitoyens issus du relevé « CONTOUR 3D » du même IFC ;
- autres bâtiments, voirie, trottoirs, passages piétons, feux, stops, cédez-le-passage, arrêts de bus et lampadaires
  d'OpenStreetMap, recalés sur les volumes IFC ;
- rampe d'accès au parking souterrain creusée dans le sol ;
- interface volontairement simple (végétation, noms de rues, recentrer).

- `bso.glb` : le bâtiment (≈ 0,5 Mo, compression meshopt)
- `context.glb` : terrain, 5 volumes IFC mitoyens, volumes OSM (≈ 80 Ko)
- `sol.jpg` : texture du sol vue du dessus (fond blanc, chaussées, trottoirs, marquages, ombre de contact)
- `env.json` : arbres, noms de rues, signalisation, emprise de la texture

Version 1 (coupes, logements cliquables, plans de vente) : https://doktom.github.io/bso-maquette-3d/

Test local : `python -m http.server 8000` puis http://localhost:8000

Crédits : three.js (MIT) · voirie © contributeurs OpenStreetMap (ODbL) · terrain et volumes : IFC du projet (DND Architectes).
