<!-- This is the format for text comments that will be ignored during renderings. Do not put R code in these comments because it will not be ignored. -->
<!-- With the following code you can access and display values from the yml header above. -->

Keywords:

Highlights:

<!-- The following code chunk defines some general settings how code chunks should behave. -->

    ## Warning: package 'kableExtra' was built under R version 4.0.2

Datengrundlage
==============

Daten als csv bekommen und IPs etc entfernt. Insgesamt über 600
Antworten, dabei aber viele, die sich “nur durchgeklickt” haben oder nur
Teile der Umfrage ausgefüllt haben (teilweise um die 70%).

Demographische Angaben
======================

Alter und Beschäftigungsverhältnis
----------------------------------

Zuerst einige allgemeine Statistiken zu der Teilnehmergruppe:

![](../figures/fig_alter_einrichtung-1.png) Wir haben knapp 50
20-29jährige, der Großteil der befragten ist zwischen 30 udn 60 Jahre
alt und arbeitet an einer Hochschule, in der Forschung, im Museum oder
in einer Denkmalbehörde (man beachte die über 80jährige Person, die
nicht mehr arbeitet…). Seltener kommen Grabungsfirmen und Archive vor.

Alter und Gruppe
----------------

Innerhalb der Altersstufen teilen sich die Menschen auf folgende Gruppen
auf:

![](../figures/fig_einrichtung_gruppe-1.png) Das Gros besteht aus
wissenschaftlichen Mitarbeiterinnen an der Hochschule und in
Forschungseinrichtungen.

Alter und Erfahrung + Wichtung
==============================

Gibt es einen Zusammenhang zwischen dem Alter der Teilnehmenden Person,
der Erfahrung die sie in digitalen Forschungsdatenmanagement hat und dem
Gewicht, dass sie dem sie ihm zuweist?

![](../figures/fig_erfahrung_gruppe-1.png) Alle Altersgruppen haben sehr
gemischt Erfahrungen und Wissensstände mit digitalem Datenmanagement.
Bei den Senioren (70-79) lassen sich zwei Gruppen differenzieren (viel
Ahnung - wenig Ahnung), sie halten digitales Forschungsdatenmanagement
allgemein für weniger wichtig für ihre tägliche Arbeit.

Jüngere Teilnehmende schätzen ihre eigene Erfahrung deutlich geringer
ein als diejenigen “die im Beruf stehen” und zwischen 30 und 60 Jahre
alt sind. Diese Gruppe scheint dem digitalen FDM auch den höchsten
Stellenwert in ihrer täglichen Arbeit zuzuweisen.

Wer viel von Forschungsdatenmanagement hält, scheint sich häufig schon
recht gut weitergebildet zu haben (oder anders herum: Einschätzung der
Wichtigkeit kommt von eigener Erfahrung!). Nur wenige Personen geben an,
ihre Erfahrung als mittig einzuschätzen, wenn sie FDM für wichtig halten
und die gelben Punkte (sehr hoher Stellenwert des digitalen FDM für die
eigene Arbeit) häufen sich im Bereich "viel Erfahrung).

Diese Ergebnisse sollten statistische getestet werden:

### Test: Alter - Erfahrung mit spearmans rho

Für den Test werden die Teilnehmer entfernt, die keine Altersangabe
gemacht haben.

Es bleiben für den Vergleich 850 Teilnehmer.

    #> 
    #>  Spearman's rank correlation rho
    #> 
    #> data:  age_group2$beginn and age_group2$erfahrung_digfdm
    #> S = 99630634, p-value = 0.2743
    #> alternative hypothesis: true rho is not equal to 0
    #> sample estimates:
    #>         rho 
    #> -0.03794608

Nach der Berechnung des Tests lässt sich keine signifikante Korrelation
zwischen Alter und Erfahrung feststellen, somit besteht kein linearer
Zusammenhang zwischen Alter und Erfahrung mit digitalem FDM. Dies
überrascht nicht, da die älteren Kolleg\*innen vmtl weniger Kontakt
bisher damit hatten.

Aus diesem Grund wird die Vermutung eines linearen Zusammenhangs
aufgegeben und nur ein Vergleich der verschiedenen Gruppen (kategorial)
geführt:

### Test: Alter - Erfahrung mit chi²

