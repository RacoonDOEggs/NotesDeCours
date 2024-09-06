![[CircuitGlobal.png]]

### Premier Mandat
![[PremierMandat.png]]

1) Vous devez calculer la valeur de résistance R4 permettant de faire circuler un courant de 20 mA dans la DEL, assumant qu’à ce courant, elle présente une chute de tension d’environ 2.0 V à ses bornes. ($R4 = 360\Omega\pm5\%$)
2) Placez les pièces sur votre plaquette de montage. (Attention, la DEL est un composant polarisé). Prévoyez des fils auxquels vous allez brancher les pinces alligator en provenance de la source de tension.
3) Ajustez la source de tension à 9 V et valider à l’aide de l’oscilloscope ou du multimètre qu’elle est bien ajustée.
4) Mettez le circuit sous tension. (La DEL devrait allumer)
5) Validez les valeurs de tension dans les deux composants à l’aide de l’oscilloscope, vous pourrez alors valider le courant avec la tension dans R4.
6) Validez les tensions aux points suivants :
	a) Masse → 0 V
	b) V1 → 9 V
	c) Nœud entre D2 et R5 → ~7 V

### Modification Premier Mandat
Pour cette partie, vous devez modifier le circuit pour faire clignoter la DEL,  utilisez simplement une source de tension variant dans le temps (générateur de fonctions) plutôt qu’une source de tension continue.

1) Mettez les configurations suivantes sur le générateur de fonction qui servira de source V1 du circuit ci-dessus (Figure 6).
	a) Onde carrée
	b) 9 Vcrête-à-crête
	c) 4,5 V de décalage (Offset)
	d) 2 Hz
	e) 75% de rapport cyclique
	f) Haute impédance (High Z) (faire shift menu, flèche en bas jusqu’à SYS menu, flèche droite et regarder OUTPUT, vous devriez voir HIGH Z. Si ce n’est pas le cas, changez pour High Z).
2) Connectez le générateur de tension à l’oscilloscope, puis validez la tension de sortie. Si vous n’obtenez pas la tension désirée, vérifiez le paramètre d’impédance de sortie du générateur de fonctions ou demandez de l’aide pour comprendre. Fermez ensuite le générateur de fonction.
3) Connectez le générateur au montage avec la DEL
4) À l’aide de l’oscilloscope, valider les tensions aux points suivants :
	a) Masse → 0 V
	b) V1 → Onde carrée env. 0-9 V, fréquence de 2 Hz et rapport cyclique de 75%
	c) R4 → Onde carrée env. 0-7 V, fréquence de 2 Hz et rapport cyclique de 75%
	d) Tension dans R4.
	e) Courant dans le circuit.

### Deuxième Mandat
Pour cette partie, vous devez monter un circuit qui permettra de générer la cadence de la DEL à la fréquence désirée en remplacement du générateur de fonction (Figure 8). Vous devrez débuter par déterminer le numéro de chacune des pattes pour faire vos connections, voir la (Figure 9Figure 1). Le NE556 contient 2 timer, vous devrez en choisir un seul et laisser les autres pattes libres.

![[Mandat2.png]]

1) À l’aide de la fiche technique du NE556, calculez les valeurs de R1 et R2 pour ajuster la sortie du 556 à la fréquence désirée. Consulter la section « Astable operation » de la fiche technique du NE555 pour obtenir les équations.
($R1=11k\Omega\pm5\%,R2=5.6k\Omega\pm5\%$)

**Note #1 :** Dépendamment de votre montage, vous pourriez rencontrer des problèmes de stabilité avec les NE556. Ces derniers sont sensibles aux variations d’alimentation et de charge. Il faut découpler l’alimentation en mettant des condensateurs entre l’alimentation et la masse. Ces condensateurs vont minimiser les variations sur l’alimentation résultant des pics de courant
momentanés demandés par les circuits électroniques; ce qui a pour effet de « nettoyer » l’alimentation. Vérifiez la stabilité de l’alimentation en utilisant la technique vue dans le laboratoire 1. Les condensateurs de découplage doivent idéalement être placés proche des circuits intégrés. Si cela n’est pas suffisant, on utilise même parfois des ferrites pour séparer les alimentations de chacun des
circuits. Il est raisonnable de prévoir un condensateur de découplage pour chacun des circuits intégrés quand vous en avez plusieurs.

2) Assurez-vous que le circuit est désalimenté. Déconnectez le générateur de fonctions si pas déjà fait.
3) Ajoutez le NE556, les condensateurs et les résistances.
4) Ouvrez la source de tension.
5) À l’aide de l’oscilloscope, validez les tensions aux points suivants :
	a) Masse → 0 V
	b) V1 → 9 V
	c) TP1 → Onde carrée 0-9 V, 2 Hz, Rapport cyclique de 75%
1) Fermez la source d’alimentation et ajouter l’étage 3 qui a été monté précédemment, voir Figure 10
![[Images/Laboratoires/2/Figure10.png]]

### Troisième Mandat
1) Mesurez et observez la forme d’onde du courant circulant dans tout le circuit à l’aide d’une résistance R3 de 10 Ohms et de l’oscilloscope (voir la note #2 plus bas). Voir Figure 11.

**Note #2 :** Une approche pour mesurer le courant total d’un circuit est de mettre une petite résistance (résistance de mesure de courant) entre le 0 V de la source de tension (fil noir) et le 0 V (TP2) de l’alimentation du circuit. On utilise ensuite l’oscilloscope pour mesurer la tension aux bornes de cette résistance, qui est proportionnelle au courant. La valeur de la résistance ne doit pas être trop élevée
pour affecter le circuit, mais pas trop basse, car la tension générée sera trop petite pour que l’oscilloscope puisse bien la mesurer. Vous pouvez estimer la valeur de cette résistance en évaluant le courant théorique consommé par le circuit. Il faut que la tension dégagée par le courant circulant dans la résistance soit de l’ordre de 100 mV au maximum; ce qui est une perte considérée négligeable par rapport à la tension d’alimentation de 9 V. 
Portez attention avant de réaliser le montage : est-ce que la référence du bloc d’alimentation est connectée au « ground » du secteur, et qu’en est-il de la référence de l’oscilloscope? Est-ce que ça a un impact sur votre branchement pour cette mesure?

![[Figure11.png]]

2) Avec la mesure de courant que vous venez de réaliser, calculez la puissance consommée par tout le circuit.