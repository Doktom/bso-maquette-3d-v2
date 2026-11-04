# Résidence Henri Clérisse – maquette 3D (V2)

Le bâtiment, fidèlement modélisé depuis l'IFC du projet, dans son environnement réel :
terrain et volumes voisins issus du relevé « CONTOUR 3D » du même IFC, voirie et marquages OpenStreetMap
recalés sur ces volumes. Interface volontairement simple (végétation, noms de rues, recentrer).

- `bso.glb` : le bâtiment (≈ 0,5 Mo, compression meshopt)
- `context.glb` : terrain + volumes voisins (≈ 85 Ko)
- `sol.jpg` : texture du sol vue du dessus (herbe, chaussées, trottoirs, passages piétons, ombre de contact)
- `env.json` : arbres, noms de rues, emprise de la texture

Version 1 (coupes, logements cliquables, plans de vente) : https://doktom.github.io/bso-maquette-3d/

Test local : `python -m http.server 8000` puis http://localhost:8000

Crédits : three.js (MIT) · voirie © contributeurs OpenStreetMap (ODbL) · terrain et volumes : IFC du projet (DND Architectes).