Der Chi-Quadrat-Test darf eigentlich für diese Daten nicht angewendet
werden, da die Erwartungswerte zu gering werden (Anzahl der Teilnehmer
muss auf zu viele Subgruppen aufgeteilt werden). Anhang der Residuen
lassen sich trotzdem Erkenntnisse erarbeiten:
<table>
<thead>
<tr>
<th style="text-align:left;">
</th>
<th style="text-align:right;">
0
</th>
<th style="text-align:right;">
1
</th>
<th style="text-align:right;">
2
</th>
<th style="text-align:right;">
3
</th>
<th style="text-align:right;">
4
</th>
<th style="text-align:right;">
5
</th>
<th style="text-align:right;">
6
</th>
<th style="text-align:right;">
7
</th>
<th style="text-align:right;">
8
</th>
<th style="text-align:right;">
9
</th>
<th style="text-align:right;">
10
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
20-29
</td>
<td style="text-align:right;">
3.7803715
</td>
<td style="text-align:right;">
0.7163280
</td>
<td style="text-align:right;">
0.7161859
</td>
<td style="text-align:right;">
-0.5587377
</td>
<td style="text-align:right;">
0.5136689
</td>
<td style="text-align:right;">
1.8344985
</td>
<td style="text-align:right;">
-0.8132230
</td>
<td style="text-align:right;">
-0.0946490
</td>
<td style="text-align:right;">
-1.4080190
</td>
<td style="text-align:right;">
-1.5119790
</td>
<td style="text-align:right;">
-0.6023567
</td>
</tr>
<tr>
<td style="text-align:left;">
30-39
</td>
<td style="text-align:right;">
-1.4357282
</td>
<td style="text-align:right;">
-2.0343612
</td>
<td style="text-align:right;">
-0.9246371
</td>
<td style="text-align:right;">
-0.4177876
</td>
<td style="text-align:right;">
-2.1144043
</td>
<td style="text-align:right;">
0.2360961
</td>
<td style="text-align:right;">
0.0875959
</td>
<td style="text-align:right;">
1.8062580
</td>
<td style="text-align:right;">
1.6510160
</td>
<td style="text-align:right;">
-1.0991788
</td>
<td style="text-align:right;">
0.0220848
</td>
</tr>
<tr>
<td style="text-align:left;">
40-49
</td>
<td style="text-align:right;">
-0.9855187
</td>
<td style="text-align:right;">
-0.2163476
</td>
<td style="text-align:right;">
0.9926926
</td>
<td style="text-align:right;">
0.0320451
</td>
<td style="text-align:right;">
0.7735451
</td>
<td style="text-align:right;">
-1.8993041
</td>
<td style="text-align:right;">
2.3356071
</td>
<td style="text-align:right;">
-1.5684687
</td>
<td style="text-align:right;">
-0.3903671
</td>
<td style="text-align:right;">
1.5941161
</td>
<td style="text-align:right;">
0.3548404
</td>
</tr>
<tr>
<td style="text-align:left;">
50-59
</td>
<td style="text-align:right;">
0.9290039
</td>
<td style="text-align:right;">
1.1015447
</td>
<td style="text-align:right;">
-1.3119447
</td>
<td style="text-align:right;">
-0.6888301
</td>
<td style="text-align:right;">
1.2118019
</td>
<td style="text-align:right;">
0.5362489
</td>
<td style="text-align:right;">
-1.6494430
</td>
<td style="text-align:right;">
-0.4188121
</td>
<td style="text-align:right;">
-0.0400150
</td>
<td style="text-align:right;">
0.6535173
</td>
<td style="text-align:right;">
0.9429166
</td>
</tr>
<tr>
<td style="text-align:left;">
60-69
</td>
<td style="text-align:right;">
-0.3268602
</td>
<td style="text-align:right;">
1.9568590
</td>
<td style="text-align:right;">
1.0764170
</td>
<td style="text-align:right;">
1.6359643
</td>
<td style="text-align:right;">
0.5108449
</td>
<td style="text-align:right;">
0.5778127
</td>
<td style="text-align:right;">
-0.2529239
</td>
<td style="text-align:right;">
0.0166945
</td>
<td style="text-align:right;">
-1.0840727
</td>
<td style="text-align:right;">
-0.9621024
</td>
<td style="text-align:right;">
-1.4783806
</td>
</tr>
<tr>
<td style="text-align:left;">
70-79
</td>
<td style="text-align:right;">
-0.3922323
</td>
<td style="text-align:right;">
-0.4160251
</td>
<td style="text-align:right;">
2.0549780
</td>
<td style="text-align:right;">
2.4243808
</td>
<td style="text-align:right;">
-0.6650622
</td>
<td style="text-align:right;">
-1.1094004
</td>
<td style="text-align:right;">
-0.9250780
</td>
<td style="text-align:right;">
-0.2838067
</td>
<td style="text-align:right;">
-0.5321812
</td>
<td style="text-align:right;">
1.8735678
</td>
<td style="text-align:right;">
-0.7783118
</td>
</tr>
</tbody>
</table>

