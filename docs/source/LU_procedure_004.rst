**Procedure Latch-Up Test**

Document Owner: Reliability Stress Lead

**Table of content**

1. Scope

2. Field of application

3. Process flow and RACI’s.

4. Detailed Description

5. Responsibilities

6. Escalation

7. Definition

8. Relevant Documents

1. **Scope**

The purpose of this document is to establish a clear procedure for IC
Latch-Up Test planning, executing, assessment and reporting.

2. **Field of Application**

This Procedure is applicable for all Melexis reliability sites

3. **Process flow and RACI’s**

+----------------+--------+--------+--------+--------+--------+--------+
| **Flow**       | **R    | **A    | *      | **Info | **R    | **Rec  |
|                | espons | ccount | *Consu | rmed** | elated | ords** |
|                | ible** | able** | lted** |        | docum  |        |
|                |        |        |        |        | ents** |        |
+================+========+========+========+========+========+========+
| LU request     | P      | Relia  | Relia  | Relia  | LU     | LU     |
| creation       | roject | bility | bility | bility | r      | r      |
|                | M      | Asse   | Stress | Stress | equest | equest |
|                | anager | ssment | Lead,  | Lead,  |        |        |
|                |        | En     | Design | Design |        |        |
|                |        | gineer | En     | En     |        |        |
|                |        |        | gineer | gineer |        |        |
+----------------+--------+--------+--------+--------+--------+--------+
| Review of LU   | Relia  | Relia  | Relia  | Relia  | LU     |        |
| request        | bility | bility | bility | bility | proc   |        |
|                | Asse   | Asse   | Stress | Stress | edure; |        |
|                | ssment | ssment | Lead,  | Lead,  | Q      |        |
|                | En     | m      | Design | Design | ualifi |        |
|                | gineer | anager | En     | Eng    | cation |        |
|                |        |        | gineer | ineer, | plan   |        |
|                |        |        |        | PM     |        |        |
+----------------+--------+--------+--------+--------+--------+--------+
| Electrical     | Relia  | Relia  | Relia  | Relia  | Test   | Data   |
| test before    | bility | bility | bility | bility | Instru | logs   |
| stress         | Ope    | Stress | Asse   | Asse   | ction, |        |
|                | rator, | Lead   | ssment | ssment | Q      |        |
|                | Tech   |        | Eng    | Eng    | ualifi |        |
|                | nician |        | ineer, | ineer, | cation |        |
|                |        |        | TE     | PM     | Plan   |        |
+----------------+--------+--------+--------+--------+--------+--------+
| LU tester      | Relia  | Relia  | Relia  | Relia  | LU     | C      |
| configuration  | bility | bility | bility | bility | proc   | onfigu |
|                | Tech   | Stress | Asse   | Asse   | edure; | ration |
|                | nician | Lead   | ssment | ssment | local  | file   |
|                |        |        | En     | En     | WI     |        |
|                |        |        | gineer | gineer |        |        |
+----------------+--------+--------+--------+--------+--------+--------+
| Execution of   | Relia  | Relia  | Relia  | Relia  | LU     | LU     |
| LU stress      | bility | bility | bility | bility | proc   | test   |
|                | Tech   | Stress | Asse   | Asse   | edure; | data   |
|                | nician | Lead   | ssment | ssment | local  | logs   |
|                |        |        | En     | En     | WI     |        |
|                |        |        | gineer | gineer |        |        |
+----------------+--------+--------+--------+--------+--------+--------+
| Electrical     | Relia  | Relia  | Relia  | Relia  | Test   | Data   |
| test Post PC   | bility | bility | bility | bility | Instru | logs   |
|                | Ope    | Stress | Asse   | Asse   | ction, |        |
|                | rator, | Lead   | ssment | ssment | Q      |        |
|                | Tech   |        | Eng    | Eng    | ualifi |        |
|                | nician |        | ineer, | ineer, | cation |        |
|                |        |        | TE     | P      | Plan   |        |
|                |        |        |        | roject |        |        |
|                |        |        |        | M      |        |        |
|                |        |        |        | anager |        |        |
+----------------+--------+--------+--------+--------+--------+--------+
| LU stress data | Relia  | Relia  | Relia  | Relia  | LU     | Report |
| (LU logs;      | bility | bility | bility | bility | proc   |        |
| electrical     | Tech   | Stress | Asse   | Asse   | edure; |        |
| test logs)     | nician | Lead   | ssment | ssment | local  |        |
| consolidation. |        |        | En     | En     | WI     |        |
| Report         |        |        | gineer | gineer |        |        |
| preparation    |        |        |        |        |        |        |
+----------------+--------+--------+--------+--------+--------+--------+
| Assessment on  | Relia  | Relia  | Relia  | P      | Re     | Re     |
| stress         | bility | bility | bility | roject | ports, | ports, |
| results.       | Asse   | Asse   | Stress | M      | Log    | Log    |
| Initiating of  | ssment | ssment | Lead,  | anager | Files, | Files, |
| failure        | En     | Team   | Design |        | FA     | FA     |
| analisys.      | gineer | Lead   | En     |        | r      | r      |
| Escalation in  |        |        | gineer |        | equest | equest |
| case of issues |        |        |        |        |        |        |
+----------------+--------+--------+--------+--------+--------+--------+

