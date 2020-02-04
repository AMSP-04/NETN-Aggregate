# NETN-Aggregate

The NATO Education and Training Network (NETN) Aggregate FOM Module.

Copyright (C) 2019 NATO/OTAN.
This work is licensed under a [Creative Commons Attribution-NoDerivatives 4.0 International License](LICENCE.md).

## Introduction

The NETN FAFD representation of aggregate entities such as military units is based on the [SISO-STD-001-2015 standard RPR-FOM v2.0](https://www.sisostds.org/). The NETN FOM Module extends the RPR-FOM with a NETN_Aggregate object class which include additional attributes for unique identification of simulated entities.

It is recommended that NETN federates support the NETN extension for Aggregate Entities. For compatibility reasons, NETN federates, that implement NETN extensions of Aggregate Entities, are also required to support RPR-FOM v2.0.

### Purpose

The NETN-Aggregate FOM Module provides a common standard interface for the representation of Units in a federated distributed simulation. The module extends the existing RPR-FOM v2.0 standard with subclasses classes and additional attributes to allow additional information to be associated with simulated aggregate entities.

A unique identification attribute has been included to provide better support for initialization, NETN-TMR and other advanced design patterns requiring unique pre-defined identifiers for simulated entities. NETN federations still allow pure RPR-FOM based federates in the federation but with limited ability to interoperate in some NETN design aspects. 

### Scope

The `NETN_Aggregate` object class is a specialization/subclass of the RPR-FOM object class `BaseEntity.AggregateEntity` and defines additional attributes.

<img src="./images/NETN-Aggregate Object Class Tree.png" />





<img src="./images/NETN-Aggregate.png" width="75%"/>

The relation to NETN-ORG is normally not a one-to-one mapping, excepted for some cases. 

|Attribute|Description|NETN-ORG Relations|
|---|---|---|
|UnitPersonnel|This summarizes the health status of personnel comprising the aggregate.|Unit.Holdings|
|Callsign|The name of the object.|Unit.Name|
|VisualSignature|Describes the unit's susceptibility to electro-optical detection.|-|
|SourceUnit|Aggregate from which this aggregate was spawned.|Unit.SuperiorUnit|
|Mission|The operational task the aggregate has been ordered to perform.|-|
|Mounted|The percentage of aggregate personnel travelling on or in their organic transport.|-|
|UnitSupplies|The type and quantities of supplies available (on hand) to the unit.|Unit.Holdings|
|HigherHeadquarters|A pointer to the aggregate's superior unit or headquarters. The highest level unit or headquarters on each side will publish its own UniqueID as its HigherHeadquarters value.|Unit.SuperiorUnit|
|CombatValue|A summary value (in percent) of unit effectiveness based on level of training, leadership, moral, personnel and equipment operational status, etc.|Unit.CombatEffectiveness|
|WeaponsControlOrder|Describes current Weapon Control Order Free, Tight, or Hold.|-|
|SupportUnit|Identifies unit(s) which support the aggregate logistically, or with a specified combat or combat support relationship, e.g. a Direct Support or General Support Artillery unit.|-|
|Activity|The current activity of the aggregate. This may differ from the mission due to casualties, readiness, etc.|
|Symbol|The APP6A/MILSTD 2525B/MILSTD 2525C code for the aggregate.|Unit.SymbolIdentifier|
|CaptureStatus|The status of an aggregate with respect to its control or influence over its own activities.|-|
|UnitEquipment|This summarizes the health status of the equipment comprising the aggregate.|-|
|Echelon|The level of command of the aggregate.|Unit.Echelon|
|HUMINTSignature|Describes the unit's susceptibility to human intelligence (HUMINT), i.e. information collected and provided by human sources.|-|
|ElectronicSignature|Describes the aggregate's susceptibility to electronic detection both as a summary value and by identifying aggregate sensors together with their operational status.|-|
|Footprint|The region occupied by the aggregate. the region is defined as that bounded by line segments connecting the listed world locations.|-|
|CoverStatus|Describes the unit's protection from the effects of weapons fire.|-|
|EntityList|Provides data on entities comprising the aggregate.|Unit.Holdings|
|Status|If an instance shall be taken into account by federates.|-|
|UniqueID|The unique identifier of the object.|Unit.UUID|
|EmbeddedUnitList|The list of objects carried by this aggregate.|Unit.EmbarkedIn (indirect)|
|AggregateMarking|RPR_v2 attribute|Unit.Name|
|EntityType|RPR_v2 attribute|Unit.EntityType| 
|Spatial|RPR_v2 attribute|Unit.Location| 
|Spatial|RPR_v2 attribute|Unit.Direction| 
|Spatial|RPR_v2 attribute|Unit.Speed| 
|IsPartOf|RPR_v2 attribute|Unit.SuperiorUnit|
|Formation|RPR_v2 attribute|Unit.FormationPosition|
|SubAggregatesIdentifiers|RPR_v2 attribute|Unit.SuperiorUnit (indirect)|
|EntityIdentifiers|RPR_v2 attribute|Unit.EmbarkedIn (indirect)|
|SilentAggregates|RPR_v2 attribute|Unit.Holdings (deaggregated)|
|SilentEntities|RPR_v2 attribute|Unit.Holdings (deaggregated)|

