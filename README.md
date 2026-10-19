# Telecom Customer Churn Analysis – Power BI

## Om prosjektet

Dette prosjektet er utviklet for å utforske kundeatferd og kundefrafall (*customer churn*) i telekommunikasjonsbransjen ved hjelp av Microsoft Power BI.

Formålet er å undersøke hvilke kundegrupper som har høyest kundefrafall, hvordan kontraktstyper og tjenester henger sammen med kundefrafall, og hvordan data kan brukes til å gi bedre beslutningsgrunnlag.

Prosjektet er et selvstendig porteføljeprosjekt hvor jeg har jobbet med datarensing, dataanalyse, DAX og utvikling av et interaktivt dashboard.

## Teknologier og verktøy

- **Power BI Desktop:** Utvikling av interaktive dashboards og datavisualiseringer.
- **Power Query:** Datarensing, transformasjon og kontroll av datakvalitet.
- **DAX (Data Analysis Expressions):** Beregning av nøkkeltall og egendefinerte mål.
- **CSV:** Import og behandling av kundedata.

## Datasett

Datasettet er hentet fra [Telco Customer Churn på Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) og er basert på IBM-eksempeldata.

Det inneholder informasjon om 7 043 fiktive telekomkunder, blant annet:

- Kontraktstype og abonnement
- Månedlige kostnader
- Betalingsmetode
- Internettjenester
- Kundeforholdets varighet (*tenure*)
- Kundefrafall (*churn*)

## Databehandling og datarensing

Før analysen ble datasettet importert til Power BI og behandlet i Power Query.

Arbeidet omfattet:

1. Kontroll av datakvalitet, kolonnefordelinger og datatyper.
2. Kontroll av unike kunde-ID-er.
3. Konvertering av `MonthlyCharges` og `TotalCharges` fra tekst til desimaltall.
4. Bruk av engelske regionale innstillinger for riktig håndtering av desimalskilletegn.
5. Identifisering av 11 manglende verdier i `TotalCharges`. Disse ble beholdt som manglende verdier for å unngå å introdusere kunstige betalingsbeløp.
6. Gruppering av kundetid i intervaller på 12 måneder.

## Dashboard og visualiseringer

Dashboardet gir en interaktiv oversikt over kundebasen og kundefrafallet.

### Nøkkeltall (KPI-er)

| KPI | Resultat |
|---|---|
| Total Customers | 7 043 |
| Churn Rate | 26,54 % |
| Churned Customers | 1 869 |
| Average Monthly Charges | 64,76 |

### Visualiseringer

Dashboardet inneholder fire analyser:

- **Churn Rate by Contract Type:** Sammenligning av kundefrafall mellom kontraktstyper.
- **Churn Rate by Internet Service:** Analyse av kundefrafall fordelt på internettjenester.
- **Churn Rate by Payment Method:** Sammenligning av kundefrafall mellom betalingsmetoder.
- **Churn Rate by Customer Tenure (Months):** Analyse av sammenhengen mellom kundetid og kundefrafall.

Det er også implementert et interaktivt kontraktfilter som gjør det mulig å undersøke ulike kundegrupper og se hvordan nøkkeltallene endrer seg.

## Viktigste funn

Analysen viser flere interessante mønstre i datasettet:

**1. Kontraktstype og kundefrafall**

Kunder med månedlige kontrakter har vesentlig høyere kundefrafall enn kunder med ett- eller toårskontrakter.

**2. Internettjenester**

Kunder med fiberoptisk internett har høyere kundefrafall enn kunder med DSL eller uten internettjeneste.

**3. Betalingsmetode**

Kunder som bruker betalingsmetoden Electronic check, har høyest kundefrafall blant betalingsmetodene i datasettet.

**4. Kundetid**

Kunder med kortere kundeforhold har generelt høyere kundefrafall enn kunder som har vært hos selskapet over lengre tid.

Disse funnene viser sammenhenger i datasettet, men dokumenterer ikke nødvendigvis årsakssammenhenger.

## Hvordan åpne prosjektet

1. Installer Microsoft Power BI Desktop.
2. Last ned filen `Telecom_Customer_Churn_Analysis.pbix`.
3. Åpne filen i Power BI Desktop.
4. Utforsk nøkkeltallene, grafene og det interaktive kontraktfilteret.

Ved oppdatering av datakilden kan det være nødvendig å endre filbanen til den opprinnelige CSV-filen.

## Hva jeg har lært

Gjennom dette prosjektet har jeg fått praktisk erfaring med å importere og rense data, kontrollere datakvalitet, opprette beregninger med DAX og utvikle interaktive visualiseringer i Power BI.

Prosjektet har også gitt meg bedre forståelse for hvordan dataanalyse kan brukes til å identifisere mønstre i kundeatferd og presentere innsikt på en oversiktlig måte.

Målet har vært å utvikle grunnleggende kompetanse innen Business Intelligence og datadrevet analyse gjennom praktisk prosjektarbeid.