**
**

**LU stress flow chart:**

.. image:: media/image1.png
   :width: 3.96433in
   :height: 7.94365in

**
**

4. **Detailed Description**

4.1. Terms and definitions:

   *The following terms and definitions apply to this test method.*

**ATE:** Automated test equipment

**cool-down time:** The period of time between successive applications
of trigger pulses, or the period of time between the removal of the
Vsupply voltage and the application of the next trigger pulse. (See
Figure 2, Figure 3, Figure 4, and Table 3.)

**DUT:** The device under test.

**dynamic devices:** Devices requiring clocking in order to guarantee a
stable state while being tested.

**GND (Ground):** The common or zero-potential pin(s) of the DUT.

NOTE 1 Ground pins are not latch-up tested.

NOTE 2 A ground pin is sometimes called Vss.

**input pins:** All address, data-in control, Vref, and similar pins.

**I/O (bidirectional) pins:** Device pins that can be made to operate as
an input or an output or in a high-impedance state.

**Isupply:** The total supply current in each Vsupply pin (or pin group)
with the DUT biased as indicated in Table 2.

**I-test:** A latch-up test that supplies positive and negative current
pulses to the pin under test.

**latch-up:** A state in which a low-impedance path, resulting from an
overstress that triggers a parasitic thyristor structure, persists after
removal or cessation of the triggering condition.

NOTE 1 The overstress can be a voltage or current surge, an excessive
rate of change of current or voltage, or any other abnormal condition
that causes the parasitic thyristor structure to become regenerative.

NOTE 2 Latch-up will not damage the device provided that the current
through the low-impedance path is sufficiently limited in magnitude or
duration.

**logic-high:** A level within the more positive (less negative) of the
two ranges of logic levels chosen to represent the logic states.

NOTE 1 For digital devices, the maximum value of the high logic level
voltage is used for latch-up testing. Themaximum logic high level is
designated as Vmax.

NOTE 2 For non-digital devices, the maximum operating voltage that can
be applied to that pin as defined in the device specification is used
for latch-up testing.

**logic-low:** A level within the more negative (less positive) of the
two ranges of logic levels chosen to represent the logic states.

NOTE 1 For digital devices, the minimum value of the low logic level
voltage is used for latch-up testing. The minimum logic low level is
designated as Vmin.

NOTE 2 For non-digital devices, the minimum operating voltage that can
be applied to that pin as defined in the device specification is used
for latch-up testing.

**maximum Vsupply; maximum operating voltage:** The maximum supply
voltage at which a device is specified to operate in compliance with the
applicable device specification.

NOTE 1 **“**\ Maximum” refers to the magnitude of supply voltage and can
be either positive or negative.

NOTE 2 The maximum voltage is **not the absolute maximum rated voltage,
i.e., the voltage beyond which permanent damage is likely.**

*maximum stress voltage (MSV):* The maximum voltage allowed to be placed
on any given pin during latch-up immunity testing without causing
catastrophic damage to the device due to electrical over-stress (EOS)
not related to latch-up.

NOTE 1 **MSV is higher than the maximum operating voltage**.

