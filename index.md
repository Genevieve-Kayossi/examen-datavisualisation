


# Projet de datavisualisation: La consommation d'énergie en France

![Politique de sobriété](https://media.admagazine.fr/photos/632449f823ec612145384d66/master/w_1600%2Cc_limit/GettyImages-98180138.jpg)

Comprendre et analyser la structure de la consommation d’énergie est indispensable afin de bien identifier les enjeux liés à la transition énergétique et les secteurs à cibler dans le cadre d’une stratégie bas carbone. Il s’avère que le pétrole est l’énergie la plus consommée en France (42 % de l’énergie totale consommée), principalement pour un usage de transport et de chauffage.



# Sommaire
1. [ Acquision et traitement des données sur la consomation d'énergie en France](#1- Acquision et traitement des données sur la consomation d'énergie en France)
2. [Carte des consommations d'énergie de la France par Région (DataWrapper)](#2-Carte des consommations d'énergie de la France par Région (DataWrapper))
3. [Evolution de la consommation d'energie dans le Centre De Val de Loire (Flourish)](#3-Evolution de la consommation d'energie dans le Centre De Val-De-Loire (Flourish))
4. [Evolution de la consommation par catégorie dans le Centre Val-De-Loire (Flourish)](#4-Evolution de la consommation par catégorie dans le Centre Val-De-Loire (Flourish))
5. [Evolution des consommations d'energie primaire en France de 1990 à 2021 (DataWrapper)](#5-Evolution des consommations d'energie primaire en France de 1990 à 2021 (DataWrapper))
6. [Conclusion](#6-Conclusion)


## 1. Acquision et traitement des données sur la consomation d'énergie en France

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

## 2. Carte des consommations d'énergie de la France par Région (DataWrapper)
  
  La consommation d'energie des regions de France est varié nous pouvons voir sur cette carte que les régions comme Bretagne, Normandie, Hat DeFrance et Centre De Val de Loire sont les pricipaux consommateurs d'energie en France. Ceci est expliquer par le fait "qu’elles sont aussi les plus équipées en chaudières électriques" Selon des études statistiques et sur nos analyses "les régions du Centre-Val de Loire", qui ont consommé le plus d'électricité en 2021. 
  
  <iframe title="La consommation d'energie par région Francaises" aria-label="Map" id="datawrapper-chart-RIQxz" src="https://datawrapper.dwcdn.net/RIQxz/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="622" data-external="1"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>
  
## 3. Evolution de la consommation d'energie dans le Centre De Val-De-Loire (Flourish)
  
  Avec l'outils Flourish nous avons analyser l'évolution de la Region du Centre Val de Loire entre 2018 et 2021 pour faire une analyse proportionel entre les années.
  Nous avons utilisés Pie Chart qui nous permis d'avoir une visualisation dynamique par années mais aussi par energie le plus plus utilisé par cette région.
  
  <div class="flourish-embed flourish-chart" data-src="visualisation/12576200"><script src="https://public.flourish.studio/resources/embed.js"></script></div>
  
## 4. Evolution de la consommation par catégorie dans le Centre Val-De-Loire (Flourish)
  
Nous avons utilisé Flourish pour faire un packed circle qui montre les types de consommation dans le centre Val-De-Loire. Sur le visuel il est possible de faire des filtres et voir l'évolution par année. Par exemple pour l'année 2021 nous pouvons constaté que les entreprises et résidences sont les consommateurs principales de gaz et d'electricité dans le Centre Val-De-Loire.
  
  <div class="flourish-embed flourish-hierarchy" data-src="visualisation/12679303"><script src="https://public.flourish.studio/resources/embed.js"></script></div>
  
  
 
  
## 5.  Evolution des consommations d'energie primaire en France de 1990 à 2021 (DataWrapper)
  
  Avec L'outils DataWrapper nous avons fait un diagrame pour voir l'évolution de la consomation d'energie primaire en france et nous constaté que l'utilisation du Charbon et de l'energie renuveleable reste trés faible durant ces 2O ans tandisque que l'electricité atteint son pic en 2015. Ceci dit nous pouvons aussi constater que vers les années 2010 une baisse de consommation du a la crise pétroliere.  
  
  <iframe title="Evolution des 20 dernieres années de consommation primaire énergie en France" aria-label="Interactive line chart" id="datawrapper-chart-aCD6a" src="https://datawrapper.dwcdn.net/aCD6a/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="673" data-external="1"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
</script>
  
  
## Conclusion
  

Le sujet que nous avons choisi est un sujet d'actualité de la France. Il était important pour moi de voir l'évolution de la consommation d'énergie de la France avant 2022 ou on ne parle que de politique de sobriété avec des coupures d'électricité un peu partout dans le pays. Grace à la datavisualisation nous avons pu voir les villes qui consomment le plus d'énergie mais aussi l'évolution de la consommation d'énergie dans dans les régions.
  
En sommes nous pouvons dire que la datavisualisation est d'une importance capitale dans la mesure ou elle permet à simplifier la lecture et la compréhension de données complexes en les imageant.Il faut considerer la datavisualisation comme un outil efficient et efficace de communication. Parce que cette méthode est ergonomique, simple et fonctionnelle, elle est percutante. En effet nous avons avec notre jeux de données fais sortir plusieurs informations sur la consommation d'energie en France. Sans la datavisualisation des données ces deux jeux de données seront tres penible a lire et à comprendre. 
  
Ceci dit nous avons eu beaucoup de difficultés pour finir ce projet notament pour faire le sanity check mais aussi pour faire des visuels parlant et qui répondent à nos questions surtout avec Flourish ou on devait modifier nos données ou encore le retravailler pour avoir un visuel.
Avec WikiData malheuresement nous n'avons pas eu la possibilité de trouver une requete qui illustre notre théme d'analyse.