die größten Abweichungen gibt es bei der Altersgruppe der 20-29jährigen
im Bereich “Erfahrung = 0”, dort sind sie überrepräsentiert, ebenso wie
die Altersgruppen 60-69 und 70-70 im Bereich der niedrigen
Erfahrungswerte 1-3 überrepräsentiert sind.

    #> [1] 0.1557093

Cramers V ergibt einen Wert von 0,16, was auf einen schwachen
Zusammenhang zwischen Altersgruppe und Erfahrung schließen lässt.

–\> Conclusio: Ältere und junge haben wenig Erfahrung. Das ist nicht
allzu überraschend.

Als nächstes kann die Gewichtung für die eigene Arbeit untersucht
werden:

### Test: Alter - Wichtung mit spearmans rho

    #> 
    #>  Spearman's rank correlation rho
    #> 
    #> data:  rank(age_group[, 1]) and age_group[, 8]
    #> S = 111667326, p-value = 2.176e-06
    #> alternative hypothesis: true rho is not equal to 0
    #> sample estimates:
    #>        rho 
    #> -0.1633436

Je älter, desto weniger wichtig. Schwacher, aber höchstsignifikanter
Zusammenhang.

### Test: Alter - Wichtung mit Chi²

Wie oben kann auch hier nur mit den Residualwerten gearbeitet werden.

    #>               age_group[, 8]
    #> age_group[, 1]           0           1           2           3           4
    #>          20-29 -0.25943726 -0.63548891 -0.24657867  1.01551156 -0.91420749
    #>          30-39 -0.57596074  0.71562822 -1.31559957 -1.14357421  0.59543767
    #>          40-49 -0.49759035 -0.39839187  1.98053478 -0.47826645 -0.30596170
    #>          50-59  1.46460302  0.36765411 -0.40124627 -0.16968540 -1.07119833
    #>          60-69 -0.29417420 -0.72057669  0.27745145  1.24860606  1.63430113
    #>          70-79 -0.09805807 -0.24019223 -0.42742521  3.58892527  1.11132477
    #>               age_group[, 8]
    #> age_group[, 1]           5           6           7           8           9
    #>          20-29  1.06090576 -0.19917412  0.29738600 -3.38657493  0.67666495
    #>          30-39 -2.56256150 -1.37171824 -0.92235505  0.73669310  2.72490066
    #>          40-49  0.16873391 -0.39215848  0.29282650  0.81607905 -1.23128762
    #>          50-59  1.83349695  0.87542636 -0.29005027 -0.02587174 -1.05574893
    #>          60-69 -0.00858377  2.24653579  1.55781939  0.18768111 -1.67093471
    #>          70-79  1.93134826 -0.69337525 -0.02843889  0.06256037 -1.07417231
    #>               age_group[, 8]
    #> age_group[, 1]          10
    #>          20-29  2.33460911
    #>          30-39  0.35915555
    #>          40-49 -0.17194282
    #>          50-59  0.09886962
    #>          60-69 -2.16694124
    #>          70-79 -1.42437571

Auffällig ist hier die Altersgruppe der 20-29jährigen, die dem digitalen
FDM eine höhere Bedeutung zuweist als erwartet. Ältere Semester tun das
wenig überraschender weise gegenteilig.

    #> [1] 0.1553697

Anhand Cramers V \~ 0,16 lässt sich wieder ein schwacher Zusammenhang
zwischen Alter und Gewichtung festhalten.