NOTE 2 **MSV is NOT the same as the absolute maximum voltage rating**
from the device data sheet. MSV applies to latch-up testing only,
protecting the DUT from physical damage due to stress mechanisms not
directly related to latch-up. An example of an unrelated stress is one
exceeding the destructive breakdown voltage of a pin resulting in EOS
damage. MSV may be different for each pin and each polarity during
testing, depending on process technology and circuit topology. Further,
the MSV value depends on the pulse width used during latch-up testing.
Shorter pulse widths may allow a higher value for MSV. Therefore, the
MSV value chosen should take into account the pulse width as well as
process technology and circuit topology.

**“no connect” pin:** A pin that has no internal connection and that can
be used as a support for external wiring without disturbing the function
of the device.

NOTE All “no connect” pins shall be left in an open (floating) state
during latch-up testing.

**nominal Isupply (Inom):** The measured dc supply current for each
Vsupply pin (or pin group) with the DUT biased at the test temperature
as defined in clause 7.3 and Table 2.

**output pin:** A device pin that generates a signal or voltage level as
a normal function during the normal operation of the device.

NOTE Output pins, though left in an open (floating) state during testing
of other pin types, are latch-up tested.

**preconditioned pin:** A device pin that has been placed in a defined
state or condition (input, output, high impedance, etc.) by applying
control vectors to the DUT.

**test condition:** The test temperature, supply voltage, current
limits, voltage limits, clock frequency, input bias voltages, and
preconditioning vectors applied to the DUT during the latch-up test.

**timing-related input pin:** A pin such as clock crystal oscillator,
charge pump circuit, etc., required to place the DUT in a normal
operating mode.

NOTE Required timing signals may be applied by the latch-up tester,
external equipment, and/or external components as appropriate.

**trigger pulse:** The positive or negative current pulse (I-Test) or
voltage pulse (Vsupply overvoltage test) applied to any pin under test
in an attempt to induce latch-up (see Figure 2, Figure 3 and Figure 4).

**trigger duration:** The duration of an applied pulse from the trigger
source. (See Figure 2, Figure 3, Figure 4 and Table 3.)

**VDD Tolerant I/O:** Some applications require that the I/O pin voltage
be independent of the supply voltage level (higher or lower). In both
cases a diode between the supply pin and I/O pin is not present, thus
the I/O pin voltage will not be clamped internally. The Vabsmax of these
specific pins will be different from the other pins and could also be
limited by the process. Testing above Vabsmax would require setting the
MSV according to the process limit (MSV set by process).

**VSS tolerant I/O:** Some applications require I/O pins to have a
minimum voltage level less than VSS where a diode between I/O and VSS is
not present. These pins must be tested to 1.5 x Vabsmin. MSV needs to be
set according to the process limit (MSV set by process).

**Vsupply pin (or pin group):** All DUT power supply and external
voltage source pins (excluding ground pins), including both positive-
and negative-potential pins.

NOTE 1 Generally, it is permissible to treat equal-potential voltage
source pins as one Vsupply pin (or pin group) and connect them to one
power supply.

NOTE 2 When forming Vsupply pins (or pin groups), the combination of
Vsupply pins with significantly different supply current levels is not
recommended as this would make it difficult to detect significant
current changes on low supply current pins.

**Vsupply overvoltage test:** A latch-up test that supplies overvoltage
pulses to the Vsupply pin under test.

4.2. Classification:

There are two classes for latch-up testing.

*Class I* is for testing at room temperature ambient.

*Class II* is for testing at the maximum operating ambient temperature
(Ta) or maximum operating case temperature (Tc) or maximum operating
junction temperature (Tj) in the data sheet.

For Class II testing at the maximum operating Ta or Tc, the ambient
temperature or case temperature (Tc) shall be established at the
required test value. For Class II testing at the maximum operating Tj,
the ambient temperature Ta or the case temperature Tc should be selected
to achieve a temperature characteristic of the junction temperature for
a given device operating mode(s) during latch\ **-**\ up testing. The
values used in Class II testing shall be recorded in the final report.

**According to AEC Q100-004 (qualification of automotive IC), latch-up
test shell be performed at maximum ambient operating temperature (JEDEC
Class II) with following stress conditions. In case of qualification of
non-automotive IC other conditions can be used according to
qualification plan and/or engineering judgment:**

**Positive I-test current** = (Inom+100 mA) or 1.5 (Inom) whichever is
greater, with voltage clamped at 1.5 times maximum logic high or MSV
whichever value provides maximum stress without creating an EOS
condition.

