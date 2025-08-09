<p align="center">
   <img width="768" height="768" alt="Satellite" src="https://github.com/user-attachments/assets/36eb0eb9-4e3e-4b7e-b065-11105dfbef58" />
</p>

<img width="16" height="16" alt="image" src="https://github.com/user-attachments/assets/a03063ab-5834-437d-846d-acc130d903ab" /> [English version](README_en.md)

# 🛰️ Satellite GPS – ComputerCraft

## 📖 Présentation
Ce script transforme un ordinateur ou une turtle équipée d’un modem sans fil en balise GPS pour le système de localisation ComputerCraft.  
Il permet à d’autres appareils (turtles, ordinateurs, drones, etc.) d’obtenir leurs coordonnées précises dans le monde Minecraft.  

Ce satellite fait partie d’un réseau GPS composé d’au moins 3 balises (idéalement 4 pour plus de précision et de fiabilité).

## ⚙️ Fonctionnement
Diffuse en continu sa position exacte via le protocole GPS de ComputerCraft.

Utilise un modem sans fil pour communiquer avec les autres appareils.

Supporte les modems standards et les Ender Modems pour un réseau multi-dimensions.

Compatible avec PixelLink si utilisé dans un réseau supervisé.

## 🛠️ Installation

> [!TIP]
> Idéalement, le satellite doit être placé à la couche 255 afin d'optimiser au maximum sa portée.

1. Construisez la structure suivante (7x7x4) :

<p align="center">
   <img width="1579" height="1217" alt="2025-08-04_18 44 52" src="https://github.com/user-attachments/assets/d51c7993-c5b9-48e0-a52d-b948f15ddc89" />
</p>

2. Fixez le modem sans fil sur n’importe quel côté.
3. Notez avec précision les coordonnées (x, y, z) de votre balise.
4. Téléchargez le script du satellite : *startup.lua* disponible dans ce repository.
5. Adaptez les coordonnées x, y et z dans le startup.lua aux coordonnées de votre PC.
6. Redémarrez l’ordinateur.
7. Répetez cette action pour les 3 autres balises.

## 🛰️ Nombre et placement des satellites
Minimum : 3 balises par satellite pour un fonctionnement basique.

Recommandé : 4 balises par satellite, placés de préférence à haute altitude (> y=100) pour maximiser la portée.

Portée des modems :

Modem sans fil : 64 blocs (portée augmente avec l’altitude, jusqu’à 384 blocs au niveau 256)

Ender modem : portée illimitée, inter-dimensionnelle

## 🔍 Utilisation par une Turtle
Exemple pour obtenir les coordonnées GPS :
```
local x, y, z = gps.locate()
if x then
    print("Position actuelle : ", x, y, z)
else
    print("Signal GPS indisponible")
end
```
