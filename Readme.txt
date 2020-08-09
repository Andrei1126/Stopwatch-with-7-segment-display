Micut Andrei-Ion 
Grupa 321CB

				~Ceas cu afisaj 7 segmente~


Front Panel:

	In panoul frontal am creat cele 6 cifre prin folosirea segmentelor Square LED, iar 
punctele ce delimiteaza doua cate doua cifre (pentru a arata asemenea unui ceas real) sunt
round LED. Numele fiecarui Square LED (Ex.: boolean 45) l-am omis pentru a simula un ceas
digital.

Block Diagram:
	
	In diagrama block se aflau initial boolene pentru care am creat constante. Pentru
fiecare cifra a panoului frontal am folosit un case structure in care am setat ledurile
pentru fiecare caz in parte (Ex.: case 0 este pentru ledurile ce produc aparitia cifrei 0,
case 1 este pentru 1, etc.). 
	
Pentru primele 2 cifre din panoul frontal am folosit un for loop care va merge pana
la valoarea 60 (numarul de secunde dintr-un minut), un timer a carui valoaree este de 1000
pentru a face trecerea de la o secunda la alta si un Quotient & Remainder pentru a stii a 
doua cifra sa creasca cu 1 dupa ce prima cifra a ajuns la cifra 9.
	
	Pentru urmatoarele 2 cifre am repetat procesul realizat pentru primele 2, cu observatia
ca in for loop se va afla for loop-ul anterior si cele 2 cifre curente.

	Pentru urmatoarele 2 cifre s-a repetat procesul, iar for loop-ul de la cele 2 cifre 
anterioare este inclus in for loop-ul celor 2 cifre actuale. De data aceasta for loop-ul
va merge pana la 24 (reprezentand numarul de ore).


	Ultimul for loop (cel care include toate componentele shemei) se va gasi intr-un while
ce va itera la infinit sau pana cand este apasat butonul abort execution.