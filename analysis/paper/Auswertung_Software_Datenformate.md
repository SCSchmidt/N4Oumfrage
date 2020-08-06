<!-- This is the format for text comments that will be ignored during renderings. Do not put R code in these comments because it will not be ignored. -->
<!-- With the following code you can access and display values from the yml header above. -->

Keywords: Auswertung Umfrage, Software, Datenformate

Highlights: Anbieter benutzter Projektmanagement-Software: v.a.
Microsoft und Atlassian, aber auch sehr spezialisiert, meist genannte
Forschungsdatenauswertende Programme: QGIS und Excel

<!-- The following code chunk defines some general settings how code chunks should behave. -->

Datengrundlage
==============

Daten als csv bekommen und IPs etc entfernt. Insgesamt über 600
Antworten, dabei aber viele, die sich “nur durchgeklickt” haben oder nur
Teile der Umfrage ausgefüllt haben (teilweise um die 70%).

Analyse der Software, die für Projektmanagement genutzt wird
============================================================

Häufigkeit der genannten Anbieter und ob dies freie oder proprietäre
Software ist:

![](../figures/softw_projmanagement-1.png) Lösungen von Atlassian und
Microsoft sind besonders beliebt. Einige nutzen selbstprogrammierte
Lösungen. Versionskontrolle ist relativ bekannt.

Analyse Software, die für Forschungsdatenanalyse genutzt wird
=============================================================

Visualisierung der Häufigkeiten der Nennung (bis zu sieben Nennungen pro
Person)

![](../figures/dienste_häufigkeiten-1.png) Zwei Programme werden extrem
häufig genannt: Excel und QGIS. Access ist das bekannteste
Datenbanksystem. Die beiden hervorgehobenen Punkte “eigene” und “keine”
sollen im Folgenden etwas im Detail analysiert werden: Wer programmiert
eigene Lösungen und wer benutzt gar keine Analysesoftware?

### eigen programmierte Lösungen

    #>  [1] "MS Excel, Sparql, selbstgebauter Datenbankabfrage "                                                                                       
    #>  [2] "oXygen XML Editor\nselbstgeschriebene Software\nMS Excel"                                                                                 
    #>  [3] "R, ADP, selbstentwickelte Python-Applikationen"                                                                                           
    #>  [4] "eigene Software"                                                                                                                          
    #>  [5] "QGIS, eigene software Open Source"                                                                                                        
    #>  [6] "MS Excel, QGIS, eigene Entwicklungen zur Datenbankauswertung"                                                                             
    #>  [7] "MS Excel, QGIS  für die tägliche Arbeit / eigene Forschungsprojekte sind zur Zeit nicht in Bearbeitung"                                   
    #>  [8] "Hierzu kann ich keine Angaben machen. Ich suche/erforsche Daten, trage unsere eigenen Daten in der Datenbank ein, erstelle Dokumente."    
    #>  [9] "R, Excel, ADP (www.rgzm.de/adp), AMT (www.academic-meta-tool.xyz), SamianResearch (www.rgzm.de/samian), QGIS, ArcGIS, eigene Analysetools"
    #> [10] "Kein externer Dienst, nur dienststellen interne Datenbanken"                                                                              
    #> [11] "interne Fundstellendatenbank, QGIS, MS Excel"

<table>
<thead>
<tr>
<th style="text-align:left;">
Var1
</th>
<th style="text-align:right;">
Freq
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Außeruniversitäre Forschungseinrichtung
</td>
<td style="text-align:right;">
4
</td>
</tr>
<tr>
<td style="text-align:left;">
Denkmalbehörde
</td>
<td style="text-align:right;">
3
</td>
</tr>
<tr>
<td style="text-align:left;">
Sonstiges
</td>
<td style="text-align:right;">
2
</td>
</tr>
<tr>
<td style="text-align:left;">
Universität/Hochschule
</td>
<td style="text-align:right;">
1
</td>
</tr>
</tbody>
</table>

V.a. in außeruniversitären Forschungseinrichtungen (4x genannt) und
Denkmalbehörden (4x – einmal in sonstiges) wird selbständig Software
entwickelt.

