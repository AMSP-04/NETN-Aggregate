# NETN-Aggregate (DEPRECATED)

## Introduction

The NETN FAFD representation of aggregate entities such as military units and physical entities such as platforms is based on the [SISO-STD-001-2015 standard RPR-FOM v2.0](https://www.sisostds.org/). The NETN FOM Module extends the RPR-FOM with NETN-Aggregate and NETN-Physical object classes which include additional attributes for unique identification of simulated entities. The unique identification has been included to provide better support for initialization, NETN-TMR and other advanced design patterns requiring unique pre-defined identifiers for simulated entities. NETN federations still allow pure RPR-FOM based federates in the federation but with limited ability to interoperate in some NETN design aspects. 

It is recommended that NETN federates support NETN extensions of Aggregate and Physical Entities. For compatibility reasons NETN federates, that implement NETN extensions of Aggregate and/or Physical Entities, are also required to support RPR-FOM v2.0.

## License

Copyright (C) 2019 NATO/OTAN.
This work is licensed under a [Creative Commons Attribution-NoDerivatives 4.0 International License](LICENCE.md). 

The work includes the [NETN Aggregate FOM Module](NETN-Aggregate_v1.0.4.xml).

Above license gives you the right to use and redistribute the NETN FOM Module (XML file) in its entirety without modification. You are also allowed to develop your own new FOM Modules (in separate XML files and separate documentation) that build-on/extends the NETN module by reference and including neccessary scaffolding classes. You are NOT allowed to modify this FOM Module without prior permission by the NATO Modelling and Simulation Group. 

## Versions, updates and extentions

All updates and versioning of this work is coordinated by the NATO Modelleing and Simulation Coordination Office (MSCO), managed by the NATO Modelling and Simulation Group (NMSG) and performed as NATO Science and Technology Organization (STO) technical activities in support of the NMSG Modelling and Simulation Standards Subgroup (MS3).

Feedback on the use of this work, suggestions for improvements and identified issues are welcome and can be provided using GitGub issue tracking. To engage in the development and update of this FOM Module please contact your national NMSG representative.

Version numbering of this FOM Module and associated documentation is based on the following principles:

* New official version number is assigned and in effect only when new release is made in the Master branch.
* Updates in the Develop branch will not change version number.
* In the FOM Module useHistory information include only information on official releases.
* Update of the major version number is made if the change constitute a major restructuring, merging, addition or redefinition of semantics that breaks backward compatibility or cover entirely new concepts.
* Update of the minor version number is made if the change constitute a minor additions to existing concepts and editorial changes that do not break backward compatibility but may require updates of software to use new concepts.
* Patches are released to fix minor issues that do not break backward compatibility.

## Note
NETN-Aggregate is merged with NETN-MRM in NETN-FOM v3.0 and will not be released as a separate module.

|Version|Description|
|---|---|
|v1.0.4 | NETN Aggregate FOM Module included in NETN FOM v2.0 part of AMSP-04 Ed A|

## Documentation

[Full Documentation](https://nso.nato.int/nso/nsdd/APdetails.html?APNo=2268&LA=EN)