**Negative I-test current** =-100 mA or -0.5 (Inom) whichever is greater
in magnitude, with voltage clamped at -0.5 times maximum logic high or
MSV whichever value provides maximum stress without creating an EOS
condition. For VSS tolerant pins the voltage clamp must be set to -1.5
times minimum logic low.

**Vsupply overvoltage test** = 1.5 (Vmax) or MSV whichever value
provides maximum stress without creating an EOS condition.

Recommended range of current and voltage stress, according to JESD78,
presented in Table 1.

.. image:: media/image2.png
   :width: 6.92569in
   :height: 4.05972in

4.3. General latch-up test procedure:

Prior to the latch-up test, the device needs to be in a stable state
with reproducible Inom. Engineering judgment may be needed to achieve
sufficient stability. The supply current should be made as low as
practicable. The supply current must be stable enough and low enough to
reliably detect the supply current increase if latch-up occurs. A
minimum of six (6) devices shall be subjected to latch-up testing using
the I-test and supply over-voltage test. It is allowed to partition
I-test, supply over-voltage test, or test combinations by using at least
6 fresh devices for each partition. All devices to be latch-up tested
must have passed ATE testing to the device specification requirements.
Before latch-up testing, the device continuity in the socket should be
checked to avoid false latch-up failures. The devices to be tested shall
be subjected to the test conditions specified in Table 2 and Table 3.
All “no connect” pins on the DUT shall be left open (floating) at all
times.

All pins on the DUT, with the exception of “no connect” pins and timing
related pins, shall be latch-up tested. The Input, output, and
configurable I/O pins are to be tested with the I-test and the Vsupply
pins tested with the Overvoltage test. This includes special pins
defined in Annex A. The passing current or voltage values for the
special pins can be used for determining the values of the
passive-components connected to the pins. I/O pins shall be tested in
all possible operating states or the worst case operating state
(typically high impedance for configurable I/O pins). Dynamic devices
shall be tested per 7.4.3. When a device is sufficiently complex that
testing of all configurable I/O pins in the worst case condition is not
practicable, the device should be conditioned with a set of vectors
representative of the typical operation of the device as determined by
engineering judgment. When an I/O pin cannot be tested in the high
impedance state, the I/O shall be tested in a valid logic state.
Untested pins and pins that could not be completely tested shall be
recorded and the user shall be informed of all I/O pins that were not
tested or tested in all states. After latch-up testing, all devices must
pass the failure criteria specified in clause 7.5.

.. image:: media/image3.png
   :width: 6.92569in
   :height: 3.60486in

**
**

**Table 2 (continuation)**

.. image:: media/image4.png
   :width: 6.92569in
   :height: 4.60694in

4.4. Detailed latch-up test procedure:

   4.4.1. I-test

The I-test shall be performed as follows:

1. The devices shall be subjected to the I-test as indicated in Figure
   1/Table 2 and Figures 2 and 3/Table 3.

2. Bias the DUT as indicated in Figure 5 (see 4.4.5). All input pins,
   including bi-directional I/O pins in an input state or high impedance
   state, not used for preconditioning the I/O pins, shall be tied to
   the maximum logic-high level specified in the device specification.
   Input pins used for preconditioning must be tested in their defined
   state (pins that are tied to a logic-high level to precondition the
   DUT can only be tested in the logic-high state; pins that are tied to
   a logic-low level to precondition the DUT can only be tested in the
   logic-low state). Allow the DUT to stabilize at the test temperature.

3. Put the pin under test in logic-high state. Measure nominal Isupply
   (Inom) for each Vsupply pin (or pin group). Then, apply the positive
   current trigger (per Table 2 for a duration as specified in Table 3)
   to the pin under test.

4. After the trigger source has been removed, return the pin under test
   to the level it was in before the application of the trigger pulse,
   and measure the Isupply for each Vsupply pin (or pin group). If any
   Isupply is greater than or equal to the failure criteria specified in
   Table 2, latch-up has occurred and power must be removed from the
   DUT. If latch-up has occurred, stop the test; the DUT has failed
   latch-up testing. Using a new part, return to step 1 and continue
   testing.

5. If latch-up has not occurred, after the necessary cool-down time (see
   Table 3), repeat steps 3 and 4 for all pins to be tested (noting the
   exceptions stated in step 2).

