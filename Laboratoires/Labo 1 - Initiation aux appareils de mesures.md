### Manipulations avec multimètre
#### Mesure de résistances
- Dans les petits casiers du C1-3018 et C1-3024, prenez trois résistances au hasard entre 700 Ω et 2 kΩ. Notez les valeurs en Ω des casiers dans votre cahier de laboratoire.
- Toujours dans votre cahier de laboratoire, notez les codes de couleurs. Déterminez si ces couleurs correspondent bien aux valeurs souhaitées. Notez que le code de couleurs se trouve dans le document d’Annexe du guide étudiant de l’APP1 SN.
![[resistor-color-chart.avif]]
- Allumez le multimètre de votre poste de travail et placez-le en mode de mesure de résistance.
- Validez que les fils sont bien dans le port haute impédance. 
- Mesurez la résistance de vos trois composants et validez qu’elles correspondent aux valeurs attendues.

### Manipulations avec sources de tension et multimètre

- Allumez le bloc d’alimentation. Réduisez la limite de courant presque au minimum en tournant dans le sens antihoraire. Lorsque la lumière CC s’allume, tourner légèrement le bouton afin dans le sens horaire que la lumière CC éteigne.
- Ajustez la tension à 12 V.
- Branchez la source aux bornes d’une des résistances utilisées avec le multimètre. 
- Calculer la valeur théorique du courant qui devrait passer dans la résistance$^1$. 
- Est-ce que la puissance attendue est inférieure à 250 mW (i.e. ¼ W qui est la limite des résistances de laboratoire)? 
- Si ce n’est pas le cas, quel est le problème?$^2$ 

$^1$ Calculez P=V2/r où V = 12 V et donc 144/r. Si r = 10 kΩ alors P= 14,4 mW.
$^2$  Réponse: On brûlera la résistance si la puissance est > 250 mW.

N.B Pour le Siglent, il faudrait utiliser une résistance inférieure à 1 k et limiter le courant à une valeur de 0,01 A.

- Augmentez la limite en courant jusqu’à la stabilisation de la tension à 12 V. 
- Est-ce que le courant lu sur la source est cohérent avec cette prévision ? 
**NOTE** : Si le courant est beaucoup plus grand que vos calculs, il est possible que vous ayez un court-circuit. Fermer la source et valider vos connexions.

- Placer le multimètre en mode voltmètre DC et prenez une lecture de la tension aux bornes de la résistance à l’aide du multimètre (assurez-vous d’être branché dans le port haute-impédance).
- Est-ce que la lecture est plus précise que sur la source ?
- Fermez la source et placez le multimètre en mode ampèremètre (en mode basse impédance et en série entre la source et la résistance). 
- Allumez la source. 
- Comparez la valeur attendue versus la lecture par l’ampèremètre versus le courant affiché sur la source. Expliquez les différences.
- Laquelle est la plus fiable$^3$ ?
$^3$ L’ampèremètre possède une meilleure résolution. Vous pouvez consulter les fiches techniques des appareils sur le web.

**NOTE** : Il se pourrait que le fusible de protection du multimètre soit brûlé, ce qui rend impossible la lecture de courant. Dans ce cas, passez à l’étape suivante.

- Maintenant, calculez la puissance réelle qui est dissipée par la résistance. Refaites les mêmes manipulations avec les deux résistances restantes, mais cette fois en utilisant des tensions de 5 V et 9 V.

**NOTE** : il est possible que le fusible soit brûlé à l’intérieur de l’ampèremètre, dans quel cas, essayer avec le port 10 A (mais il est possible que le courant soit trop petit pour être mesurable) si cela ne fonctionne pas, passer à l’étape suivante.

- Mettre deux sources ajustées à 9 V en série. Mettre les 3 bornes des sources aux bornes (voir les numéros 1, 2 et 3 de la Figure 8) de deux résistances en série comme l’indique la Figure 8.
![[Figure8.png]]

- À l’aide du multimètre en mode voltmètre, mesurez la différence de potentiel des trois points par rapport à la masse du bloc d’alimentation (borne verte ou ou ) sans que celui-ci ne soit branché dans le circuit. 
- Que mesurez-vous ? Pourquoi ?$^4$
$^4$  Réponse : Comme les sources ne sont pas référencées à la masse, on ne devrait rien mesurer. En réalité, en faisant cette mesure, on vient successivement mettre les bornes 1, 2 et 3 à la mise à la terre à travers une résistance élevée. Ceci ne constitue pas une bonne mise à la terre

