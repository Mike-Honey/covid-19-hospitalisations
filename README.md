# covid-19-hospitalisations
Projects on the topic of COVID-19 hospitalisations - mostly DataViz

The idea being explored is that cases can predict future hospitalisations. Parameters are used for:
- the % of cases predicted to result in hospitalisation
- the number of days to shift/delay between case reporting and hospitalisation

Once parameters are found that get a close fit between the lines, then any divergence might indicate something has changed in the situation, e.g.
- new variant causing more/less severe illness
- new variant causing faster/slower onset of severe illness
- health system under pressure
- more/less vulnerable population becoming infected

## New South Wales - June 2021

Adjust the parameters to suit, default is now 18% after 6 days.

[Link to interactive DataViz](https://app.powerbi.com/view?r=eyJrIjoiY2QzODIzZmYtMGFjOS00ZGEzLWFhZTktYWU0YzhkN2JhOGViIiwidCI6ImRjMWYwNGY1LWMxZTUtNDQyOS1hODEyLTU3OTNiZTQ1YmY5ZCIsImMiOjEwfQ%3D%3D)

[![Click to view and interact with the report](https://github.com/Mike-Honey/covid-19-hospitalisations/raw/main/covid-19-hospitalisations%20NSW%202021-06.png)](https://app.powerbi.com/view?r=eyJrIjoiY2QzODIzZmYtMGFjOS00ZGEzLWFhZTktYWU0YzhkN2JhOGViIiwidCI6ImRjMWYwNGY1LWMxZTUtNDQyOS1hODEyLTU3OTNiZTQ1YmY5ZCIsImMiOjEwfQ%3D%3D)

## Australia - explore

Choose any state/territory, date range etc. Adjust the parameters to suit, default is 18% after 6 days.

[Link to interactive DataViz](https://app.powerbi.com/view?r=eyJrIjoiY2QzODIzZmYtMGFjOS00ZGEzLWFhZTktYWU0YzhkN2JhOGViIiwidCI6ImRjMWYwNGY1LWMxZTUtNDQyOS1hODEyLTU3OTNiZTQ1YmY5ZCIsImMiOjEwfQ%3D%3D&pageName=ReportSection32e05b49cb88a98d511b)

[![Click to view and interact with the report](https://github.com/Mike-Honey/covid-19-hospitalisations/raw/main/covid-19-hospitalisations%20Australia.png)](https://app.powerbi.com/view?r=eyJrIjoiY2QzODIzZmYtMGFjOS00ZGEzLWFhZTktYWU0YzhkN2JhOGViIiwidCI6ImRjMWYwNGY1LWMxZTUtNDQyOS1hODEyLTU3OTNiZTQ1YmY5ZCIsImMiOjEwfQ%3D%3D&pageName=ReportSection32e05b49cb88a98d511b)

**Reference:**

I noticed a few international analyses using a similar method - comparing: 
- "expected hospitalisations" - % X of new cases (typically 2% to 10%), vs
- hospitalisations, shifted back N days (typically 2 to 10 days)

The expectation is that the lines track each other, confirming the hypothesis that % X of cases result in hospitalisation after N days. 

Needing to using different % X and N days values might reflect changes in vaccination rates, or the characteristics of variants.

Here's one by [Oliver Johnson](https://twitter.com/BristOliver) for the UK, using 5% and 10 days:
[![Click to view the tweet](https://github.com/Mike-Honey/covid-19-hospitalisations/raw/main/covid-19-hospitalisations%20bristoliver.png)](https://twitter.com/BristOliver/status/1404857813248118784)

Another by [Andrew Steele](https://twitter.com/statto) for the UK, using 8% and 10 days:

The lines tracked quite tightly until vaccination rates increased, then hospitalisations started to drop away.

[![Click to view the tweet](https://github.com/Mike-Honey/covid-19-hospitalisations/raw/main/covid-19-hospitalisations%20statto.png)](https://twitter.com/statto/status/1409590572583555081)

And another by [Eran Segal](https://twitter.com/segal_eran) for Israel, using 2.2% and 4 days: 

The lines tracked quite tightly for their first and second waves (top chart), but the bottom chart shows an even stronger effect of vaccinations.

[![Click to view the tweet](https://github.com/Mike-Honey/covid-19-hospitalisations/raw/main/covid-19-hospitalisations%20segal_eran.png)](https://twitter.com/segal_eran/status/1410661825197363201)

**Summary**

I present my version for the available Australian data, from covidlive.com.au. Australian data is sparse and spiky so I smoothed using 7-day rolling averages. 

I found the closest fit for the line now seems to be for 18% (cases expected to result in hospitalisation) and 6 days (delay from case reporting to hospitalisation). Using the interactive dataviz you can adjust those to suit your understanding.

A page is presented set for the current New South Wales outbreak, with an indicator of the date that outbreak started.

An "explorer" page is also presented where you can choose to focus on a state of interest or alter the date range. 

Note the hospitalisation figures used internationally are understood to be the number of people admitted to hospital each day. That figure is publicly available in some countries, but not for Australia (AFAIK - please contact me if you are aware of a source dataset). 

Instead in Australia we can get the number of people currently in hospital for COVID-19 each day. So for a fairly close approximation of hospital admissions, I am using the daily increase in hospitalisations. This will be slightly understated at the tail end of each outbreak, when more people are leaving hospital than entering.

Note Queensland current policy is to admit all COVID-19 cases to hospital, so their figures dont make sense for this analysis.


THIS REPORT IS NOT HEALTH ADVICE - REFER TO YOUR LOCAL HEALTH AUTHORITY.