Korreliert die Einschätzung der Wichtigkeit und die Erfahrung und lassen sich darin Gruppen unterscheiden?
----------------------------------------------------------------------------------------------------------

Für diese Frage werden die beiden Werte Einschätzung der Wichtigkeit für
das eigene Arbeiten und die eigene Erfahrung gegeneinander plotten. Da
in beiden Fällen keine stetigen metrischen Werte vorliegen, sondern nur
mit diskreten Werten gearbeitet wurde, muss für die Visualisierung ein
“jitter-Effekt” eingesetzt werden, der die Punkte ein wenig verschiebt,
damit nicht alle direkt übereinander liegen.

Allgemein kann der Zusammenhang bestätigt werden (eingezeichnet blaue
Linie ist lineare Regression mit Konfidenzintervall). Verschiedene
Einfärbungen werden nun getestet:

### Gruppenzugehörigkeit

![](../figures/fig_gruppe-1.png) m. E. lässt sich kein Zusammenhang
zwischen der Zugehörigkeit zu einer Gruppe und der Wichtung / Erfahrung
im digitalen FDM finden.

Auffällig ist der/die einsame Studierende oben links in der Ecke,
der/die die Bedeutung von FDM sehr hoch einschätzt, aber selber
überhaupt keine Erfahrung hat. Kann dieser Person jemand bitte ganz
schnell einen Datenbankenkurs anbieten?

Der Bereich “hat selber wenig Erfahrung, schätzt aber die Bedeutung für
die eigene Arbeit hoch ein” (also Einschätzung Bedeutung FDM 6-10 und
Einschätzung eigene Erfahrung FDM 0-4) ist eine Zielgruppe für uns: Das
sind die Personen, die wissen, dass sie sich fortbilden müssen, denen
aber evtl einfach das Angebot fehlt. Es sind darin alle Gruppen
vertreten, außer Daten- und IT-Beautragte.

### Blickwinkel der Antwortenden

![](../figures/fig_blickwinkel-1.png) Institutionen und Individuen
zeigen keine Musterungen.

### Einrichtungen

![](../figures/fig_einrichtungen-1.png) Eventuell zeigen sich
Grabungsfirmen insbesondere in dem höherschätzenden Bereich. Es zeigt
sich bei allen Einrichtungen eine große Heterogenität.

### Teststatistiken zu dem Zusammenhang eigenes Wissen und Bedeutung

    #> 
    #> Call:
    #> lm(formula = erfahrung_digfdm ~ stellenwert_digfdm, data = erfahrung_group)
    #> 
    #> Residuals:
    #>     Min      1Q  Median      3Q     Max 
    #> -7.7089 -1.4109  0.2381  1.5626  7.4831 
    #> 
    #> Coefficients:
    #>                    Estimate Std. Error t value Pr(>|t|)    
    #> (Intercept)         1.21895    0.24708   4.934 9.72e-07 ***
    #> stellenwert_digfdm  0.64900    0.03105  20.900  < 2e-16 ***
    #> ---
    #> Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    #> 
    #> Residual standard error: 1.989 on 849 degrees of freedom
    #>   (18 observations deleted due to missingness)
    #> Multiple R-squared:  0.3397, Adjusted R-squared:  0.3389 
    #> F-statistic: 436.8 on 1 and 849 DF,  p-value: < 2.2e-16

R² \~ 0,34: moderater Zusammenhang zwischen eigener Erfahrung und dem
Stellenwert der dem digitalen FDM zugeschrieben wird.

### Gibt es eine Trennung zwischen Menschen mit viel und wenig Ahnung?

Hier ist es sinnvoll, sich einfach die Verteilung anzuschauen. Ist sie
normalverteilt? ![](../figures/fig_verteilung_erfahrung-1.png)

Die Erfahrung mit digitalem Datenmanagement in unserer Umfrage ist
nicht-normalverteilt, sondern nach rechts verschoben:

-   Median = 6
-   Mittelwert = 6.0018484
-   Modus = 8

Hier kann sich zeigen, dass wir vor allem Leute erreicht haben, die sich
mit dem Thema schon beschäftigt haben. Es gibt einen deutlichen Anstieg
zwischen der Einschätzung “4” und “5”. Hier lassen sich eventuell zwei
Gruppen unterscheiden.

Welche Arbeitgeber haben ein Richtlinienkatalog?
================================================

