
J'ai affich� le calendrier avec deux m�thodes diff�rentes:
La premi�re m�thode :

Dand le fichier "seo.contactpromo1" , pour les boutons date1 et date2, il suffit de cliquer sur
n'importe quelle zone de l'�l�ment date1 pour afficher le calendrier afin de choisir une date.

Dans le fichier style.css, j'ai ajout� quelques modifications pour la forme des4 boutons afin qu'ils soient similaire aux autres boutons.

J'ai d�sactiv� le choix de choisir "nombre d'adultes" ou "nombre d'enfants".

Pour que le formulaire ne doive pas pouvoir �tre envoy�, j'ai fait "" l'action="#" "" du formulaire.Mais il y a une autre m�thode
 en javascript, il suffit d'utiliser  event.preventDefault()
 pour annuler l'envoi du formulaire :

document.getElementById("submit_button").addEventListener("click", function(event)
{
    event.preventDefault()

	

});

Avec submit_button l'id du bouton envoyer.

dans le ficheir main.js, j'ai ajout� le code suivant : 
$(function(){
		
	 $('.datepicker').datepicker();

});

----------------------------------------------------------------------------------------------
La 2�me m�thode :

Dand le fichier "seo.contactpromo2" , pour les boutons date1 et date2, il faut  cliquer sur
l'icone du bouton pour afficher le calendrier afin de choisir une date(On peut choisir la date et l'heure AM ou PM).

Dans le fichier style.css, j'ai ajout� quelques modifications pour la forme des4 boutons afin qu'ils soient similaire aux autres boutons.

J'ai d�sactiv� le choix de choisir "nombre d'adultes" ou "nombre d'enfants".

Dans le html, j'ai modifi� le code des deux dates en utilisant bootsrap:
<div class="form-group">
			
	<div class='input-group date' id='datetimepicker1' >

											
		<input type='text' class="form-control" required="" placeholder="Choisir une date *" id='date1'/>
										
		<span class="input-group-addon">
										
			<span class="glyphicon glyphicon-calendar"></span>
												</span>
									
	</div>
									
</div>

Pour que le formulaire ne doive pas pouvoir �tre envoy�, j'ai fait "" l'action="#" "" du formulaire.Mais il y a une autre m�thode
en javascript, il suffit d'utiliser  event.preventDefault()
 pour annuler l'envoi du formulaire :

document.getElementById("submit_button").addEventListener("click", function(event)
{
    event.preventDefault()

	

});
Avec submit_button l'id du bouton envoyer.

dans le ficheir main.js, j'ai ajout� le code suivant : 

$(function () {
   
         $('#datetimepicker1').datetimepicker({
 
		useCurrent: false 
	
		});
       
     $('#datetimepicker2').datetimepicker({
       
         	useCurrent: false 
      
      });

});

J'ai ajout� la lib de datetimepicker.js