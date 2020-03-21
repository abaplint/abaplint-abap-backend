# abaplint abap backend

## Purpose

This is a toolset to run abaplint checks within an SCI run.

![sci](docs/img/sci-sample.png)

It consist of 2 parts: (1) the abap backend (this repo), which integrates with SCI and posts the code to the server part (2) which runs the abaplint (with nodejs).

![landscape](docs/img/landscape.png)

**Important:** the code under test leaves your abap instance! Be sure to use secure and controllable abaplint server. For a test you might use common one: [http://sci.abaplint.org/](http://sci.abaplint.org/) (but please don't post any proprietary code).

## Installation

* Prerequisites: 
    * abapGit dev version must be installed (with all the separate classes, not a simple file version)
    * ABAP731 required, potentially works with 702. Though downported json xml parser should be availble.
* Install on ABAP backend (this repo) using abapGit
* Activate check in SCI -> Management of -> Tests
* Adjust check variants, maintain connection to [abaplint-cloud-foundry](https://github.com/abaplint/abaplint-cloud-foundry)
* abaplint settings are defined per target package

![setup1](docs/img/setup1.png)
![setup2](docs/img/setup2.png)

## Posts

- https://blogs.sap.com/2020/02/01/running-abaplint-from-sci-atc-adt/
