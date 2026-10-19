# Voorbeeld: van wetenschappelijk artikel naar LinkedIn-post

*Example of a full input and output (Dutch). The skill works the same way in English and French.*

## Input

> Maak een prompt om van een wetenschappelijk artikel een LinkedIn-post te maken.

## Output (ingekort)

### De prompt

```
Ik deel regelmatig onderzoek over AI in het onderwijs op LinkedIn, voor een publiek van leerkrachten, docenten en beleidsmakers. Zij hebben weinig tijd en geen toegang tot betalende tijdschriften, dus mijn posts moeten de kern van een studie helder en eerlijk overbrengen.

<artikel>
{{ARTIKEL}}
</artikel>

Schrijf op basis van het artikel hierboven een LinkedIn-post in het {{TAAL}}.

Wat de post moet doen:
- Openen met één zin die de belangrijkste bevinding of een verrassend inzicht naar voren brengt, want de eerste twee regels bepalen of mensen verder lezen.
- In gewone taal uitleggen wat onderzocht werd, bij wie, en wat er gevonden werd.
- Eerlijk zijn over de beperkingen (bv. kleine steekproef, één land), zodat de post niet meer belooft dan het onderzoek toont.
- Afsluiten met wat dit betekent voor de praktijk in de klas, en een vraag aan de lezer.

Vorm:
- Maximaal 200 woorden, want langere posts worden op LinkedIn ingekort.
- Korte alinea's, geen opsommingstekens met emoji's.
- Vermeld de bron (auteurs, jaar, tijdschrift) onderaan.

Controleer voor je antwoordt: staat elk cijfer in de post ook in het artikel?
```

### Variabelen
- `{{ARTIKEL}}`: de volledige tekst of het abstract van het artikel
- `{{TAAL}}`: Nederlands, Frans of Engels

### Keuzes en aannames
- Het artikel staat bovenaan en de opdracht onderaan, omdat Claude dan beter met lange teksten omgaat.
- Elke beperking krijgt een reden ("want…"), zodat Claude de bedoeling begrijpt en die ook in randgevallen volgt.
- De zelfcontrole op cijfers voorkomt dat de post een getal verzint.