<table class="table table-striped table-hover" style="margin-left: auto; margin-right: auto;">
<thead>
<tr>
<th style="text-align:left;">
</th>
<th style="text-align:right;">
ja
</th>
<th style="text-align:right;">
nein
</th>
<th style="text-align:right;">
weiß nicht
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Archiv
</td>
<td style="text-align:right;">
4
</td>
<td style="text-align:right;">
1
</td>
<td style="text-align:right;">
2
</td>
</tr>
<tr>
<td style="text-align:left;">
Außeruniversitäre Forschungseinrichtung
</td>
<td style="text-align:right;">
66
</td>
<td style="text-align:right;">
36
</td>
<td style="text-align:right;">
24
</td>
</tr>
<tr>
<td style="text-align:left;">
Denkmalbehörde
</td>
<td style="text-align:right;">
24
</td>
<td style="text-align:right;">
23
</td>
<td style="text-align:right;">
18
</td>
</tr>
<tr>
<td style="text-align:left;">
Forschungsverbund
</td>
<td style="text-align:right;">
3
</td>
<td style="text-align:right;">
5
</td>
<td style="text-align:right;">
2
</td>
</tr>
<tr>
<td style="text-align:left;">
Grabungsfirma
</td>
<td style="text-align:right;">
15
</td>
<td style="text-align:right;">
1
</td>
<td style="text-align:right;">
1
</td>
</tr>
<tr>
<td style="text-align:left;">
keiner
</td>
<td style="text-align:right;">
1
</td>
<td style="text-align:right;">
3
</td>
<td style="text-align:right;">
10
</td>
</tr>
<tr>
<td style="text-align:left;">
Museum
</td>
<td style="text-align:right;">
24
</td>
<td style="text-align:right;">
67
</td>
<td style="text-align:right;">
32
</td>
</tr>
<tr>
<td style="text-align:left;">
Sonstiges
</td>
<td style="text-align:right;">
7
</td>
<td style="text-align:right;">
7
</td>
<td style="text-align:right;">
12
</td>
</tr>
<tr>
<td style="text-align:left;">
Universität/Hochschule
</td>
<td style="text-align:right;">
60
</td>
<td style="text-align:right;">
53
</td>
<td style="text-align:right;">
55
</td>
</tr>
</tbody>
</table>

Für die Analyse, ob es hier nennenswerte Unterschiede gibt, entfernen
wir die Angaben “weiß nicht”:

<table>
<thead>
<tr>
<th style="text-align:left;">
</th>
<th style="text-align:right;">
ja
</th>
<th style="text-align:right;">
nein
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Archiv
</td>
<td style="text-align:right;">
0.9080252
</td>
<td style="text-align:right;">
-0.9263710
</td>
</tr>
<tr>
<td style="text-align:left;">
Außeruniversitäre Forschungseinrichtung
</td>
<td style="text-align:right;">
1.9383045
</td>
<td style="text-align:right;">
-1.9774661
</td>
</tr>
<tr>
<td style="text-align:left;">
Denkmalbehörde
</td>
<td style="text-align:right;">
0.0061276
</td>
<td style="text-align:right;">
-0.0062514
</td>
</tr>
<tr>
<td style="text-align:left;">
Forschungsverbund
</td>
<td style="text-align:right;">
-0.5346797
</td>
<td style="text-align:right;">
0.5454824
</td>
</tr>
<tr>
<td style="text-align:left;">
Grabungsfirma
</td>
<td style="text-align:right;">
2.3944789
</td>
<td style="text-align:right;">
-2.4428571
</td>
</tr>
<tr>
<td style="text-align:left;">
keiner
</td>
<td style="text-align:right;">
-0.7281456
</td>
<td style="text-align:right;">
0.7428571
</td>
</tr>
<tr>
<td style="text-align:left;">
Museum
</td>
<td style="text-align:right;">
-3.2895468
</td>
<td style="text-align:right;">
3.3560090
</td>
</tr>
<tr>
<td style="text-align:left;">
Sonstiges
</td>
<td style="text-align:right;">
-0.0523937
</td>
<td style="text-align:right;">
0.0534522
</td>
</tr>
<tr>
<td style="text-align:left;">
Universität/Hochschule
</td>
<td style="text-align:right;">
0.3121936
</td>
<td style="text-align:right;">
-0.3185012
</td>
</tr>
</tbody>
</table>

