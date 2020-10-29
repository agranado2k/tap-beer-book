# Architecture Design

## Stakeholders

- Beer drinkers (users);

- Pub/Bar owners;

- Brewers;

- Develop team.

## Business goals

| Stakeholder | Goal | Context |
| ----------- | ----- | ------ |
| Pub/Bar owners | 100 in the first quarter and 1000 beers | Pub/Bars want to attract beer drinkers to buy beers in their pubs/bars. So they will create their profiles and link the beers to it. |
| Brewers | 20 brewers in the first quarter and 100 beers | Brewers want to expose their beers and make it good ranked. So they will create the brewer and beers profiles. |
| Beer drinkers | handle thousands of user (1000 new user every week) | Beer drinkers are thirst for information about beers and which pub/bar sell its. They're joining the app to find it and rank its. |

## Architectural Significant Requirements

### Requirements

| Constrains | Origin | Type | Context |
| ---------- | ------ | ---- | ------- |
| Use Clojure for backend | Develop team | Technical | We want to learn functional program and apply it for a real project. |
| Limit budget | Develop team | Business | We have a really tiny budget to spend in the project. |

### Quality Attributes

#### Scenarios

- look for type of beer -> request sent -> system get beer of this type (the response should happen in less than 1 second): the database has hundreds of beers;

- look for a beer around -> request sent -> system get pubs closed the location that has that beer (the response should happen in less than 10 seconds): the database has thousands of pubs;
