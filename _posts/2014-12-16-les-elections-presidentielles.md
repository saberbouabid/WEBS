---
published: true
title: Les éléctions présidentielles tunisiennes sur Facebook 
layout: post
tags: [Politics] 
image: 
  feature: 	BCE.jpg
modified: 2014-12-16 
comment: true
share: ture
---


>Cet Article a été publié aussi sur le site nawaat.org    <a href="http://nawaat.org/portail/2014/12/16/les-elections-presidentielles-tunisiennes-sur-facebook/" class="btn btn-success"> Visitez Nawaat </a>


Dans cet article, je vais faire un Benchmark des données statistiques prises du réseau social Facebook . Rappelons qu' en Janvier 2011, la Tunisie a fait le buzz à l'échelle planétaire , à travers une révolution pacifique et légitime,  comme un résultat , le régime de dictateur Ben Ali  qui a paralysé tous les courants politiques,  a fait chute libre et Zaba a fini par s'enfuir en Arabie saoudite !


Des observateurs, des analystes et même les tunisiens avouent qu'ils ont fait une révolution à travers Facebook et Twitter avant de passer à l'action et descendre dans la rue. Bref, même l'état tunisien a su l'importance de ce réseau social et nous avons vu le ministère de l’intérieur publiait les nouvelles sur une page Facebook "officielle" comme d'autres institutions à savoir la présidence de la république.

Facebook est sans doute un espace ou la transparence règne et l'information circule d'une manière accélérée que même les médias tunisiens n'arrivent plus à le maîtriser. Alors ils ont pensé à l'utiliser comme détecteur d'incident ou événement et c'est un changement radical. Ce n'est pas nouveau pour d'autre média comme France 24 qui utilise Twitter pour ce but. Aujourd'hui , La Tunisie et après quatre ans de la révolution organise les premières élections transparentes et réelles. Les résultats de premier tour qui sont ci-dessous. montre qu'il n’y a plus le candidat de 99% :)  et c'est un bon indicateur !


<iframe src="https://dl.dropboxusercontent.com/u/63050880/graphe%20article/resultat.html" width="100%" height="450"  frameBorder="0" ></iframe>


Le deuxième  tour est donc entre  *Beji Caid Essebsi* _39,46 %_ et *Mohamed Moncef Marzouki*  _33,43%_ . Les médias sont toujours les moyens de transmission de l’information aux électeurs . Mais attention ,les campagnes électorales présidentielles ne se jouent pas seulement sur les plateaux de la télévision mais aussi avec un chevauchement instantané sur les pages Facebook et Twitter. Dans la suite, je vais essayer de répondre à quelques questions sur l'activité de deux candidats à l'élection présidentielle,en analysant leurs pages Facebook vérifiée pour Dr Mohamed Moncef Marzouki et la page officielle de Beji Caid Essebsi récemment inscrit sur ce réseau social. 


_La Première question : Qui est à la première position sur les trois volets ? Le nombre de commentaire, le nombre de j'aime et les nombres de partages ?_

J'ai utilisé  R et l'api Facebook pour analyser les pages de deux candidats. Ensuite, j'ai tronqué les données et j'ai comptabilisé que l'activité ultérieure à la date de 01/11/2014 



Tous les graphiques sont zoomables sur l'axe vertical et horizontal et vous pouvez les exporter .

<iframe src="https://dl.dropboxusercontent.com/u/63050880/graphe%20article/shares.html" width="100%" height="450" frameBorder="0" ></iframe>
<!doctype HTML>
<meta charset = 'utf-8'>
<html>
<head>
<script src='https://code.jquery.com/jquery-1.9.1.js' type='text/javascript'></script>
<script src='https://code.highcharts.com/highcharts.js' type='text/javascript'></script>
<script src='https://code.highcharts.com/highcharts-more.js' type='text/javascript'></script>
<script src='https://code.highcharts.com/modules/exporting.js' type='text/javascript'></script>
<style>

    .rChart {
      display: block;
      margin-left: auto; 
      margin-right: auto;
      width: 100%;
      height: 400px;
    }  
    </style>
    
  </head>
  <body >
    
    <div id = 'pub.html' class = 'rChart highcharts'></div>    
    <script type='text/javascript'>
    (function($){
        $(function () {
            var chart = new Highcharts.Chart({
 "dom": "pub.html",
"width":            800,
"height":            400,
"credits": {
 "enabled": "true",
"href": "http://blog.bi-statistics.com",
"text": "Bi-statistics.com" 
},
"exporting": {
 "enabled": true 
},
"title": {
 "text": "Type de publications " 
},
"yAxis": [
 {
 "title": {
 "text": "Nombre Total",
"labels": {
 "enabled": "false",
"style": {
 "fontSize": "13px",
"fontFamily": "Verdana, sans-serif" 
} 
} 
} 
} 
],
"series": [
 {
 "data": [
 [
 "link",
41 
],
[
 "photo",
315 
],
[
 "status",
15 
],
[
 "video",
107 
] 
],
"name": "Beji Caid Essebsi",
"type": "areaspline",
"marker": {
 "radius":              3 
} 
},
{
 "data": [
 [
 "link",
50 
],
[
 "photo",
185 
],
[
 "status",
180 
],
[
 "video",
181 
] 
],
"name": "Moncef Marzouki",
"type": "areaspline",
"marker": {
 "radius":              3 
} 
} 
],
"xAxis": [
 {
 "categories": [ "link", "photo", "status", "video", "link", "photo", "status", "video" ],
"labels": {
 "enabled": "false",
"align": "right",
"style": {
 "fontSize": "13px",
"fontFamily": "Verdana, sans-serif" 
} 
} 
} 
],
"subtitle": {
 "text": null 
},
"chart": {
 "zoomType": "xy",
"renderTo": "pub.html" 
},
"tooltip": {
 "shared": false,
"formatter":  function() { return  this.y +' '+ this.x ; }  
},
"id": "pub.html" 
});
        });
    })(jQuery);
</script>
    
    <script></script>    
  </body>
</html>



_les statistiques des j'aime sur la même période_

<iframe src="https://dl.dropboxusercontent.com/u/63050880/graphe%20article/like.html" width="100%" height="450" frameBorder="0" ></iframe>


_Les statistiques des commentaires :_

<iframe src="https://dl.dropboxusercontent.com/u/63050880/graphe%20article/comment.html" width="100%" height="450" frameBorder="0" ></iframe>




_La deuxième question :   Quels sont les types des publications utilisés par les CM ?_ 

La réponse est dans ce graphique qui montre une distribution équilibrée pour la page de MMM et une distribution modale autour des photos  sur la page BCE .


<iframe src="https://dl.dropboxusercontent.com/u/63050880/graphe%20article/pub.html" width="100%" height="450" frameBorder="0"></iframe>


_La troisième question : Quelles sont les publications les plus réussies sur  les trois axes like, comment , share ?_


<iframe src="https://dl.dropboxusercontent.com/u/63050880/graphe%20article/top.html" width="100%" height="450" frameBorder="0"></iframe>



Ces graphiques présentent une preuve sur l'importance de Facebook sur la scène politique tunisienne . L'utilité de communication digitale est devenue une clé de réussite qui optimise le temps et passe l'information directement à la cible ou les fans .

<iframe src="https://dl.dropboxusercontent.com/u/63050880/graphe%20article/nombrepub.html" width="100%" height="450" frameBorder="0"> </iframe>


Cette analyse peut être poussée par l'analyse sémantique des commentaires qui sera le sujet d'un prochain article.
