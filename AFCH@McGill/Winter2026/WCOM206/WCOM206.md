Add Questions tonight (due 11:59)
Respond tomorrow (due 11:59)

Do Oral Critique assignment tomorrow (due 11:59)

Business proposal due 4/16, with meeting minutes
## Tokamak Presentation
How manage temp before reactor running/downtime
Toxicity hazard for maintenance?
Does putting it outside the vacuum vessel cause problems with ITER use case?
	Is it an easy retro fit to ITER
	If need to rebuild vacuum vessel, is it a drop in replacement
Module vs Tank wrt use in ITER
Structure -> Inconel, cost increase?
~~Much lower heat capacity (1/2), does cause problems?~~

## Venus Presentation
Lot of detail on chosen alloy, less so on other alloys weaknesses
Molten Salt is a interesting (good) choice
	1kWh
RTG output?
	83 W
How to test/prove/readiness
Benefits of push-pull
	Especially over 4wd
Camera: Why 360deg
**What reactions are being done, if steering is purely mechanical**
Is data filtration necessary on-board? (asked)
	How to know if something is meaningful
	Send more, or collect less
Keep memory free in case of emergencies?
VHF?? Absorption? (100MHZ)
Compared to UHF, but not HF? would seem better for thicker atm
More could have been explained about SiC
Lot of AI images
Overall mass, and LV needed for launch/transfer


Given that the current geopolitical situation is rapidly evolving and volatile, it is important to note that our current pricing models were developed with historical data. Our airship has been designed in order to minimize the amount of helium used (and especially the amount lost), so we would be less affected by rising helium costs. To obtain large quantities of helium, our proposal would be limited to the current sources, although due to the development timeline, we are not able to determine how much present instability would affect the cost.
A 200 ton payload capacity was chosen to provide substantial cargo capabilities, which allow us to reduce the cost/kg, and operate fewer airships. This also allows us to move both larger and heavier cargoes, which is important to permit growth in the arctic regions, specifically enabling larger water-treatment plants, industrial operations, and potentially transport for defence use cases. This increases our efficiency, as our fixed operational costs are distributed over a much larger cargo. Our proposal neither aims to compete with planes, nor replace them, as our design is fundamentally slower, regardless of payload mass.

Thank you for your questions, I will address a few of them below:

Envelope Life Cycle
We recognize that hydrogen is a very hard substance to contain, especially in these volumes. A key focus of the testing we will be conducting is into the effects of hydrogen on the envelope materials, by simulating permeation in a variety of conditions. The full-scale airship will be a rigid design, using numerous gas bags, so the hydrogen will not need to be pressurized substantially, which will help to increase the lifespan. Additionally, we will verify that our multi-layered design is successful in slowing the rate of damage to the structural layers of the envelope material. We expect a minimum of 2 years of lifespan per gas bag, although are hopeful that performance will far exceed that minimum. Additionally, the work required to repair or replace a gas bag is lessened due to the smaller size.

Fuel Reclamation/Buoyancy
Exhaust condensers are not essential to our design, but could be explored during the testing phase if necessary. As we model routes more closely, and gain a better understanding of typical fuel burn amounts, we will assess if this recovery is necessary for our desired operating margins. In order to make these vents more economical, we will explore the possibility of venting hydrogen gas through the turbine, where it is combusted, in order to recoup some energy from the gas, decreasing fuel burn slightly, and making our vents less of a flammability hazard. This supplemental system would be thoroughly tested during the testing phase, with the intent to deploy it on the full-scale airship, unless significant issues were observed.












# Post template

**_2026-04-11 - AV Bay SW Intergration_**

* Goal: Verify SW for FC with Backplane
* Location: Workshop
* Personnel:
* Tested Component(s)/System: FC SN01, Backplane, AV Bay Radio: 433-SN2, PCB
* Test Setup Description: AV Bay with FC, System A Pad and Control Station radios
    * SW commit (with link):
* Desired Result: FC sends and receives telemetry and commands end to end, while powered off of 25.2V
* Result: FC was able to send telemetry, and receive commands, and correctly was able to send packets with BAD and NAK flags, when the commands were unable to be completed, or was a NOP, respectively. Ground Station correctly parsed the flags in the packet.
* Ensuing Design Adjustments:
* Will a report be provided?: Yes/No


**_2026-04-11 - AV Bay HW Intergration_**

* Goal: Verify HW for FC with Backplane
* Location: Workshop
* Personnel:
* Tested Component(s)/System: FC SN01, Backplane, AV Bay Radio: 433-SN2, PCB
* Test Setup Description: AV Bay with FC, 25.2V from power supply
    * SW commit (with link):
* Desired Result: FC operates correctly on 25.2V, with CAN communication for Prop Top/Bottom
* Result: CAN was unable to be tested due to a short in Prop Top (Short is in VBat, runs correctly off USB-C, but not power supply set to 0.2A through backplane). Additionally, the FC 
* Ensuing Design Adjustments:
* Will a report be provided?: Yes/No





Tested 433SN2, and 900SN2 (Both bodged and unbodged) radio boards. Both 900 boards caused the FC to reset when radio power was enabled. Problem suspected to be in the backplane.

All end-to-end testing was done with the 433 radio boards

