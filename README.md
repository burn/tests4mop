<img src="https://img.shields.io/badge/tests-passing-green">   <img
src="https://img.shields.io/badge/purpose-se--ai-blueviolet"> <img
src="https://img.shields.io/badge/platform-osx,linux-pink">

<img align=right width=250
src="https://gist.githubusercontent.com/timm/a50169221e10702307f27cc2ead9cad9/raw/92ff182a04561cd5b0497bf6abbd9527ec3016f4/logo.png">


# Test data, Multi-objective Problems, SE


For those tired on DTLZ, fonseca, etc etc etc.

## Contents

| What | File|
|------|-----|
| [Misc](#Misc) |  healthCloseIsses12mths0011-easy.csv healthCloseIsses12mths0001-hard.csv auto93.csv |
| [UCI](#UCI) | Wine_quality.csv |
| [Process data](#process_data) | pom3a.csv pom3b.csv pom3c.csv pom3d.csv xomo_flight.csv xomo_ground.csv xomo_osp.csv xomo_osp2.csv coc1000.csv china.csv nasa93dem.csv |
| [Configuration](#configuration) | SS-A.csv SS-B.csv SS-C.csv SS-D.csv SS-E.csv SS-F.csv SS-G.csv SS-H.csv SS-I.csv SS-J.csv SS-K.csv SS-L.csv SS-M.csv SS-N.csv SS-O.csv |

## Misc

- auto93.csv :  designing a car
- healthCloseIsses12mths0011-easy.csv : predicting software project health indicators,  12 months into the future (easy example)
- healthCloseIsses12mths0001-hard.csv : predicting software project health indicators,  12 months into the future (hard example)

## UCI

Related to red and white vinho verde wine samples, from the north of Portugal. The goal is to model wine quality based on physicochemical tests (see [Cortez et al., 2009], http://www3.dsi.uminho.pt/pcortez/wine/).
For more info, please see: https://archive.ics.uci.edu/dataset/186/wine+quality

## Process data


These descriptions were taken from [8].

### XOMO

XOMO was introduced in [^me05] and is a general framework for Monte Carlo simulations that combine four COCOMO-like process models from Barry Boehm's group at USC. XOMO has four objectives:
- Reduce project risk
- Reduce development effort
- Reduce predicted defects
- Reduce total months of development

The variables used are described below, and takes values in the range  1..6.

| Variable  | Description   |
|-------------- | -------------- |
| prec    | Have we done this before?     |
| flex    | Development flexibility |
| resl    | Any risk resolution activities? |
| team    | Team cohesion |
| pmat    | Process maturity |
| acap    | Analyst capability |
| pcap    | Programmer capability |
| pcon    | Programmer continuity |
| aexp    | Analyst experience |
| pexp    | Programmer experience |
| ltex    | Language and tool experience |
| tool    | Tool use |
| site    | Multiple site development |
| sced    | Length of schedule |
| rely    | Required reliability |
| data    | Secondary memory requirements |
| cplx    | Program complexity |
| ruse    | Software reuse |
| docu    | Documentation requirements |
| time    | Runtime pressure |
| stor    | Main memory requirements |
| pvol    | Platform volatility |

This directory contains four scenarios taken from NASA's Jet Propulsion Lab [7]. Flight and ground are general descriptions of all flight and ground software, and OSP and OSP2 represent two versions of the Orbital Space Plane flight guidance system. In order of complexity: OSP = OSP2 < Ground < Flight.

### POM3

POM3 is a model of the management challenge specific to Agile development [^boehm03] [3-4]. In particular, it simulates Boehm & Turner's model of agile programming [5] where teams select tasks as they appear in the scrum backlog. The goals of POM3 are:
- Increase completion rates
- Reduce idle rates
- Reduce overall cost

The inputs to the model are below:

| Short name  | Decision   | Description   |
|-------------- | -------------- | -------------- |
| Cult    | Culture     | Percent of requirements that change     |
| Crit    | Criticality | Requirements cost effect for safety-critical systems |
| Crit.Mod | Criticality modifier | Percentage of teams affected by criticality |
| Init. Kn | Initial Known | Percentage of initially known requirements |
| Inter-D | Inter-dependency | Percentage of requirements that have inter-dependencies with other teams |
| Dyna    | Dynamism | Rate of how new requirements are made |
| Size    | Size    | Number of base requirements in the project |
| Plan    | Plan | Prioritization strategy, see below |
| T.Size  | Team size | Number of personnel in each team |

Where the prioritization strategy values are:
- 0: Cost ascending
- 1: Cost descending
- 2: Value ascending
- 3: Value descending
- 4: Cost/Value ascending
- 5: Cost/Value descending

There are three sets of POM models: POM3a covers a wide range of projects; POM3b represents small and highly critical projects; POM3c represents large and dynamic projects, where cost and value can be altered over a wide range. In order of complexity, POM3a < POM3b < POM3c [6].


[^me05]: Menzies, Tim, and Julian Richardson. "Xomo: Understanding development options for autonomy." COCOMO forum. Vol. 2005.

[^boehm03]: Boehm, Barry, and Richard Turner. "Using risk to balance agile and plan-driven methods." Computer 36.6 (2003): 57-66.

[3] Boehm, Barry W., and Richard Turner. Balancing agility and discipline: A guide for the perplexed. Addison-Wesley Professional, 2004.  
[4] Port, Dan, Alexy Olkov, and Tim Menzies. "Using simulation to investigate requirements prioritization strategies." 2008 23rd IEEE/ACM International Conference on Automated Software Engineering. IEEE, 2008.     
[5] Boehm, Barry W., et al. Software cost estimation with Cocomo II with Cdrom. Prentice Hall PTR, 2000.     
[6] Lekkalapudi, Naveen Kumar. Cross trees: Visualizing estimations using decision trees. West Virginia University, 2014.     
[7] Menzies, Tim, et al. "How to avoid drastic software process change (using stochastic stability)." 2009 IEEE 31st International Conference on Software Engineering. IEEE, 2009.    
[8] Chen, Jianfeng, et al. "“Sampling” as a baseline optimizer for search-based software engineering." IEEE Transactions on Software Engineering 45.6 (2018): 597-614.

## Configuration

For more details and data description, please see Table 1 and Table 2 from this paper: https://arxiv.org/pdf/1801.02175.pdf.

<img src="/img/ss.png">