Chi nur eingeschränkt nutzbar, weil die Voraussetzungen nicht 100%
erfüllt. Grabungsfirmen und außeruniversitäre Forschungseinrichrungen
haben häufiger einen Richtlinienkatalog als zu erwarten währen, während
insbesondere Museen keine haben.

Acknowledgements
================

<!-- The following line inserts a page break  -->
References
==========

<!-- The following line ensures the references appear here for the MS Word or HTML output files, rather than right at the end of the document (this will not work for PDF files):  -->

### Colophon

This report was generated on 2020-07-31 17:33:20 using the following
computational environment and dependencies:

    #> - Session info ---------------------------------------------------------------
    #>  setting  value                       
    #>  version  R version 4.0.0 (2020-04-24)
    #>  os       Windows 7 x64 SP 1          
    #>  system   x86_64, mingw32             
    #>  ui       RTerm                       
    #>  language (EN)                        
    #>  collate  German_Germany.1252         
    #>  ctype    German_Germany.1252         
    #>  tz       Europe/Berlin               
    #>  date     2020-07-31                  
    #> 
    #> - Packages -------------------------------------------------------------------
    #>  package     * version date       lib source        
    #>  assertthat    0.2.1   2019-03-21 [1] CRAN (R 4.0.0)
    #>  backports     1.1.6   2020-04-05 [1] CRAN (R 4.0.0)
    #>  callr         3.4.3   2020-03-28 [1] CRAN (R 4.0.0)
    #>  cli           2.0.2   2020-02-28 [1] CRAN (R 4.0.0)
    #>  colorspace    1.4-1   2019-03-18 [1] CRAN (R 4.0.0)
    #>  crayon        1.3.4   2017-09-16 [1] CRAN (R 4.0.0)
    #>  desc          1.2.0   2018-05-01 [1] CRAN (R 4.0.0)
    #>  devtools      2.3.1   2020-07-21 [1] CRAN (R 4.0.2)
    #>  digest        0.6.25  2020-02-23 [1] CRAN (R 4.0.0)
    #>  dplyr       * 1.0.0   2020-05-29 [1] CRAN (R 4.0.0)
    #>  ellipsis      0.3.0   2019-09-20 [1] CRAN (R 4.0.0)
    #>  evaluate      0.14    2019-05-28 [1] CRAN (R 4.0.0)
    #>  fansi         0.4.1   2020-01-08 [1] CRAN (R 4.0.0)
    #>  farver        2.0.3   2020-01-16 [1] CRAN (R 4.0.0)
    #>  fs            1.4.2   2020-06-30 [1] CRAN (R 4.0.2)
    #>  generics      0.0.2   2018-11-29 [1] CRAN (R 4.0.0)
    #>  ggplot2     * 3.3.0   2020-03-05 [1] CRAN (R 4.0.0)
    #>  glue          1.4.1   2020-05-13 [1] CRAN (R 4.0.2)
    #>  gridExtra     2.3     2017-09-09 [1] CRAN (R 4.0.0)
    #>  gtable        0.3.0   2019-03-25 [1] CRAN (R 4.0.0)
    #>  highr         0.8     2019-03-20 [1] CRAN (R 4.0.0)
    #>  hms           0.5.3   2020-01-08 [1] CRAN (R 4.0.0)
    #>  htmltools     0.4.0   2019-10-04 [1] CRAN (R 4.0.0)
    #>  httr          1.4.2   2020-07-20 [1] CRAN (R 4.0.2)
    #>  kableExtra  * 1.1.0   2019-03-16 [1] CRAN (R 4.0.2)
    #>  knitr         1.28    2020-02-06 [1] CRAN (R 4.0.0)
    #>  labeling      0.3     2014-08-23 [1] CRAN (R 4.0.0)
    #>  lattice       0.20-41 2020-04-02 [2] CRAN (R 4.0.0)
    #>  lifecycle     0.2.0   2020-03-06 [1] CRAN (R 4.0.0)
    #>  lsr         * 0.5     2015-03-02 [1] CRAN (R 4.0.0)
    #>  magrittr      1.5     2014-11-22 [1] CRAN (R 4.0.0)
    #>  Matrix        1.2-18  2019-11-27 [2] CRAN (R 4.0.0)
    #>  memoise       1.1.0   2017-04-21 [1] CRAN (R 4.0.0)
    #>  mgcv          1.8-31  2019-11-09 [2] CRAN (R 4.0.0)
    #>  munsell       0.5.0   2018-06-12 [1] CRAN (R 4.0.0)
    #>  nlme          3.1-147 2020-04-13 [2] CRAN (R 4.0.0)
    #>  pillar        1.4.3   2019-12-20 [1] CRAN (R 4.0.0)
    #>  pkgbuild      1.0.7   2020-04-25 [1] CRAN (R 4.0.0)
    #>  pkgconfig     2.0.3   2019-09-22 [1] CRAN (R 4.0.0)
    #>  pkgload       1.0.2   2018-10-29 [1] CRAN (R 4.0.0)
    #>  prettyunits   1.1.1   2020-01-24 [1] CRAN (R 4.0.0)
    #>  processx      3.4.2   2020-02-09 [1] CRAN (R 4.0.0)
    #>  ps            1.3.2   2020-02-13 [1] CRAN (R 4.0.0)
    #>  purrr         0.3.4   2020-04-17 [1] CRAN (R 4.0.0)
    #>  R6            2.4.1   2019-11-12 [1] CRAN (R 4.0.0)
    #>  Rcpp          1.0.4.6 2020-04-09 [1] CRAN (R 4.0.0)
    #>  readr         1.3.1   2018-12-21 [1] CRAN (R 4.0.2)
    #>  remotes       2.2.0   2020-07-21 [1] CRAN (R 4.0.2)
    #>  rlang         0.4.7   2020-07-09 [1] CRAN (R 4.0.2)
    #>  rmarkdown     2.3     2020-06-18 [1] CRAN (R 4.0.2)
    #>  rprojroot     1.3-2   2018-01-03 [1] CRAN (R 4.0.0)
    #>  rstudioapi    0.11    2020-02-07 [1] CRAN (R 4.0.0)
    #>  rvest         0.3.5   2019-11-08 [1] CRAN (R 4.0.0)
    #>  scales        1.1.0   2019-11-18 [1] CRAN (R 4.0.0)
    #>  sessioninfo   1.1.1   2018-11-05 [1] CRAN (R 4.0.0)
    #>  stringi       1.4.6   2020-02-17 [1] CRAN (R 4.0.0)
    #>  stringr     * 1.4.0   2019-02-10 [1] CRAN (R 4.0.0)
    #>  testthat      2.3.2   2020-03-02 [1] CRAN (R 4.0.0)
    #>  tibble        3.0.0   2020-03-30 [1] CRAN (R 4.0.0)
    #>  tidyr       * 1.0.3   2020-05-07 [1] CRAN (R 4.0.0)
    #>  tidyselect    1.1.0   2020-05-11 [1] CRAN (R 4.0.0)
    #>  usethis       1.6.1   2020-04-29 [1] CRAN (R 4.0.0)
    #>  vctrs         0.3.1   2020-06-05 [1] CRAN (R 4.0.2)
    #>  viridis     * 0.5.1   2018-03-29 [1] CRAN (R 4.0.0)
    #>  viridisLite * 0.3.0   2018-02-01 [1] CRAN (R 4.0.0)
    #>  webshot       0.5.2   2019-11-22 [1] CRAN (R 4.0.2)
    #>  withr         2.2.0   2020-04-20 [1] CRAN (R 4.0.0)
    #>  xfun          0.14    2020-05-20 [1] CRAN (R 4.0.0)
    #>  xml2          1.3.1   2020-04-09 [1] CRAN (R 4.0.0)
    #>  yaml          2.2.1   2020-02-01 [1] CRAN (R 4.0.0)
    #> 
    #> [1] C:/Users/SCSchmidt/Documents/R/win-library/4.0
    #> [2] C:/Program Files/R/R-4.0.0/library

The current Git commit details are:

    #> Local:    gh-page E:/R/N4Oumfrage
    #> Remote:   gh-page @ origin (https://github.com/SCSchmidt/N4Oumfrage)
    #> Head:     [7cbe4e5] 2020-07-31: Auslagerung d. Software- und Datenauswertung