- Si on relie la masse à la borne 1 des deux sources, quelle sera la différence de potentiel entre la masse et les deux autres nœuds du circuit? $^5$ 
$^5$ Réponse : 9 V à la borne 2 et 18 V à la borne 3.
- Si maintenant on relie la masse à la borne 2, quelle sera la différence de potentiel entre la masse et les deux autres nœuds du circuit? $^6$ 
$^6$ Réponse : -9 V à la borne 1 et + 9 V à la borne 3.
- Si on relie la masse à la borne 3, quelle sera la différence de potentiel entre la masse et les deux autres nœuds du circuit?$^7$ 
$^7$ Réponse : -9 V à la borne 2 et – 18 V à la borne 1
- Trouver une analogie pour expliquer le fonctionnement d’une tension négative.

### Manipulations avec l'oscilloscope

- Assurez-vous que la sonde jaune est bien dans l’entrée CH 1 (jaune) et que la sonde bleue est bien dans l’entrée CH 2 (bleu). 
- Assurez-vous que les deux sondes sont en mode 10x (interrupteur sur le côté de la sonde).
- Trouvez sur le devant de l’oscilloscope deux anneaux de métal appelés **Probe Check** ou **Probe comp** ou **Probe Calib** qui servent à la calibration. Branchez-y la sonde jaune et reliez la pince de mise à la terre sur le 2e anneau identifié par le symbole de mise à la terre. Référez-vous à la Figure 9 au besoin. Sur cet anneau, une onde carrée périodique est générée par l’oscilloscope pour aider la calibration des sondes. Nous allons utiliser ce signal pour tester les fonctionnalités de l’oscilloscope.
- Appuyer sur le bouton **CH1 Menu** pour faire apparaître la ligne jaune à l’écran (si elle n’est pas déjà présente). Dans le menu **Ch1 Menu**, mettre le couplage en mode DC, la sonde en mode 10x et s’assurer que l’inversion n’est pas activée. 
- Dans le menu **Trigger**, assurez-vous que l’oscilloscope soit configuré en monde **Type Front** ou **Edge** et que la source soit sur le **CH1**.
- Ajustez les boutons **volts/div**, **vertical position** et **sec/div** afin d’avoir 2 à 3 périodes du signal à l’écran et que l’amplitude occupe plus de 50 % de l’écran. Pour faire des lectures faciles, il est conseillé d’ajuster le bouton de **vertical position** afin d’avoir un plateau directement sur une ligne de division. 
- Dans la même idée, ajuster la position horizontale afin d’avoir un front sur une ligne de division. Si le signal ne se stabilise jamais à l’écran, ajuster le bouton **Trigger Level** de manière à ce que la flèche à droite de l’écran soit environ au milieu du signal, l’image devrait alors se stabiliser.
- En ne se basant que sur les lignes de division, mesurer l’amplitude crête-à-crête du signal. En regardant la référence 0 V, trouver l’amplitude du signal.
**Rappel** : L’amplitude se trouve en multipliant le nombre de divisions par l’échelle Volts/div en bas à gauche de l’écran.
- En comptant les divisions, déterminez la période de ce signal (multipliez le nombre de divisions par l’échelle de temps en bas à droite de l’écran). Avec cette période, déterminez la fréquence du signal$^8$ .
$^8$ Réponse : Le signal de calibration est 0-5 V et de 1 kHz (période de 1 ms) ou de 0-3 V et de 1 kHz
- Si vos mesures sont cohérentes, passez au point suivant ; si non, vérifiez vos manipulations et configurations dans les menus.
- Tel que présenter précédemment, ce signal en onde carrée sert à calibrer les sondes. Vous trouverez une petite vis proche de la connexion à l’oscilloscope qui permet de sous-compenser et de surcompenser les sondes. Si votre onde carrée ressemble à l’une des deux situations de la Figure 10, c’est que la sonde doit être calibrée en se servant d’un tournevis en plastique (tout autre outil nuira à la lecture du résultat de la calibration).
![[Figure10.png]]

- Modifiez le **trigger level** jusqu’à ce que la flèche à droite de l’écran ‘sorte’ de l’écran. Qu’arrive-t-il au signal? 
- Que comprenez-vous de cette situation ? 
- Pourquoi l’oscilloscope ne peut-il pas synchroniser le signal ?$^9$  
- Ramenez le **trigger level** à son niveau précédent avant de passer à l’autre étape.
$^9$ Réponse : Le signal ne passe jamais le seuil de déclenchement. L’oscilloscope affiche n’importe quoi.
- Dans le menu **CH1 Menu**, modifiez le couplage pour être en couplage alternatif (AC). 
- Qu’arrive-t-il au signal ? Est-ce que l’amplitude a changé ? Est-ce que la fréquence a changé ? Est-ce que le signal d’entrée a vraiment changé ou est-ce uniquement l’affichage qui est différent ?$^{10}$  
- Ramenez le couplage dans le mode **DC** avant de passer à l’étape suivante.
$^{10}$ Réponse : En réalité, le signal est une onde carrée périodique de 1 kHz de ± 2,5 V à laquelle est ajoutée une tension DC de 2,5V pour générer une onde carrée périodique 0 à 5 V. Le fait de se mettre en AC enlève la composante DC de 2,5 V et l'on retrouve seulement le signal carré de ± 2,5V.

