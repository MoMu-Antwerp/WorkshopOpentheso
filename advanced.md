# Thesaurus aanbieden voor (her)gebruik

## gebruik van PIDs

### Archival Resource Keys (ark)

Archival Resource Key (ARK) identifiers are URLs that support long-term access to information. Learn below what you need to know about ARKs, whether you’re planning how your system or collection will use them, or you’re a developer building ARK tools. https://arks.org/about/

![](assets/2022-10-20-00-06-22.png)

Voor het configureren van Arks zijn er verschillende opties:

![](assets/2022-10-20-00-10-10.png)

De Server opties zijn vooral gericht op naar het (Franse) consortium dat achter Opentheso zit en vereisen een login bij een externe dienst die voor het resolven/activeren zorgt.

De onderste optie helpt je al wel om 'ark-achtige' identifiers aan te maken die eventueel later kunnen geactiveerd worden.

## koha koppeling

## omeka-s koppeling

Omeka-s is een open source content management systeem dat vooral bedoeld is voor het publiceren van erfgoedcollecties. https://omeka.org/s/

Binnen omeka-s kan je 'Resource templates' bouwen met verschillende metadatavelden. Mits enige configuratie (https://opentheso.hypotheses.org/3231) kan je voor een veld instellen dat er gebruik moet gemaakt worden van een thesaurus uit opentheso (ook andere thesauri zoals aat zijn beschikbaar).
https://github.com/omeka-s-modules/ValueSuggest

In dit demo voorbeeld is het veld Subject gelinkt aan de Pactols onderwerpen thesaurus:

![](assets/2022-10-19-23-14-34.png)

Bij het invullen van het metadataveld krijg je dan een autocomplete functie te zien:

![](assets/opentheso_omeka-s_2022-10-19.gif)

# playtime

Exporteer je thesaurus door in de Toolbox op Exporter te klikken, kies Skos als formaat

![](assets/advanced-dba7bf7b.png)

## skosplay

https://skos-play.sparna.fr/play/



## virtuoso

via dockerfile
https://hub.docker.com/r/openlink/virtuoso-opensource-7
daarna deze walktrough om skosfile te importern in quadstore: https://www.youtube.com/watch?v=A8gVp1Wjmso

Open Sparql endpoint

```
SELECT * WHERE {
?s ?p ?o
}
LIMIT 10
```


```
PREFIX skos: <http://www.w3.org/2004/02/skos/core#>
SELECT * WHERE
{
  $concept skos:prefLabel $prefLabel .
  FILTER (str($prefLabel) = "binding")
  FILTER ( lang(?narrowerLabel) = "en" )
  OPTIONAL { $concept skos:altLabel $altLabel . }
  OPTIONAL { $concept skos:hiddenLabel $hiddenLabel . }
  OPTIONAL { $concept skos:definition $definition . }
  OPTIONAL { $concept skos:broader $broader . $broader skos:prefLabel $broaderLabel . }
  OPTIONAL { $concept skos:narrower $narrower . $narrower skos:prefLabel $narrowerLabel . }
  OPTIONAL { $concept skos:related $related . $related skos:prefLabel $relatedLabel . }
}
LIMIT 10
```



## openrefine(?)

...
