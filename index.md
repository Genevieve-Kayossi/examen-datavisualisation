@@ -17,7 +17,7 @@

# Projet de datavisualisation: La consommation d'energie en France
( Image illustratif a mettre)

Comprendre et analyser la structure de la consommation d’énergie est indispensable afin de bien identifier les enjeux liés à la transition énergétique et les secteurs à cibler dans le cadre d’une stratégie bas carbone. Il s’avère que le pétrole est l’énergie la plus consommée en France (42 % de l’énergie totale consommée), principalement pour un usage de transport et de chauffage.

# Sommaire
(a definir)

## 1. Acquision et traitement des données sur la consomation d'energie en France

Les jeux de données utilisés afin d’étudier la consommation d'energie en france se trouve respectivement sur Data.gouv.fr et OpenDataSoft.fr

### Jeu de données sur Data.gouv.fr 
>[Significant consommation annuelle de gaz et d'electricité par Region et par code NAF](https://www.data.gouv.fr/fr/datasets/consommation-annuelle-delectricite-et-gaz-par-region-et-par-code-naf/#description)

Ce jeu de donnée permet de visualiser l’évolution de 2011 à 2021 des consommations d'électricité et de gaz par secteur d'activité, par catégorie de consommation, par code NAF et par région. Nous avons décidé de supprimé manuellement beaucoup de collone car étant un jeux de donnée trés lourd avec plus de 18000 lignes. Nous avons décidé d'enlevé les région comme  Guadeloupe, Reunion, Martinique car ayant des code de departement avec (02 ou 04) le fichier ne prends pas en compte le zéro et affiche toujours erreur. Nous avons donc travailler sans ces régions que nous venont de citer. Nous avons aussi utilisé Openrifine pour en extraire une partie donnée notament sur la région du Centre de val loire pour en faire un visuel.
###Extrait des données finales (DataWrapper)

<iframe title="Consommation annuelle d’électricité et gaz sur la région du Centre Val De Loire." aria-label="Table" id="datawrapper-chart-FfLRt" src="https://datawrapper.dwcdn.net/FfLRt/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="1300" data-external="1"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>

### Jeu de données sur OpenDataSoft.fr
>[Significant la répartition de la consomation d'energie en France](https://odre.opendatasoft.com/explore/dataset/repartition-de-la-consommation-denergie-primaire-en-france/table/?sort=annee&dataChart=eyJxdWVyaWVzIjpbeyJjaGFydHMiOlt7InR5cGUiOiJsaW5lIiwiZnVuYyI6IlNVTSIsInlBeGlzIjoiY2hhcmJvbiIsInNjaWVudGlmaWNEaXNwbGF5Ijp0cnVlLCJjb2xvciI6IiM2NmMyYTUifSx7ImFsaWduTW9udGgiOnRydWUsInR5cGUiOiJsaW5lIiwiZnVuYyI6IlNVTSIsInlBeGlzIjoicGV0cm9sZSIsInNjaWVudGlmaWNEaXNwbGF5Ijp0cnVlLCJjb2xvciI6IiNmYzhkNjIifSx7ImFsaWduTW9udGgiOnRydWUsInR5cGUiOiJsaW5lIiwiZnVuYyI6IlNVTSIsInlBeGlzIjoiZ2F6Iiwic2NpZW50aWZpY0Rpc3BsYXkiOnRydWUsImNvbG9yIjoiIzhkYTBjYiJ9LHsiYWxpZ25Nb250aCI6dHJ1ZSwidHlwZSI6ImxpbmUiLCJmdW5jIjoiU1VNIiwieUF4aXMiOiJlbmVyZ2llX3Jlbm91dmVsYWJsZSIsInNjaWVudGlmaWNEaXNwbGF5Ijp0cnVlLCJjb2xvciI6IiNlNzhhYzMifSx7ImFsaWduTW9udGgiOnRydWUsInR5cGUiOiJsaW5lIiwiZnVuYyI6IlNVTSIsInlBeGlzIjoiZWxlY3RyaWNpdGUiLCJzY2llbnRpZmljRGlzcGxheSI6dHJ1ZSwiY29sb3IiOiIjYTZkODU0In1dLCJ4QXhpcyI6ImFubmVlIiwibWF4cG9pbnRzIjoiIiwidGltZXNjYWxlIjoieWVhciIsInNvcnQiOiIiLCJjb25maWciOnsiZGF0YXNldCI6InJlcGFydGl0aW9uLWRlLWxhLWNvbnNvbW1hdGlvbi1kZW5lcmdpZS1wcmltYWlyZS1lbi1mcmFuY2UiLCJvcHRpb25zIjp7InNvcnQiOiJhbm5lZSJ9fX1dLCJkaXNwbGF5TGVnZW5kIjp0cnVlLCJhbGlnbk1vbnRoIjp0cnVlfQ%3D%3D)

Ce jeu de données représente l’évolution de 1990 à 2021 des consommations d’énergie primaire en France par type d’énergie. L’énergie primaire exprime le contenu énergétique de la ressource prélevée dans la nature on peut donner l'exemple du minerai fossile pour l’électricité nucléaire, du gaz naturel, du charbon, etc.)
En premier lieu nous avons fait un sanity check avec WTF csv pour voir si notre jeux de données doit etre traité avant d'etre exploité. En deuxieme nous avons modifier à la main sur openOffice le jeux de donnée pour avoir les années par ordre. En troisieme lieu nous avons utilisé DataWrapper pour avoir un jeux de données plus comprenhensible.

<iframe title="Répartition de la consommation d'énergie primaire en France." aria-label="Table" id="datawrapper-chart-yMyCA" src="https://datawrapper.dwcdn.net/yMyCA/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="1007" data-external="1"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++)
{if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
  </script>

## 2. Carte des consommations d'energie de la France par Région (DataWrapper)
  
  La consommation d'energie des regions de France est varié nous pouvons voir sur cette carte que les régions comme Bretagne, Normandie, Hat DeFrance et Centre De Val de Loire sont les pricipaux consommateurs d'energie en France. Ceci est expliquer par le fait "qu’elles sont aussi les plus équipées en chaudières électriques" Selon des études statistiques et sur nos analyses "les régions du Centre-Val de Loire", qui ont consommé le plus d'électricité en 2021. 
  
  <iframe title="La consommation d'energie par région Francaises" aria-label="Map" id="datawrapper-chart-RIQxz" src="https://datawrapper.dwcdn.net/RIQxz/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="622" data-external="1"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>
  
