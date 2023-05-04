# LLM-filtered news pipeline

## Motivation
It is difficult to acquire an effective summary of daily current events, even from aggregation platforms (twitter, reddit). I want multiple sources presented in an unbiased way, and I want to be able to filter for events that are likely to be high impact.

## Killer Feature
The pipeline needs to try and forecast the amount of impact it will have on my life. I also want to know why the service is scoring news the way that it does: it needs to know about who I am, and what the event is to come up with a relevancy score breakdown.

## Data Pipeline overview
1. Fetch batch of 1,000 headlines from the list of global sources
2. add new batch to data lake
3. determine if there are globally relevant moments in todays batch
4. fetch local sources for the user
5. determine if any of the local news is actually important
6. compose the news page for the user