.. image:: media/image5.png
   :width: 5.04782in
   :height: 3.14167in

.. image:: media/image6.png
   :width: 5.23333in
   :height: 3.2482in

6.  Repeat steps 2 through 5 with all input pins, including
    bi-directional I/O pins in an input state or high impedance state,
    not used for preconditioning the I/O pins tied to the minimum
    logic-low level specified in the device specification.

7.  Bias the DUT as indicated in Figure 6 (see 4.4.5) with all input
    pins, including bi-directional I/O pins in an input state or high
    impedance state, not used for preconditioning the I/O pins shall be
    tied to the maximum logic-high level specified in the device
    specification (noting the exceptions stated in step 2).

8.  Put the pin under test in logic-low state. Measure nominal Isupply
    (Inom) for each Vsupply pin (or pin group). Then, apply the negative
    current trigger source below ground (per Table 2 for a duration as
    specified in Table 3) to the pin under test.

9.  After the trigger source has been removed, return the pin under test
    to the level it was in before the application of the trigger pulse
    and measure the Isupply for each Vsupply pin (or pingroup). If any
    Isupply is greater than or equal to the failure criteria specified
    in Table 2, latch-up has occurred and power must be removed from the
    DUT. If latch-up has occurred, stop the test; the DUT has failed
    latch-up testing. Using a new part, return to step 1 and continue
    testing.

10. If latch-up has not occurred, after the necessary cool-down time
    (see Table 3), repeat steps 8 and 9 for all pins to be tested.

11. Repeat steps 8 through 10 with all input pins, including
    bi-directional I/O pins in an input state or high impedance state,
    not used for preconditioning the I./O pins tied to the minimum
    logic-low level specified in the device specification (noting the
    exceptions stated in step 2). I-test in 4.4.1 does not require the
    removal of power-supply voltage between stresses, i.e., cool-down
    time. Users should evaluate the risk of leaving the power-supply on.

..

   4.4.2. Vsupply overvoltage test

The Vsupply overvoltage test shall be performed on each Vsupply pin (or
pin group) as indicated below. To provide a true indication of latch-up
for given test conditions input pins configured as logic-high shall
remain within the valid logic-high region as defined in the device
specification (typically greater than 70% of the Vsupply overvoltage
test level). If input pin levels fall outside of the valid logic-high
region, the device may change state causing a change in Inom and invalid
test data. If a latch-up failure occurs when the input pin(s) fall
outside of the valid logic-high region, engineering judgment must be
used to determine whether the failure is a valid latch-up condition or a
failure caused by a change in state.

1. The devices shall be subjected to the Vsupply overvoltage test as
   indicated in Figure l/Table 2 and Figure 4/Table 3.

2. Bias the DUT as indicated in Figure 7 (see 4.4.5). All input pins,
   including bi-directional I/O pins in an input state or high impedance
   state, not used for preconditioning the I/O pins shall be tied to the
   maximum logic-high level specified in device specification. Input
   pins used for preconditioning must be tested in their defined state
   (pins that are tied to a logic-high level to precondition the DUT can
   only be tested in the logic-high state, pins that are tied to a
   logic-low level to precondition the DUT can only be tested in the
   logic-low state). Allow the DUT to stabilize at the test temperature.
   Measure nominal Isupply (Inom) for each Vsupply pin (or pin group) at
   this time.

3. Apply the voltage trigger source (per Table 2 for a duration as
   specified in Table 3) to the Vsupply pin (or pin group) under test.

4. After the trigger source has been removed, return the Vsupply pin
   under test to the state it was in before the application of the
   trigger pulse and measure the Isupply for each Vsupply pin (or pin
   group). If any Isupply is greater than or equal to the failure
   criteria specified in 4.4.5, latch-up has occurred and power must be
   removed from the DUT. If latch-up has occurred stop the test; the DUT
   has failed latch-up testing. Using a new part, return to step 1 and
   continue testing.

5. If latch-up has not occurred, after the necessary cool-down time (see
   Table 3), repeat steps 2 through 4 with all input pins, including
   bi-directional I/O pins in an input state or high impedance state,
   not used for preconditioning the I/O pins tied to the minimum
   logic-low level specified in the device specification (noting the
   exceptions stated in step 2).

6. Repeat steps 2 through 5 until each Vsupply pin (or pin group) has
   been tested.

