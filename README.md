# salmon-habitat-monitoring
An edge habitat monitoring prototype for Taiwan’s endangered landlocked salmon, built with Nordic nRF54LM20 DK and Bluetooth LE.


### Edge AI for Monitoring Taiwan’s Endangered Salmon Habitat

Salmon Refuge Sentinel is a proposed low-power habitat monitoring system
for Taiwan’s endangered Formosan landlocked salmon
(*Oncorhynchus masou formosanus*).

The project will use the Nordic nRF54LM20 DK to collect environmental
measurements, identify unusual changes locally, and share information
through Bluetooth Low Energy.

## Project Status

Concept and prototype planning.

Hardware selection, firmware development, and experimental validation
are planned. No field deployment or conservation partnership is
currently claimed.

This project is being developed for the Sustain the System challenge.

## The Problem

Population surveys provide essential information about salmon abundance
and distribution. Environmental monitoring complements these surveys
by documenting conditions between field visits.

Floods, sediment transport, low flows, and changes in streamside shade
can affect habitat. Some changes may persist after water levels and
clarity appear to recover.

The project will investigate whether continuous local measurements can
help identify sites that need closer inspection.

## What I Will Build

The initial prototype will measure:

- Water temperature
- Water level
- Turbidity
- Battery condition
- Optional enclosure movement

The intended monitoring approach compares a candidate refuge with a
nearby main-channel location. Initial development will use one station
in a controlled water-test rig.

A second station or independent reference logger will be needed for
simultaneous field comparisons.

## How It Will Work

1. Sensors collect timestamped environmental measurements.
2. The nRF54LM20 DK checks readings and calculates time-window features.
3. Thresholds, trend analysis, and a compact Edge AI model are compared.
4. Measurements and event records are stored locally.
5. Bluetooth LE provides configuration, data retrieval, and notifications
   to a nearby phone or gateway.

Remote notifications require a gateway with an additional network
connection. The radio antenna will remain above water.

## Predictive Maintenance

The system aims to identify developing habitat problems and monitoring
equipment faults early enough to support inspection.

Examples include persistent warming, unusual water-level trends,
prolonged turbidity, sensor displacement, and declining battery condition.

Environmental alerts will indicate conditions requiring review.
They will not be presented as validated predictions of salmon mortality
or population decline.

Habitat interventions would remain decisions for conservation professionals.

## Use of Nordic nRF54LM20 DK

The DK will serve as the central platform for:

- Sensor acquisition
- Local feature extraction and analysis
- Edge AI inference
- Local data logging
- Bluetooth Low Energy communication
- Power-consumption evaluation

Axon NPU acceleration will be evaluated for a compatible model using
Nordic’s supported development tools. Initial firmware may use CPU
inference while the sensing and analysis workflow is validated.

## Preliminary Bill of Materials

This is a planning BOM for one development station.
Components are not yet purchased unless explicitly stated.

| Component | Quantity | Purpose | Selection status |
|---|---:|---|---|
| Nordic nRF54LM20 DK | 1 | Sensor acquisition, local processing, Edge AI, and Bluetooth LE | Required platform |
| Waterproof temperature probe | 1 | Measure water temperature | Model to be selected |
| Water-level sensor | 1 | Measure water-level changes | Sensing method and model to be selected |
| Turbidity sensor | 1 | Measure relative changes in suspended particles | Model to be selected |
| Accelerometer | 1, optional | Detect enclosure movement | Under evaluation |
| Local storage | 1 provision | Retain measurements during communication interruptions | Evaluate DK storage before adding hardware |
| Regulated power supply | 1 | Power the development prototype | To be selected |
| Battery and protection circuitry | 1 set | Evaluate autonomous operation | To be selected |
| Weather-resistant enclosure | 1 | Protect electronics | To be selected |
| Cable glands and mounting hardware | 1 set | Secure and protect installation | To be selected |
| Interface circuitry and connectors | 1 set | Provide compatible sensor connections | Depends on sensor selection |
| Controlled water-test rig | 1 | Validate sensing and event detection | To be designed |

Exact part numbers, voltage compatibility, prices, and supplier links
will be added after component evaluation.

The final paired monitoring system will require an expanded BOM.

## Validation Plan

Controlled tests will evaluate:

- Gradual warming
- Falling and rising water levels
- Sediment pulses
- Sensor disconnection or displacement
- Bluetooth interruptions and data recovery

Performance measures will include measurement agreement with reference
instruments, detection delay, false alarms, data completeness, memory
use, and power consumption.

Engineering tests will be distinguished from ecological validation.
Field evaluation would require appropriate authorization and guidance
from conservation specialists.

## Development Milestones

- [ ] Select sensors and verify electrical compatibility
- [ ] Implement sensor acquisition and local logging
- [ ] Implement Bluetooth configuration and data retrieval
- [ ] Build the controlled test rig
- [ ] Establish threshold and trend baselines
- [ ] Train and evaluate a compact Edge AI model
- [ ] Measure power consumption
- [ ] Document results and limitations
- [ ] Explore an authorized field pilot

## Background References

- [Nordic nRF54LM20 DK](https://www.nordicsemi.com/Products/Development-hardware/nRF54LM20-DK)
- [Nordic Edge AI](https://www.nordicsemi.com/Products/Technologies/Edge-AI)
- [Shei-Pa: Implications of Wuling Long-Term Ecological Monitoring](https://www.spnp.gov.tw/ch/titlelist/conservation-column/1654)
- [NTHU Salmon FAQ — historical background](https://life.nthu.edu.tw/~labtcs/Salmon/faq/faq_index.htm)
- [Sustain the System Competition Rules](https://www.hackster.io/contests/sustain-the-system/rules)

Historical references will be interpreted in their original time context.
