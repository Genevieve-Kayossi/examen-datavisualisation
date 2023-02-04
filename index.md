@@ -17,7 +17,7 @@

# Projet de datavisualisation: La consommation d'energie en France
( Image illustratif a mettre)

Comprendre et analyser la structure de la consommation d’énergie est indispensable afin de bien identifier les enjeux liés à la transition énergétique et les secteurs à cibler dans le cadre d’une stratégie bas carbone. Il s’avère que le pétrole est l’énergie la plus consommée en France (42 % de l’énergie totale consommée), principalement pour un usage de transport et de chauffage.

# Sommaire
(a definir)

## 1. Acquision et traitement des données sur la consomation d'energie en France
Le jeu de données utilisé afin d’étudier la consommation d'energie en france ce trouve sur OpenDataSoft:

>[Significant la répartition de la consomation d'energie en France](https://odre.opendatasoft.com/explore/dataset/repartition-de-la-consommation-denergie-primaire-en-france/table/?sort=annee&dataChart=eyJxdWVyaWVzIjpbeyJjaGFydHMiOlt7InR5cGUiOiJsaW5lIiwiZnVuYyI6IlNVTSIsInlBeGlzIjoiY2hhcmJvbiIsInNjaWVudGlmaWNEaXNwbGF5Ijp0cnVlLCJjb2xvciI6IiM2NmMyYTUifSx7ImFsaWduTW9udGgiOnRydWUsInR5cGUiOiJsaW5lIiwiZnVuYyI6IlNVTSIsInlBeGlzIjoicGV0cm9sZSIsInNjaWVudGlmaWNEaXNwbGF5Ijp0cnVlLCJjb2xvciI6IiNmYzhkNjIifSx7ImFsaWduTW9udGgiOnRydWUsInR5cGUiOiJsaW5lIiwiZnVuYyI6IlNVTSIsInlBeGlzIjoiZ2F6Iiwic2NpZW50aWZpY0Rpc3BsYXkiOnRydWUsImNvbG9yIjoiIzhkYTBjYiJ9LHsiYWxpZ25Nb250aCI6dHJ1ZSwidHlwZSI6ImxpbmUiLCJmdW5jIjoiU1VNIiwieUF4aXMiOiJlbmVyZ2llX3Jlbm91dmVsYWJsZSIsInNjaWVudGlmaWNEaXNwbGF5Ijp0cnVlLCJjb2xvciI6IiNlNzhhYzMifSx7ImFsaWduTW9udGgiOnRydWUsInR5cGUiOiJsaW5lIiwiZnVuYyI6IlNVTSIsInlBeGlzIjoiZWxlY3RyaWNpdGUiLCJzY2llbnRpZmljRGlzcGxheSI6dHJ1ZSwiY29sb3IiOiIjYTZkODU0In1dLCJ4QXhpcyI6ImFubmVlIiwibWF4cG9pbnRzIjoiIiwidGltZXNjYWxlIjoieWVhciIsInNvcnQiOiIiLCJjb25maWciOnsiZGF0YXNldCI6InJlcGFydGl0aW9uLWRlLWxhLWNvbnNvbW1hdGlvbi1kZW5lcmdpZS1wcmltYWlyZS1lbi1mcmFuY2UiLCJvcHRpb25zIjp7InNvcnQiOiJhbm5lZSJ9fX1dLCJkaXNwbGF5TGVnZW5kIjp0cnVlLCJhbGlnbk1vbnRoIjp0cnVlfQ%3D%3D)

Ce jeu de données représente l’évolution de 1990 à 2021 des consommations d’énergie primaire en France par type d’énergie. L’énergie primaire exprime le contenu énergétique de la ressource prélevée dans la nature on peut donner l'exemple du minerai fossile pour l’électricité nucléaire, du gaz naturel, du charbon, etc.)
En premier lieu nous avons fait un sanity check avec WTF csv pour voir si notre jeux de données doit etre traité avant d'etre exploité. En deuxieme nous avons modifier à la main sur openOffice le jeux de donnée pour avoir les années par ordre. En troisieme lieu nous avons utilisé DataWrapper pour avoir un jeux de données plus comprenhensible.

<iframe title="Répartition de la consommation d'énergie primaire en France." aria-label="Table" id="datawrapper-chart-yMyCA" src="https://datawrapper.dwcdn.net/yMyCA/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="1007" data-external="1"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(e){if(void 0!==e.data["datawrapper-height"]){var t=document.querySelectorAll("iframe");for(var a in e.data["datawrapper-height"])for(var r=0;r<t.length;r++){if(t[r].contentWindow===e.source)t[r].style.height=e.data["datawrapper-height"][a]+"px"}}}))}();
  </script>