.. image:: media/image7.png
   :width: 4.55in
   :height: 2.90574in

   4.4.3. Testing dynamic devices

Devices that during normal operating conditions have a clock and/or
other timing signal inputs may be latch-up tested in a static manner. If
the device does not show a stable Isupply (Inom) measurement or appears
to latch up, the clock and/or other associated timing and control
signals, as defined in the device specification, may be applied to the
device during latch-up testing per 4.4.1and 4.4.2. Unless otherwise
specified, the clock pins and other associated timing pins used to place
the device in a stable state shall not be latch-up tested while being
used to stabilize the device. The supplier shall maintain records
indicating how the device was tested.

   4.4.5. Timing specifications and Equivalent circuits for LU testing

.. image:: media/image8.png
   :width: 4.97604in
   :height: 2.45833in

.. image:: media/image9.png
   :width: 4.12504in
   :height: 3.225in

.. image:: media/image10.png
   :width: 4.24011in
   :height: 3.15in

.. image:: media/image11.png
   :width: 4.01353in
   :height: 2.08383in

.. image:: media/image12.png
   :width: 4.07238in
   :height: 3.23978in

   4.4.6. Latch-up detection criteria

A device is considered to have experienced latch-up if it meets the
latch-up detection criteria listed in Table 2 or it does not pass the
device ATE requirement. ATE testing is required to detect damage from
short duration latch-up events or EOS that may occur during latch-up
stress.

NOTE 1 Comments on ATE testing following latch-up stress:

‐ Latch-up events triggered during supply over-voltage or current
injection tests may damage the device, and the damage could end the
latch-up event before the latch-up tester detects the failure
(short-duration latch-up). An ATE test failure may be the only
indication of this kind of latch-up.

‐ Latch-up test current injection could directly damage the DUT through
EOS without an actual latch-up event. ATE testing can be used to confirm
this source of device damage.

‐ These damage sources (undetected short-duration latch-up events and
EOS) may prevent proper control of the device during automated latch-up
testing and could invalidate some latch-up test results for some pins on
the device.

NOTE 2 ATE failure disposition guidelines:

‐ If the ATE failure is suspected to be caused by an ESD issue (not
latch-up stress), repeat the latch-up test with fresh samples.

‐ If the ATE failure is suspected to be caused by EOS damage during
latch-up stress, adjust the trigger pulse according to Table 3, and
repeat the latch-up test with fresh samples.

‐ If the samples still fail ATE test after the above evaluation the
device fails Level A latch-up. On fresh samples the IO trigger current
can be adjusted to a value at which the integrated circuit can pass the
latch-up test as well as ATE following latch-up test.

   4.4.7. Reporting/Archiving

All results/conditions (temperature, stress conditions for each pin) of
the latch-up test should be included in Reliability Test Latch-Up
Report.

Test logs of ATE verification prior / after stress should be collected,
analyzed and archived.

5. **Responsibilities**

Local Reliability Stress lead is responsible to carry out this
procedure.

**
**

6. **Escalation**

Level #1: Reliability stress lead, Reliability assessment manager

Level #2: Global Reliability Manager

Level #3: Global Quality Manager

7. **Definition**

See section 4.1

8. **Relevant Documents**

-  Stress Test Qualification for Integrated Circuits
   `AEC-Q100 <http://www.aecouncil.com/Documents/AEC_Q100_Rev_H_Base_Document.pdf>`__

-  IC Latch-Up Test
   `AEC-Q100-004 <http://www.aecouncil.com/Documents/AEC_Q100-004D.pdf>`__

-  IC Latch-Up Test
   `JESD78 <https://www.jedec.org/system/files/docs/JESD78E.pdf>`__

-  Reliability and Qualification Procedure
   `3419013 <http://docserver.melexis.com/data/3/3419013M003.DOC>`__

-  Template Reliability Test Request
   `3419004 <http://docserver.melexis.com/prog/3/showdoc.cfm?DOCUMENT=3419004>`__

-  Template Reliability Test Latch-Up Report
   `341900301 <http://docserver.melexis.com/prog/3/showdoc.cfm?DOCUMENT=341900301>`__

-  WI XTA based HV LU tester (Kiev, Ieper) 321649

-  WI LU tester (Erfurt) Paper manual. Electronic version is under
   construction
