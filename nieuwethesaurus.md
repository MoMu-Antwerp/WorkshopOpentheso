# Creëer een Thesaurus

## Als eerste oefening creëren we een thesaurus 'from scratch':


 - Klik op Toolbox:
 ![](assets/nieuwethesaurus-0e73d9ab.png)
 - Daarna op Nouveau: ![Nouveau](assets/nieuwethesaurus-1bfb8b9c.png)
 - Geef een naam, selecteer een taal en druk vervolgens op "Créer": ![](assets/nieuwethesaurus-9ecb1cbe.png)
 - De thesaurus verschijnt nu in de lijst:

![](assets/nieuwethesaurus-e6c5df94.png)
> <b>Note</b>: Standaard staat een nieuwe thesaurus op publiek beschikbaar

- Je thesaurus is nog niet meteen beschikbaar in het 'thesaurus-selectie-veld'. Klik op de refresh-knop ernaast om hem beschikbaar te maken: ![](assets/nieuwethesaurus-ac900159.png)

## Eerste concept

- Selecteer de nieuwe thesaurus in het selectieveld:

> Deze is nog volledig leeg

![](assets/nieuwethesaurus-2a51cce9.png)
 - Klik op het plusteken in het overzichtvenster om een eerste, 'top concept' aan te maken: ![](assets/nieuwethesaurus-99270b17.png)

 - Vul de naam en eventueel de beschrijving (Notation) in en klik op <b>Validate</b>:

 ![](assets/nieuwethesaurus-ca6016a0.png)
 > <i>Voor deze oefening is enkel de <b>naam</b> van het top concept belangrijk. De andere functies komen later aan bod.</i>

![](assets/nieuwethesaurus-9ee843cc.png)

## Meer Concepten
- voeg een 10-tal Narrower terms toe door op het plusteken naast je top concept te klikken en 'Concept' te kiezen: ![](assets/nieuwethesaurus-78fde3cc.png)
    ![](assets/nieuwethesaurus-65b0ef4a.png)
    - je kan meerdere concepten na elkaar invoeren:
      - voeg minstens twee verschillende pasta soorten en kauwgom toe. Deze gaan we nodig hebben in een volgende stap.

    ![](assets/nieuwethesaurus-7ebfe824.png)


## Hiërarchie aanbrengen

- breng nieuwe structuur aan (door bijvoorbeeld een nieuw concept 'pasta' aan te maken.
- klik en sleep de pastasoorten naar 'pasta'

![](assets/2022-10-18_10-46_pasta.gif)
- breng nog wat verder hiërarchie aan door verschillende tussenniveaus aan te brengen (vb 'voedsel' ; 'drank' ; 'conserven' ; ...)

![](assets/nieuwethesaurus-4c8fcbfb.png)

- maak een vertaling voor een Concept
- aligneer een concept met wikidata



![](assets/nieuwethesaurus-5799b2df.png)

- maak een tweede top concept 'To do lijst'

## Facetten

Het is mogelijk om in plaats van een concept aan te maken, te kiezen voor 'new Facet'.
Je mag er gerust mee experimenteren maar hier hebben we zelf in onze usecases nog geen gebruik van gemaakt.
Wanneer je een Facet aanmaakt, krijgt het in de skos export het volgende label:

``` xml
    <!-- http://purl.org/iso25964/skos-thes#ThesaurusArray -->

    <owl:Class rdf:about="http://purl.org/iso25964/skos-thes#ThesaurusArray">
        <rdfs:subClassOf rdf:resource="http://www.w3.org/2004/02/skos/core#Collection"/>
        <dcterms:modified rdf:datatype="http://www.w3.org/2001/XMLSchema#date">2013-12-09</dcterms:modified>
        <rdfs:isDefinedBy rdf:resource="http://purl.org/iso25964/skos-thes"/>
        <rdfs:label xml:lang="en">Thesaurus Array</rdfs:label>
        <vs:term_status rdf:datatype="http://www.w3.org/2001/XMLSchema#string">released</vs:term_status>
        <skos:definition xml:lang="en">Definition: ISO ThesaurusArray
An array is a group of sibling concepts

Instances of ThesaurusArray can be mapped to instances of skos:OrderedCollection (a subclass of skos:Collection) if and only if the array needs to be an ordered array (in the ISO-25964 model the value of its Boolean attribute "ordered" is true).
It is advised to use the skos:inScheme (http://www.w3.org/2004/02/skos/core#inScheme) property on such a skos:Collection to relate it to its Thesaurus (see ISO 25964: isPartOf).

Concepts in a thesaurus array are sibling concepts in the thesaurus.

If present, the node label of a thesaurus array is mapped to rdfs:label or xl:prefLabel.
Optional node label attributes typically are mapped to dc: (or dct:) properties:
- dct:created
- dct:modified
These can be attached (if needed) to the xl:Label instance that is the value of xl:prefLabel.</skos:definition>
    </owl:Class>
```

## Collecties

Een andere manier om je concepten te structureren is aan de hand van 'Collecties'.

Voor deze workshop maken we collecties aan voor de winkels waar we de items uit onze shoppinglijst kunnen kunnen terugvinden.
Navigeer naar 'Collection' in het overzichtsvenster

![](assets/2022-10-19-20-42-29.png)

- klik op het plusteken en maak enkele 'collections' aan

![](assets/2022-10-19-20-44-13.png)

![](assets/2022-10-19-20-45-58.png)

- Om concepten toe te voegen aan een collectie, ga terug naar de Concept-tab en selecteer een concept.
![](assets/2022-10-19-20-47-41.png)
- Klik op het tandwieltje bij 'Collection' en kies of je het enkel het conept of het concept en onderliggende concepten (narrower terms) wil toevoegen aan een collectie.



> volgende: [thesaurus op basis van een excel-bestand](https://github.com/MoMu-Antwerp/WorkshopOpentheso/blob/main/import_csv.md)