### keine Angaben zu benutzer Software

Insgesamt sind sehr häufig keine Angaben gemacht worden. Im Nachhinein
herauszufiltern, warum dies geschah, ist kaum möglich.

19 x findet sich der Begriff “keine” o.ä. und 304 ist diese Frage nicht
beantwortet worden, also ca. die Hälfte der Antwortenden hat keine
Informationen dazu geben können / wollen.

*“Mit keinen so richtig. Weiterbildung wäre gut”* ist ein Hinweis einer
30-39jährigen Person. Zudem gab es 4x den Hinweis, dass die Analyse von
FD nicht zu den Aufgaben gehört.

Der Chi-Quadrat-Test zeigt, dass es keine Zusammenhänge zwischen Alter /
Einrichtung oder Gruppenzugehörigkeit und ob eine Angabe gemacht wurde
oder nicht, gibt.

genutzte Datenformate
---------------------

![](../figures/häufigkeiten_datenformate-1.png) Insgesamt 67
unterschiedliche Datenformate, darunter sehr spezialisierte
Ausgabeformate von bestimmten Geräten (z.B. Laserscannern). Dargestellt
sind hier diejenigen die häufiger als 2x genannt wurden.

Acknowledgements
================

<!-- The following line inserts a page break  -->
References
==========

<!-- The following line ensures the references appear here for the MS Word or HTML output files, rather than right at the end of the document (this will not work for PDF files):  -->

### Colophon

This report was generated on 2020-08-06 15:40:24 using the following
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
    #>  date     2020-08-06                  
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
    #>  gtable        0.3.0   2019-03-25 [1] CRAN (R 4.0.0)
    #>  highr         0.8     2019-03-20 [1] CRAN (R 4.0.0)
    #>  hms           0.5.3   2020-01-08 [1] CRAN (R 4.0.0)
    #>  htmltools     0.4.0   2019-10-04 [1] CRAN (R 4.0.0)
    #>  httr          1.4.2   2020-07-20 [1] CRAN (R 4.0.2)
    #>  kableExtra  * 1.1.0   2019-03-16 [1] CRAN (R 4.0.2)
    #>  knitr         1.28    2020-02-06 [1] CRAN (R 4.0.0)
    #>  labeling      0.3     2014-08-23 [1] CRAN (R 4.0.0)
    #>  lifecycle     0.2.0   2020-03-06 [1] CRAN (R 4.0.0)
    #>  magrittr    * 1.5     2014-11-22 [1] CRAN (R 4.0.0)
    #>  memoise       1.1.0   2017-04-21 [1] CRAN (R 4.0.0)
    #>  munsell       0.5.0   2018-06-12 [1] CRAN (R 4.0.0)
    #>  NLP         * 0.2-0   2018-10-18 [1] CRAN (R 4.0.0)
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
    #>  slam          0.1-47  2019-12-21 [1] CRAN (R 4.0.0)
    #>  SnowballC   * 0.7.0   2020-04-01 [1] CRAN (R 4.0.0)
    #>  stringi       1.4.6   2020-02-17 [1] CRAN (R 4.0.0)
    #>  stringr       1.4.0   2019-02-10 [1] CRAN (R 4.0.0)
    #>  testthat      2.3.2   2020-03-02 [1] CRAN (R 4.0.0)
    #>  tibble        3.0.0   2020-03-30 [1] CRAN (R 4.0.0)
    #>  tidyr       * 1.0.3   2020-05-07 [1] CRAN (R 4.0.0)
    #>  tidyselect    1.1.0   2020-05-11 [1] CRAN (R 4.0.0)
    #>  tm          * 0.7-7   2019-12-12 [1] CRAN (R 4.0.2)
    #>  usethis       1.6.1   2020-04-29 [1] CRAN (R 4.0.0)
    #>  vctrs         0.3.1   2020-06-05 [1] CRAN (R 4.0.2)
    #>  viridisLite   0.3.0   2018-02-01 [1] CRAN (R 4.0.0)
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
    #> Head:     [f61ad09] 2020-08-04: ups, verderhung ausgemerzt
