<!-- # Algorand Developer Bootcamp
Sign up for future sessions on the Algorand Developer Portal Events page: [https://developer.algorand.org/events](https://developer.algorand.org/events) -->

<!-- # Active Content
Multiple Bootcamp courses may be running simultaneously. Please navigate to your appropriate series and language:
-	[Beginner (ES)](beginner-es/README.md)
-	[Intermediate (EN)](intermediate-en/README.md)

# Archived Content
Completed Bootcamp courses may be found on the [branches]( https://github.com/algorand-devrel/bootcamp/branches) page of this repo. The most recent content is listed toward the top in the following format:
**`YYYY-MM-DD-language-level`**

# Video Recordings
The [@AlgoDevs YouTube Channel](https://youtube.com/@AlgoDevs) hosts videos for each episode. Navigate to the course using the links above, then locate the episode link within the README.md file. -->

# Reto \#1

- Agregamos un boton <span style="color: magenta">Recuperar asset</span> para que el depositante pueda recuperar su asset en caso de que no haya ofertas. Una vez ejecutada esta opcion, se resetean los parámetros (**global state**) a sus valores de creación para recomenzar la subasta. Utiliza el metodo *<span style="color: lightgreen;">recover-asset</span>*
 de  <span style="color: lightgreen;">Subasta-app</span>.

-  <span style="color: magenta">Reclamar Asset</span>: agregamos la funcionalidad de que la front-end app añada el opt-in del asset a reclamar por el sender (en caso de que este no lo tuviese). Al reclamar el asset, se resetea el <span style="color: lightgreen;">asa_id</span> de la app a 0.
 
- Una vez reclamado el asset, se habilita la opción de <span style="color: magenta">Reclamar Subasta</span> para que el creador retire el monto ofertado por el asset, y se resetean los parámetros restantes (<span style="color: lightgreen">auction_end</span>, <span style="color: lightgreen">highest-bid</span>  y 
 <span style="color: lightgreen">highest-bidder</span> ) para poder recomenzar la subasta, Utiliza el metodo *<span style="color: lightgreen;">claim-rewards</span>* de la app <span style="color: lightgreen;">Subasta-app</span> y chequea tanto que el tiempo de subasta haya terminado como la existencia de un highest-bidder, ya que si no, no hay recompensa para retirar.
