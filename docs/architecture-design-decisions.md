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
| Beer drinkers | handle thousands of user (1000 new user every week) | Beer drinkers are thirsty for information about beers and which pub/bar sells them. They're joining the app to find it and rank it. |

## Architectural Significant Requirements

### Requirements

| Constrains | Origin | Type | Context |
| ---------- | ------ | ---- | ------- |
| Use Clojure for backend | Develop team | Technical | We want to learn functional program and apply it for a real project. |
| Limit budget | Develop team | Business | We have a really tiny budget to spend in the project. |

### Quality Attributes

| Quality attribute | Scenario | Priority |
| ----------------- | -------- | -------- |
| Performance | When the drinker look for a type of beer, it needs to return the list of the beer of this type in 2 seconds. We expect that there will be hundreds of beers. | High |
| Performance | When the drinker look for beers around him, it needs to return the list of pubs/bar close to the drinker that has this beer in 10 seconds. We expect that there will be thousands of pubs/bar. | High |
| Scalability | The number of pubs/bars will increase in a rate of 5% per month | Medium |
| Availability | When the drinker is looking for something and the services are under pressure, it has to timeout quickly, 20% more time than establish for normal load. | Medium |

### Functional Requirements

- The user should be able to recovery all data, if log in with his/her account in a different phone;
- The pubs/bars need to be geographically located;
- Search for pubs/bars will be limited by a range chosen by drinker (max.: 10km);
