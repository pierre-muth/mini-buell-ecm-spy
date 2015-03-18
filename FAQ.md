Frequently asked questions


## Où trouver l'écran OLED ##

L'écran utilisé est un [4D Systems µOLED-128-G1(GFX)](http://www.4dsystems.com.au/prod.php?id=84).
On peut le trouver en France chez [Lextronic](http://www.lextronic.fr/P4470-afficheur-oled-couleur-uoled128-g1.html)



## L'écran suffit-il ? ##

Non, il faut également un module de conversion USB < - > Série afin de programmer l'écran, et une carte microSD contenant les fichiers nécessaires au fonctionnement du programme.



## Il existe 2 modules de conversion USB < - > Série, lequel prendre ? ##

Il existe en effet 2 modèles :

-  [µUSB-CE5](http://www.lextronic.fr/produit.php?id=2255)

-  [µUSB-MB5](http://www.lextronic.fr/produit.php?id=1639)

Les 2 modules sont compatibles avec l'afficheur, le µUSB-MB5 à l'avantage de pouvoir être intégré au boitier.


## Comment raccorde t-on l'ensemble ? ##

L'afficheur vient chercher les informations dans l'ECM via la prise diagnostique.
Il faut donc une prise compatible que l'ont peut trouver en kit chez Farnell ( ref: [DT06-4S](http://fr.farnell.com/deutsch/dt064s-ce06/plug-dt-4-way-skt/dp/1817020) ; [0462-201-16141](http://fr.farnell.com/deutsch/0462-201-16141/crimp-contact-skt-size16-16-18awg/dp/1817043) (x4) ; [W4S](http://fr.farnell.com/deutsch/w4s-p012/wedgelock-for-dt-plugs-4way/dp/1817056) )

L'afficheur s'alimente en 5V, il faut fabriquer un module de régulation afin de transformer le 12V disponible en 5V.
Pour cela, il faut un régulateur 5V 7805 et deux condensateurs (47µF 16V et 470µF 16V) disponible dans tout bon magasin d'électronique.

Il est préférable d'utiliser du câble blindé pour la liaison entre la prise diagnostique et l'afficheur.

Un schéma de câblage est disponible [ICI](http://code.google.com/p/mini-buell-ecm-spy/downloads/detail?name=Sch%C3%A9mas%20MiniECMSpy.pdf&can=2&q=)


## J'ai tous les éléments, il suffit juste de tout raccorder ? ##

Evidemment non, il faut également programmer l'afficheur. Pour cela il suffit de suivre le [Guide de mise en route](http://code.google.com/p/mini-buell-ecm-spy/wiki/Guide_de_mise_en_route).