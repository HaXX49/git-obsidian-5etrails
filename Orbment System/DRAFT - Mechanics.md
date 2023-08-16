An orbment is a small object, made of 1 to 7 slots.
Those slots are linked by power lines

Elemental Effects :

*Lower planes*
Fire: Offense, damages
Water
Earth
Wind

*Higher planes*
Time
Mirage
Space

***
Quartz List:

Attack 1 (Fire) : Add your proficiency bonus to your damage rolls.
***
Foundry Data Structure

Idéalement :

Item -> equipement -> orbment
sinon
Item -> orbment

2 types d'item
- Orbement :
	- Slot \[1-7\] : 
		- quartz : string ? Représente le quartz inséré. Idéalement, slot d'inventaire
		- open : booléen, représente si le slot est ouvert ou non
		- powerline : chiffre, représente l'appartenance d'un slot à une power line. 0 devrait être utilisé pour représenter le slot central, qui appartient à toute power line.
	- Mots clé : String Array, représente les mots clés applicables à l'orbement en question. Analogue, LR Comms, Mass Produced, Brave System, ...

Possède un ActivatedEffect : Orbal Field
*A raffiner au fur et à mesure*
- Cible l'Actor auquel l'objet est équippé
- Pour chaque slot de l'orbement, applique à l'acteur le buff/debuff attendu
- On souhaiterait arriver à un tableau triple appelable de la forme : OrbalValue\[Element\]\[ActorLevel\]\[Intensity\]
- ex: Pour un perso lv 4 ayant équippé un quartz Force 2
	- Actor.str += OrbalValue\[Fire\]\[4\]\[2\]

- Quartz :
	- Element : String parmis les éléments existants
	- Intensité : chiffre de 1 à 5
	- Valeur élémentaire :  nombre
	- Feats intrinsèques ? (pour les Quartz spéciaux)