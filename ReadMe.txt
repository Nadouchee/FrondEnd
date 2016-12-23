
J'ai affiché le calendrier avec deux méthodes différentes:
La première méthode :

Dand le fichier "seo.contactpromo1" , pour les boutons date1 et date2, il suffit de cliquer sur
n'importe quelle zone de l'élément date1 pour afficher le calendrier afin de choisir une date.

Dans le fichier style.css, j'ai ajouté quelques modifications pour la forme des4 boutons afin qu'ils soient similaire aux autres boutons.

J'ai désactivé le choix de choisir "nombre d'adultes" ou "nombre d'enfants".

Pour que le formulaire ne doive pas pouvoir être envoyé, j'ai fait "" l'action="#" "" du formulaire.Mais il y a une autre méthode
 en javascript, il suffit d'utiliser  event.preventDefault()
 pour annuler l'envoi du formulaire :

document.getElementById("submit_button").addEventListener("click", function(event)
{
    event.preventDefault()

	

});

Avec submit_button l'id du bouton envoyer.

dans le ficheir main.js, j'ai ajouté le code suivant : 
$(function(){
		
	 $('.datepicker').datepicker();

});

----------------------------------------------------------------------------------------------
La 2ème méthode :

Dand le fichier "seo.contactpromo2" , pour les boutons date1 et date2, il faut  cliquer sur
l'icone du bouton pour afficher le calendrier afin de choisir une date(On peut choisir la date et l'heure AM ou PM).

Dans le fichier style.css, j'ai ajouté quelques modifications pour la forme des4 boutons afin qu'ils soient similaire aux autres boutons.

J'ai désactivé le choix de choisir "nombre d'adultes" ou "nombre d'enfants".

Dans le html, j'ai modifié le code des deux dates en utilisant bootsrap:
<div class="form-group">
			
	<div class='input-group date' id='datetimepicker1' >

											
		<input type='text' class="form-control" required="" placeholder="Choisir une date *" id='date1'/>
										
		<span class="input-group-addon">
										
			<span class="glyphicon glyphicon-calendar"></span>
												</span>
									
	</div>
									
</div>

Pour que le formulaire ne doive pas pouvoir être envoyé, j'ai fait "" l'action="#" "" du formulaire.Mais il y a une autre méthode
en javascript, il suffit d'utiliser  event.preventDefault()
 pour annuler l'envoi du formulaire :

document.getElementById("submit_button").addEventListener("click", function(event)
{
    event.preventDefault()

	

});
Avec submit_button l'id du bouton envoyer.

dans le ficheir main.js, j'ai ajouté le code suivant : 

$(function () {
   
         $('#datetimepicker1').datetimepicker({
 
		useCurrent: false 
	
		});
       
     $('#datetimepicker2').datetimepicker({
       
         	useCurrent: false 
      
      });

});

J'ai ajouté la lib de datetimepicker.js