# Event Schemas Based on FrameNet

This repository contains event schema resources derived from FrameNet-style frame definitions. It provides event types, event scenarios, semantic roles, hierarchy views, and relation mappings between events.

The resource is useful for work on event extraction, schema induction, event argument modeling, ontology construction, semantic role analysis, and FrameNet-based event representation.

## Contents

| Path | Description |
| --- | --- |
| `eventSchemas/` | XML definitions for individual event schemas. |
| `event_schema_list.txt` | Flat list of event schemas and their argument roles. |
| `event_scenario_list.txt` | Flat list of higher-level event scenarios and their argument roles. |
| `eventRelations.xml` | XML file describing relations between event schemas, including role mappings. |
| `EventFrameHierachy.html` | Static HTML view of the event frame hierarchy. |
| `EventScenarioHierarchical.html` | Static HTML view of the event scenario hierarchy. |


## Resource Summary

- 655 event schema XML files in `eventSchemas/`
- 50 event scenario entries in `event_scenario_list.txt`
- 10 event relation types in `eventRelations.xml`
- 2,070 event-to-event relations
- 12,393 role mappings between related events

## Event Schema Format

Each file in `eventSchemas/` defines one event schema. For example:

```text
eventSchemas/Attack.xml
eventSchemas/Commerce_buy.xml
eventSchemas/Death.xml
eventSchemas/Employment_start.xml
```

The XML files contain:

- the event/frame name and ID
- a textual definition
- argument roles
- role definitions
- role core type, such as `Core`, `Peripheral`, or `Extra-Thematic`
- semantic type information when available
- lexical units and annotations when available

For example, the `Attack` schema includes roles such as:

- `Assailant`
- `Victim`
- `Weapon`
- `Place`
- `Time`
- `Purpose`
- `Result`




## Lists

`event_schema_list.txt` provides a compact tabular view:

```text
Event Type          Event Argument Roles
Attack              (Assailant, Victim, Weapon, Place, Time, ...)
Commerce_buy        (Buyer, Seller, Goods, Money, ...)
Death               (Protagonist, Cause, Time, Place, ...)
```

`event_scenario_list.txt` contains higher-level event scenarios, for example:

```text
Commerce_scenario
Crime_scenario
Employment_scenario
Medical_interaction_scenario
Motion_scenario
Transfer_scenario
```

These files are convenient starting points when browsing the resource or selecting event types for downstream tasks.

## Event Relations

`eventRelations.xml` defines structured relations between events. The relation types include:

- `Causative_of`
- `Inchoative_of`
- `Inheritance`
- `Metaphor`
- `Perspective_on`
- `Precedes`
- `ReFraming_Mapping`
- `See_also`
- `SubEvent`
- `Using`

Each relation can include mappings between argument roles in the related events. For example, a relation may connect a child event to a parent event and specify how the child event's roles correspond to the parent event's roles.