- Ouvrez le menu **Measure**. En appuyant sur les boutons à la droite de l’écran ou sur le bouton « Type » en bas de l’écran, faites circuler toutes les mesures possibles que peut fournir l’oscilloscope. Après vous être familiarisé avec les différentes mesures possibles, affichez la tension RMS du signal sur l’un des 4 ou 5 emplacements de mesure.
- Avec le **multimètre**, prenez cette même valeur de tension RMS et comparez les deux. Est-ce que les valeurs divergent ? Pourquoi ? Déterminez qui a raison et pourquoi$^{11}$ . 
$^{11}$ Si vous n’avez pas trouvé, relisez la section 2.3.3.
-  Au besoin, faites le calcul complet dans votre cahier de laboratoire.
- Prenez la 2e sonde (bleu ou rose) et branchez la sonde au même point. Dans le menu **CH2 Menu**, faites inverser la valeur affichée à l’écran. Changez les volts/div et les deux positions verticales des deux canaux afin de bien voir les deux signaux à l’écran (généralement le CH1 en haut et le CH2 en bas).
- Dans le menu **Math Menu**, essayer les différentes options possibles. Si vous additionnez les deux signaux (CH1 + (-1xCH2), qu’affichera le signal rouge ou blanc ? Si vous faite la soustraction des deux canaux (CH1 - (-1xCH2), que devriez-vous obtenir à l’écran ?$^{12}$ 
$^{12}$ Réponse : une tension DC et le signal multiplié par 2 en amplitude.

### Manipulations avec le générateur de fonctions
- Allumer le générateur et ajuster l’amplitude au minimum. 
- Brancher le générateur aux bornes de la plus haute résistance utilisée lors des manipulations avec le multimètre. 
- Brancher l’oscilloscope aux bornes de cette même résistance (pince crocodile de l’oscilloscope sur la pince noire du générateur et le crochet de la sonde de l’oscilloscope sur la pince rouge du générateur). 
Pour ceux dans le local C1-3016 et 4028, assurez-vous que les atténuateurs -20 dB ne soient pas enclenchés.
- Afin de bien vous familiariser avec les menus, générez les formes d’onde suivantes, en confirmant toujours le résultat avec l’oscilloscope. Comparez aussi la mesure du multimètre (en mode RMS) et la mesure de l’oscilloscope.
	 -  Sinus de 1 kHz de -5 à 5 V.
	-  Sinus de 10 kHz de 0 à 5 V (vous aurez besoin d’une tension de décalage (offset DC)).
	-  Onde carrée de 5 kHz, de 0 à 5 V avec un rapport cyclique de 50%.
	-  Onde carrée de 500 Hz, de -2 à 5 V avec un rapport cyclique d’environ 25%
	-  Onde triangulaire de 200 mVc.à c. à 100 Hz 
Pour ceux aux C1-3016, vous aurez besoin des atténuateurs -20dB pour cette
opération.
### Manipulations pour la mesure d’un courant avec une résistance

-  À l’aide du générateur de fonction, générer une onde carrée de 100 Hz dont l’amplitude varie, en circuit ouvert, entre un niveau bas de 0 V et un niveau haut de +10 V (10 V crête à crête avec un « offset » de + 5 V).
- Valider à l’aide de l’oscilloscope votre sortie du générateur de fonction.
- Placer une résistance de 1 kΩ entre les deux les deux pinces alligators du générateur de fonction.
- Mesurez la chute de tension dans la résistance de 1 kΩ à l’aide de l’oscilloscope. Vous pouvez déduire le courant, en utilisant la relation $𝐼 = 𝑉/𝑅$, et vous pouvez déduire que le courant présente la même forme temporelle.
- Maintenant, ajoutez une résistance de 10 Ohms entre la résistance de 1 kΩ et la masse (pince noire (-))$^{13}$  et mesurez la chute de tension dans la résistance de 10 Ω. En utilisant la même relation $𝐼 = 𝑉/𝑅$, il est plus facile d’estimer le courant qui passe dans la résistance de 1 kΩ.
- Pensez-vous que l’ajout de la résistance de 10 Ohms a un effet sur le courant circulant dans la résistance de 1 kΩ? C’est surement négligeable avec des résistances de 5 %.
- Refaite la même expérience, mais cette fois-ci avec une source de tension continue à 10 V qui remplacera le générateur de fonction.

$^{13}$ Faites un schéma électrique avant de faire ce branchement pour ne pas inverser les 2 résistances. Ce positionnement permet l’utilisation d’une seule sonde pour la mesure.