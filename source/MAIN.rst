====
MAIN
====

MAIN-1 Interlocks and Scram Features
====================================

INTRODUCTION
------------

A. Purpose
^^^^^^^^^^
This procedure is the calibration and functional check of the instrument, control and safety (ICS) system for the TRIGA reactor. Systems subject to this procedure are:
- Control console programs
- Operation control interlocks
- Control rod safety system

Three functional criteria for the procedure are:
1. Verify the conditions of the ICS system to meet the minimum requirements of the License Technical Specifications.
2. Verify the condition of the ICS system meets the broader quality assurance requirements of the ICS system design.
3. Assure **NO** task or action of this procedure is a proposed change, test, or experiment in the sense of 10CFR50.59

B. Description
^^^^^^^^^^^^^^
The instrument control and safety system is a digital processing system that monitors analog and digital signals, displays information for the operator, and logs data. Operators interact with the system to determine control of operation modes and rod positions. The safety system function is independent of the ICS system programs.

This procedure systematically examines key program features that determine ICS system interlocks and that implement ICS system SCRAM functions.

C. Schedule
^^^^^^^^^^^
Schedule procedure twice each year, at six month intervals not to exceed 7.5 months from previous completion of check.

D. Contents
^^^^^^^^^^^
A. Introduction ............................................................. Page 4  
B. Interlock Checks ......................................................... Page 5  
C. SCRAM Functions ........................................................... Page 7  
D. Instructions  
   - 1.0 Operator Log on:off ................................................ Page 9  
   - 2.0 Manual Mode ......................................................... Page 11  
   - 2.1 Entering Manual Mode ................................................ Page 11  
   - 2.2 Exiting Manual Mode ................................................. Page 11  
   - 2.3 Initiation and Termination ......................................... Page 11  
   - 2.4 Operation in Manual ................................................ Page 13  
   - 3.0 Auto Mode ........................................................... Page 16  
   - 3.1 Entering Auto Mode .................................................. Page 16  
   - 3.2 Exiting Auto Mode ................................................... Page 16  
   - 3.3 Initiation and Termination ......................................... Page 17  
   - 3.4 Operation in Auto Mode ............................................. Page 19  
   - 4.0 Pulse Mode .......................................................... Page 20  
   - 4.1 Initiating Pulse Mode .............................................. Page 20  
   - 5.0 Square Mode ......................................................... Page 22  
   - 5.1 Initiating Square Mode ............................................. Page 23  
   - SCRAM Functions  
   - 6.0 Redundant Network ................................................ Page 25  
   - 7.0 SCRAM Mode ........................................................ Page 26  
   - 7.1 CSC Program Logic ................................................ Page 30  
   - 7.2 DAC Program Logic ................................................ Page 31  
   - 7.3 NM1000 Program Logic ............................................. Page 33  
   - 7.4 Pulse Mode Features .............................................. Page 33  

E. Attachments
^^^^^^^^^^^^^^
*Note: Attachments are not part of this procedure but may be useful when performing this procedure.*
1. ICS Interlocks ........................................................... Page 2  
2. ICS SCRAMS ............................................................... Page 6  
3. Acceptance ............................................................... Page 7  

F. Equipment, Materials
^^^^^^^^^^^^^^^^^^^^^^^
1. ICS system keys  
2. Multi-meter Fluke 87 or equivalent device  
3. Multi-source Keithley 263 or equivalent device  
4. Test instrument cables and probes  

G. References, Other Procedures
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
1. ANSI N323  
2. Radiation Monitor Manual  
3. Particulate CAM Manual  
4. Gas CAM Manual  
5. OPER-6 Reactor Bay Systems  


PROCEDURE
---------

A. Introduction
^^^^^^^^^^^^^^^

**Log all console operations for diagnostic work, maintenance, surveillance, calibration and test with the password** `MIRAGE`.

1. Review calibration and functional check requirements. Follow the instructions of each section.  
2. Discontinue operation if any procedure is not successful.  
3. Run pre-startup checks to verify operable conditions. Approval by reactor supervisor required.  
4. File procedure records and pre-start checklist.  
5. Return to normal operation.

Two types of annunciation conditions may occur:
- First: detection of a failure (audible alarm)
- Second: warning of system problem (no alarm)


B. Interlock Check Conditions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**This section of the OCS system procedures tests interlocks.**

**D.1 Prerequisite Conditions:**

+---------+-------+------------------------------------------------------------+
| Section | Steps | Description                                                |
+=========+=======+============================================================+
| 1.0     | 2-7   | Password required for magnet key switch                    |
| 1.0     | 8-10  | Log ON allows replacement of active operator               |
| 1.0     | 11-16 | Log OFF requires SCRAM mode                                |
+---------+-------+------------------------------------------------------------+

**D.2 Manual Mode Conditions:**

+---------+--------+----------------------------------------------------+------------------+
| Section | Steps  | Description                                        | Tech Spec        |
+=========+========+====================================================+==================+
| 2.3     | 2-5    | SCRAM to Manual mode requires log on               |                  |
+---------+--------+----------------------------------------------------+------------------+
| 2.3     | 6-9    | Acknowledge SCRAM to reset magnet key and enter    |                  |
|         |        | manual                                             |                  |
+---------+--------+----------------------------------------------------+------------------+
| 2.4     | 10-15  | Simultaneous withdrawal only one rod up at a time  | 4.2.2 (3.2.2b)   |
+---------+--------+----------------------------------------------------+------------------+
| 2.4     | 14     | Magnet/air switch interrupt power briefly          |                  |
+---------+--------+----------------------------------------------------+------------------+
| 2.4     | 16-18  | Transient rod acts as normal rod                   | 4.2.2 (3.2.2b)   |
+---------+--------+----------------------------------------------------+------------------+
| 2.4     | 19     | Fire button works only if drive is down            | 4.2.2 (3.2.2b)   |
+---------+--------+----------------------------------------------------+------------------+
| 2.4     | 20     | No withdrawal unless neutron source level present  | 4.2.2 (3.2.2b)   |
+---------+--------+----------------------------------------------------+------------------+

D.3 Auto Mode Conditions:
"""""""""""""""""""""""""

+---------+--------+------------------------------------------------------------+-------------------+
| Section | Steps  | Description                                                | Tech Spec         |
+=========+========+============================================================+===================+
| 3.3     | 3-5    | No operator prevents entry                                 |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 3.3     | 6-7    | Auto mode allowed if shim 1 & 2 are down                   |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 3.3     | 8-9    | Neutron source check for rod movement                      | 4.2.2 (3.2.2a)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 3.3     | 10-11  | Up motion limit excludes Reg rod                           | 4.2.2 (3.2.2b)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 3.3     | 12     | Fire button for transient rod if drive is down             | 4.2.2 (3.2.2c)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 3.4     | 1-5    | Regulating rod motion limited to 3-5 sec                   |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 3.4     | 7      | Rod magnet switch changes to manual mode                   |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 3.4     | 8      | Manual scram switches to scram mode                        |                   |
+---------+--------+------------------------------------------------------------+-------------------+

D.4 Pulse Mode Conditions:
"""""""""""""""""""""""""""

+---------+--------+------------------------------------------------------------+-------------------+
| Section | Steps  | Description                                                | Tech Spec         |
+=========+========+============================================================+===================+
| 4.1     | 1-4    | Prevent entry into pulse ready                             |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 4.1     | 5-9    | Transient rod air off                                      |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 4.1     | 10-11  | Power < 1kW                                                | 4.2.2 (3.2.2c)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 4.1     | 12-13  | 1 DPM limit for pulse mode                                 |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 4.1     | 18-20  | Transient rod needs neutron level                          | 4.2.2 (3.2.2a)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 4.1     | 21-23  | Withdrawal interlock, no standard rod motion               | 4.2.2 (3.2.2d)    |
+---------+--------+------------------------------------------------------------+-------------------+

D.5 Square Wave Mode Conditions:
"""""""""""""""""""""""""""""""""

+---------+--------+------------------------------------------------------------+-------------------+
| Section | Steps  | Description                                                | Tech Spec         |
+=========+========+============================================================+===================+
| 5.1     | 1-4    | Prevent entry into square mode                             |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 5.1     | 5-9    | Transient rod air off                                      |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 5.1     | 10-11  | Power < 1kW                                                | 4.2.2 (3.2.2c)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 5.1     | 12-13  | 1 DPM limit                                                |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 5.1     | 18-20  | No pulse if no neutron source                              | 4.2.2 (3.2.2a)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 5.1     | 21-23  | Interlock: no standard rod motion                          | 4.2.2 (3.2.2d)    |
+---------+--------+------------------------------------------------------------+-------------------+

C. SCRAM Functions
^^^^^^^^^^^^^^^^^^

This section tests ICS safety circuit functions.  
SCRAM functions are independent of the digital control program.  
Several digital SCRAM conditions and system checks are also program-dependent.

D.6/7 Digital Control Program:
""""""""""""""""""""""""""""""

+---------+--------+------------------------------------------------------------+-------------------+
| Section | Steps  | Description                                                | Tech Spec         |
+=========+========+============================================================+===================+
| 6.0     | 1-10   | SCRAM for database timeout or network failure              |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.1     | 2      | SCRAM for CSC scanner timeout                              |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.1     | 3-8    | SCRAM for CSC watchdog timeout                             | 4.2.3 (3.2.3f)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.2     | 2      | SCRAM for DAC scanner timeout                              |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.2     | 3-8    | SCRAM for DAC watchdog timeout                             | 4.2.3 (3.2.3f)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.4     | 2      | NP1000 pulse mode gain relay                               |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.4     | 2      | NP1000/NM1000 pulse mode bypass relay                      |                   |
+---------+--------+------------------------------------------------------------+-------------------+

D.7 Fuel Temperature:
"""""""""""""""""""""

+---------+--------+------------------------------------------------------------+-------------------+
| Section | Steps  | Description                                                | Tech Spec         |
+=========+========+============================================================+===================+
| 7.0     | 2      | FT#1 SCRAM at 550°C                                        | 4.2.3 (3.2.3a)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.0     | 3      | FT#2 SCRAM at 550°C                                        | 4.2.3 (3.2.3a)    |
+---------+--------+------------------------------------------------------------+-------------------+

D.7 Power Safety Channels:
"""""""""""""""""""""""""""

+---------+--------+------------------------------------------------------------+-------------------+
| Section | Steps  | Description                                                | Tech Spec         |
+=========+========+============================================================+===================+
| 7.0     | 4      | NPP1000 high percentage power                              | 4.2.3 (3.2.3b)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.0     | 4      | NPP1000 high pulse peak power                              | 4.2.3 (3.2.3b)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.0     | 5      | NP1000 high percent power                                  | 4.2.3 (3.2.3b)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.0     | 9-10   | NM1000 high/low voltage                                    | 4.2.3 (3.2.3b)    |
+---------+--------+------------------------------------------------------------+-------------------+

D.7 Operable Systems:
""""""""""""""""""""""

+---------+--------+------------------------------------------------------------+-------------------+
| Section | Steps  | Description                                                | Tech Spec         |
+=========+========+============================================================+===================+
| 7.0     | 6      | Manual pushbutton SCRAM                                    | 4.2.3 (3.2.3d)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.0     | 7      | Magnet key switch SCRAM                                    | 4.2.3 (3.2.3e)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.0     | 8      | Magnet voltage/ground detection                            |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.0     | 9-10   | NM1000 high/low voltage                                    | 4.2.3 (3.2.3b)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.0     | 11-12  | NM1000 Hi% or Lo voltage                                   | 4.2.3 (3.2.3c)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.0     | 13-14  | NPP1000 high voltage loss                                  | 4.2.3 (3.2.3c)    |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.0     | 17     | SCRAM for low pool level                                   |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.3     | 2      | SCRAM for NM1000 communication fault                       |                   |
+---------+--------+------------------------------------------------------------+-------------------+
| 7.3     | 4      | SCRAM for NM1000 database timeout                          |                   |
+---------+--------+------------------------------------------------------------+-------------------+

MAIN-2 Instrument System Features
=================================

I. INTRODUCTION
---------------

A. Purpose
~~~~~~~~~~
The purpose of this procedure is the calibration and functional check of the instrument control and safety (ICS) system for the TRIGA reactor. Systems subject to this procedure are the key instrument systems that monitor the control rod power supply, fuel element temperatures and the neutron flux levels or reactor power levels.

Three functional criteria for the procedure are:
  (1) Verify the conditions of the ICS system meet the minimum requirements of the License Tech. Specs.
  (2) Verify the conditions of the ICS system meet the broader quality assurance requirements of the ICS system design.
  (3) Assure no task or action of this procedure is a proposed change, test, or experiment in the sense of 10CFR50.59.

B. Description
~~~~~~~~~~~~~~
The instrument control and safety system is a digital processing system that monitors analog and digital signals, displays information for the operator and logs data. Operator interactions with the system determine control of operation modes and rod positions. Safety system function is independent of the ICS system programs. This procedure provides instructions for the calibration, check and test of key instrument systems that monitor reactor operation. These systems include the magnet power supply, two fuel temperature channels and three neutron measurement channels. Two other procedures are necessary for the calibration of the fuel temperature channels and alignment of the neutron flux channels for reactor power calibration.

C. Schedule
~~~~~~~~~~~
Schedule procedure once each year, prior to the completion of MAIN1. Plan procedure task for the month of July but no later than 15 months from previous work. The requirement to complete MAIN2 prior to MAIN1 will limit the no later than 15 months to no later than 7.5 months.

D. Contents
~~~~~~~~~~~

+----------------------------------------------+------+
| SECTION                                      | Page |
+==============================================+======+
| A. Introduction                              | 4    |
| B. Magnet Power Supply                       | 6    |
| C. Fuel Temperature Channels                 | 8    |
| D. NM1000 Wide Range Channel                 | 10   |
| E. Power Monitoring Channels                 | 13   |
|    - NP1000 Safety Channel                   | 13   |
|    - NPP1000 Safety Channel                  | 13   |
|    - NPP1000 Safety Channel (pulse circuits) | 16   |
+----------------------------------------------+------+

E. Attachments
~~~~~~~~~~~~~~
1. Magnet circuit and fuel temp - 1 page  
2. NM1000 wide range channel - 2 pages  
3. NP(P)1000 % safety channels - 2 pages

F. Equipment, Materials
~~~~~~~~~~~~~~~~~~~~~~~
1. ICS system keys  
2. Multi-meter - Fluke 87 or  
3. Multi-meter - Keithley 196  
4. Multi-source - Keithley 263  
5. Test instrument cables, probes  
6. Thermometer (approx. range: -10 to 110 °C)  
7. IC chip clip, jumpers for NP1000  
8. HV load test assembly for NM1000

G. References, Other Procedures
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
1. UT TRIGA Mechanical System Manual (Parts 1,2,3, and 4)  
2. UT TRIGA ICS Manual (Parts 1,2,3, and 4)  
3. Interlocks and SCRAM functions (MAIN-1)  
4. NM1000 Wide Range Channel (UT Installation)  
5. NPP1000 NP1000 Safety Channel (UT Installation)  
6. AIO16 Board Alignment (Keithley) (UT Installation)  
   DAS16 programs: INSTALL, QBCAL, QBCALF, QBCALG, QBCALGA

II. PROCEDURE
-------------

A. Introduction
~~~~~~~~~~~~~~~
Log all console operation for diagnostic work, maintenance, surveillance, calibration and test with the password MIRAGE.

1. Review calibration or functional check requirement.  
   Follow instructions of each of the following sections.  
   Refer to Maintenance Manuals if necessary for adjustments.

2. Discontinue operation if any procedure is not successful.  
   Correction of all failures is necessary to continue routine operation.

3. Run pre-start checks to verify operable conditions. Review surveillance results.  
   Approval of the data by the reactor supervisor is necessary to continue operation.

4. File procedure records and pre-start checklist. Initial and date calibration check tag.  
   Tag location should be on key ring with magnet key.

5. Return to normal operation.

Technical Specification references for the instrument systems are:

+---------+------------------+------------------------------------------+-----------------------------+
| Section | Steps            | Description                              | TS requirement              |
+=========+==================+==========================================+=============================+
| B       | 1-3              | Monitor magnet power supply levels        |                            |
|         |                  | Note: Test of trip operation not done here|                            |
|         | 4-5              | Monitor shorts of magnet power supply lines|                           |
|         | See MAIN1        | Calibration (analog adjustment and trip test) | 4.2.3 (3.2.3a-d)       |
|         | See MAIN1        | Calibration (no analog adj., circuit test only) | 4.2.3 (3.2.3d-f)     |
+---------+------------------+------------------------------------------+-----------------------------+
| C       | 1-5              | Electrical function of TC junction sensor |                            |
|         | 6-9              | Temperature calibration of monitor circuit| 4.2.4 (3.2.4a)             |
|         | 10               | Trip set-point calibration of monitor circuit | 4.2.3 (3.2.3a)         |
+---------+------------------+------------------------------------------+-----------------------------+
| D       | 1-3              | Verify configuration status and power supplies |                       |
|         | 4-6              | Test calibration of counter operating modes | 4.2.4 (3.2.4b)           |
|         | 5 (c)            | Test Hi% power level trip set points      | 4.2.3 (3.2.3b)             |
|         | 8-10             | Test HV power supply trip set points      | 4.2.3 (3.2.3c)             |
+---------+------------------+------------------------------------------+-----------------------------+
| E       | 4-5              | Calibrate power level circuit             | 4.2.4 (3.2.4b)             |
|         | 6-7              | Calibrate trip power level trips          | 4.2.3 (3.2.3b)             |
|         | 9                | Calibrate high voltage level trips        | 4.2.3 (3.2.3c)             |
|         | 12,14,15-17,20   | Calibrate pulse power peak                | 4.2.4 (3.2.4c)             |
|         | 13,14,18-19,20   | Calibrate pulse power integral            | 4.2.4 (3.2.4d)             |
+---------+------------------+------------------------------------------+-----------------------------+

B. Magnet Power Supply
~~~~~~~~~~~~~~~~~~~~~~
Refer to GA Operation and Maintenance Manual (E117-1004) for adjustments to the magnet supply circuits. See Volume 1, section 4, pages 38–41.

1. Locate magnet power supply (DAC shelf 1).

2. Connect voltmeter leads to the magnet power supply.

3. Monitor console annunciation for magnet supply lo or hi voltage.
   Configuration set points for magnet supply voltage are 18 and 23 volts.
   ICS System monitoring of the magnet supply voltage uses a 4 to 20 mA signal.

   a. Measure as found magnet voltage.

   b. Adjust source voltage for low voltage detection (18.0 volts).  
      Verify that the system detects low voltage. Record trip level.

   c. Adjust source voltage for high voltage detection (23.0 volts).  
      Verify that the system detects high voltage. Record trip level.

   d. If signal levels are not correct (step b or c), then  
      Check calibration of voltage to current conversion (4 to 20 mA module).

   e. Reset magnet supply voltage to 20.0 volts.  
      Verify that the circuit detects no magnet supply problems.

4. Test ground detection circuit.  
   Trip is set to detect a 10 kilo-ohm short to ground.  
   Check trip at Action Pak #16, LED will indicate status of trip.

   a. Short the positive terminal of the magnet power supply.  
      The short is to ground thru test potentiometer set to 9 kilo-ohms.  
      Verify console annunciation. If OK remove short, skip step 5.

   b. Short the negative terminal of the magnet power supply.  
      The short is to ground thru test potentiometer set to 9 kilo-ohms.  
      Verify console annunciation. If OK remove short.

5. Adjust short detection trip levels. Readjust test potentiometer to 10 kilo-ohms.  
   Apply shorts at magnet power supply terminals.

   a. Short positive terminal to ground thru test potentiometer.  
      Adjust Action Pack *span* potentiometer:  
      - first CCW until the Hi trip LED is OFF,  
      - then CW until the Hi trip LED is ON.  
      *Remove short.*

   b. Short negative terminal to ground thru test potentiometer  
      Adjust Action Pack *zero* potentiometer:  
      - first CW until the Lo trip LED is OFF,  
      - then CCW until the Lo trip LED is ON.  
      *Remove short.*

   c. Repeat steps a and b until no further adjustments are necessary.

   d. Repeat step 4 to verify console annunciations.

C. Fuel Temperature Circuits
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Refer to GA Operation and Maintenance Manual (E117–1004) for adjustments to the fuel temperature circuit.

1. Record pool water temperature. Use control console status window.

2. Mercury thermometers may not be used on the third level reactor platform.

3. Do steps 4–10 for each fuel temperature channel, #1 and #2.  
   Thermocouple is **type K**.

4. Disconnect thermocouple connections at calibration test relays.  
   FT#1 is relay **K3** (pins 11,14).  
   FT#2 is relay **K4** (pins 11,14).

5. Measure circuit resistance from relay thru the TC junction.  
   Use AC power ground (not neutral) for measurements relative to ground.

6. Connect DC voltage source to test relay pins 11(-) and 14(+).  
   (Do not reconnect TC inputs.)

7. Measure temperature at the module junction of Action Paks 7 and 8.  
   Determine reference voltage at Action Pak modules.  
   Find reference voltage, Vref, from **type K** thermocouple table.

8. Verify zero and full-scale indication.

   a. Set source input to simulate 0 °C (V = 0.0mV – Vref)  
      e.g., at 32 °C Vref is 1.285mV and V = –1.285mV.

   b. Verify continuous illumination of first LED of console bar graph.  
      Verify reactor console indicates 0 °C ± 2.

   c. Set source input to simulate 500 °C (V = 20.64mV – Vref).  
      Verify full scale indication (5th LED) on bar graph.  
      Verify reactor console indicates 500 °C ± 5.

9. Verify the control console status box.

   a. Adjust source to represent 495 °C (V = 20.427mV – Vref).  
      Verify FT display box is black.

   b. Adjust source to represent 505 °C (V = 20.853mV – Vref).  
      Verify FT display box is red.

10. Verify fuel temperature trip levels.

   a. Test module trip at 550 °C (V = 22.772mV – Vref).  
      Gradually change voltage to activate trip module.

   b. Observe voltage that causes Action Pack module scram trip (V).  
      Calculate module trip level voltage (Vtr).  
      Lookup the module trip temperature.  
      Verify module trip condition status.  
      Vtr = V + Vref. Trip should be 550 °C ± 5.  
      Record trip voltage and temperature.

11. Reconnect TC leads. Return circuit to operating condition.

12. Run pre-start checks.  
    Verify test signal value at bar graph meters switches between 527 °C and 555 °C.

   a. Abort pre-start checks at completion of fuel temperature check.  
   b. Compare display fuel temperatures (#1 and #2) to pool water temp.

D. NM1000 System Calibration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Refer to GA Operation and Maintenance Manual (E117–1000) for alignment of unit if adjustments are necessary.

Note: Some constants (*italics*) change at the time of a power calibration. Values shown are approximate.

1. Verify values of data constants in processor stacks.  
   To display data press "Fn x",  
   where "n" is the stack tens digit and "x" is the ones digit.

**Computed Values**

+--------------------+------------+
| 10 percent power   |            |
| 11 percent power   |            |
| 12 period          | 100        |
| 13 period          | 100        |
| 14 mode            |            |
| 15 relay status    |            |
+--------------------+------------+

**Single Detector**           | **Campbell Detector**
-----------------------------|------------------------------
20 DET counts                | 30 CMB Counts  
21 alpha offset: 0.00        | 31 noise offset: *–2.00E+02*  
                             | 33 Linear Factor: 3.70E–01  
25 DET pp const: 8.33E–8     | 35 CMB pp const: *4.20E–08*  
29 DET XOVR: 1.20E+6         | 39 CMB XOVR: 1.95E+03  

**Trip Set-points**

+------------------------+--------------------------+
| 40 Lo Level            | 2.00E–7                  |
| 41 Hi Level            | 1.08E+2                  |
| 42 Float               | 1.00E–1                  |
| 43 Rate                | 3.00E+0                  |
+------------------------+--------------------------+

**Operation Mode**

+------------------------+------------+
| 50 Operation Mode      | 0          |
| 51 Flt Trip Mode       | 1, Lo LVL  |
| 59 Version Number      | 4.05       |
+------------------------+------------+

2. Check power supply test points for nominal values.

+-------------------+-------------+-----------------------------+
| Designation       | Preamplifier Test | Microprocessor Test    |
+===================+=============+=============================+
| PS1 +15 volts     | +           | TB1-1 (test), TB1-4 (common)|
| PS2 –15 volts     | –           | TB1-8 (test), TB1-5 (common)|
| PS3 +5 volts      | +           | TB1-12 (test), TB1-10       |
| HVPS +800 volts   | HV Mon      | N/A                         |
+-------------------+-------------+-----------------------------+

3. Clear all alarms.  
   Press keys “F7 9 0 ENTER”.  
   Trips display at stack location 15 (F, L, H, R).  
   Keypad lamps A1 and A2 should be extinguished.

4. Test Count Rate mode as directed in steps a–d.  
   PA-15 discriminator is set for 0.1% (900 kilowatts) = 1.2 × 10⁶ cps.  
   Compare stack 20 to expected test cps and stack 10 to expected power in each test.

   (Test cps – alpha offset) × count rate power constant = % Power  
   where:
   - alpha offset: stack 21 = 0.0  
   - count rate power constant: stack 25 = 8.33E–08

**Mode Table**

+--------------+----------+----------------+----------+
| Mode         | Stack 50 | % Power Expect | Test cps |
+==============+==========+================+==========+
| Counter LO   | 1        | 1.00E–5        | 120      |
| Counter MID  | 2        | 8.00E–4        | 9600     |
| Counter HI   | 3        | 2.84E–2        | 341000   |
+--------------+----------+----------------+----------+

   a. Execute counter low test mode.  
      Press “F5 F8 1 ENTER”.

   b. Note status of low power level trip in stack location 15.  
      Press “F1 5”, letters F and L should display.

   c. Execute counter mid test.  
      Press “F5 F8 2 ENTER”.

   d. Execute counter high test.  
      Press “F5 F8 3 ENTER”.

5. Test Campbell mode as directed in steps a–c.  
   **Detector DC current is set for ~1.2 amps at 90% (900 kilowatts).**  
   Compare stack 30 to expected test cps and stack 10 to expected power in each test.

**Campbell Mode Table**

+--------------+----------+----------------+----------+
| Mode         | Stack 50 | % Power Expect | Test cps |
+==============+==========+================+==========+
| Campbell LO  | 4        | 5.32           | 18300    |
| Campbell HI  | 5        | 112.25         | 84800    |
+--------------+----------+----------------+----------+

   a. Execute Campbell low test.  
      Press “F5 F8 4 ENTER”.

   b. Execute Campbell high test.  
      Press “F5 F8 5 ENTER”.

   c. Note status of high power level trip in stack location 15.  
      Press “F1 5”, letters L and H should display.

6. Reset normal mode operation.  
   Press keys “F5 F8 0 ENTER”.

7. Wait 10 seconds, then clear all alarms.  
   Press keys “F7 9 0 ENTER”.

8. Connect digital multi-meter to high voltage test point:  
   HV Mon, of the High Voltage Power Supply  
   (HV = HV Mon Reading × 100)

9. Test under voltage trip and over voltage trip:

   a. Adjust HV ADJUST on power supply to 750 volts (7.50V at HV Mon).  
      - Trip indicated by A1 and A2 lamps on keypad display.  
      - Inspect stack location 60 (Press “F6 0 ENTER”).  
      - Press “F7 9 0 ENTER” to clear.

   b. Adjust HV ADJUST to 850 volts (8.50V at HV Mon).  
      - Repeat same checks as above.

10. Adjust HV ADJUST for nominal 800 volts (8.00 at HV Mon).

11. Clear all trips.  
    Press keys “F7 9 0 ENTER”.

E. NP(P)1000 Power Safety Channels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

4. Check zero calibration
^^^^^^^^^^^^^^^^^^^^^^^^^

a. Disconnect input signal to unit at J2.  
   Jumper U8 pins 8 & 9 (**NPP1000 unit only**).

b. Measure voltage at test point 63.  
   Value should be less than ±100 micro-volts (Adjust R131).

c. Measure voltage at test point 56.  
   Value should be less than ±100 milli-volts (Adjust R131).  
   NPP should be slightly negative, about –5 mV.

d. Press manual reset button to clear trip conditions if necessary.  
   Remove jumper at U8 pins 8 & 9 (**NPP1000 unit only**).

e. Measure voltage between test points 57(+) and 58(–).  
   Value should be 0.00 volts.  
   The sign of the voltage will depend on the lead placement (Adjust R120).  
   Verify CSC display and bar graph read 0%.

5. Check full-scale calibration
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

a. Apply current source at input connector J2.  
   - NP1000: 8.33E–4 amps (1.00E–03 amp = 120%; 10 volts)  
   - NPP1000: 5.00E–7 amps (6.00E–07 amp = 120%; 10 volts)

b. Measure voltage at test point 63 and point 56.  
   Value should be 8.33 ± 0.05 volts DC  
   - **NP**: Adjust **R23 only**  
   - **NPP**: Adjust **R27 only**  
     (Pulse Mode: Use R23 for pulse mode. See step 15.)

c. Measure voltage between test points 57(+) and 58(–).  
   Value should be 8.33 ± 0.05 volts  
   The sign of the voltage will depend on the lead placement (Adjust R123).  
   Verify CSC display and bar graph read 100%.

d. Remove current source.
   Repeat steps 4 and 5 if adjustments are necessary, if not proceed to step 6.

6. Check trip calibrations
^^^^^^^^^^^^^^^^^^^^^^^^^^^

a. Apply current at input connector J2.  
   Calibration current is 9.0E–4 amps (5.5E–7 NPP).

b. Verify percent power (NV) trip LED illuminates.

c. Decrease input current at J2.  
   Calibration current is 8.5E–4 amps (5.0E–7 NPP).

d. Verify trip LED extinguishes.

7. Check trip set-point calibration
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

a. Connect voltmeter to TP56. Increase current at J2.

b. Record channel trip current and voltage found at TP56.

c. Trip should be at 8.75E–4 amps (5.25E–7 NPP). (Adjust R79)

8. Depress test switch S2. Measure voltage at test point 56.  
   Value should be 9.09 ± 0.05 volts DC (Adjust R196).  
   Verify both HV and NV LEDs illuminate.

9. Set HV Test Module resistance to 1.1 mega-ohm  
   (100 kilo-ohm 1/2 watt resistor in series with 1 mega-ohm potentiometer).  
   Connect Test Module at J1. Connect voltmeter at J1.

a. Adjust Test Module potentiometer to about 600 volts DC.  
   Verify HV trip LED illuminates (Adjust R96).

b. Disconnect J1. Remove Test Module.  
   Reconnect voltmeter to J1 and verify 750 ±10 volts DC (Adjust R6).  
   Depress reset switch. Verify HV trip LED extinguishes.

10. Apply 12 volts DC at test points 22 (Hi) and 23 (Lo).

a. Measure ramp rate between 7 and 8 volts at test point 64.

b. Rate should be 5 ± 1 seconds per volt (Adjust R10).

11. Reconnect detector signal and return unit to operating condition.  
    Continue to next step for the **NPP1000**. **Stop here for NP1000**.

Continue for **NPP1000 only**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

12. Zero alignment, NV
^^^^^^^^^^^^^^^^^^^^^^

a. Jumper U8 pins 8 and 9.  
   Jumper AR8 pin 2 to AR8 pin 6.  
   Clip test point 56 to ground.

b. Measure voltage 0 ± 0.05V at AR8 pin 6.  
   Use test point 10 as reference ground.  
   Adjust R134 for minimum zero offset.

c. Measure voltage 0 ± 0.05V at test point 59.  
   Use test point 10 as reference ground.  
   Adjust R138 for minimum zero offset.

d. *Remove jumpers in step 12a.*

13. Zero alignment, NVT
^^^^^^^^^^^^^^^^^^^^^^^

a. Jumper U7 pin 1 to ground.  
   Short capacitor C30 with a clip lead.

b. Measure voltage 0 ± 0.02V at test point 38.  
   Use test point 10 as reference ground.  
   Adjust R47 for minimum offset.

c. *Remove jumper(s) in step 13a.*

14. *Close switch S4-4.*  
    Calibrate circuit full-scale, NV and NVT.

15. Calibrate peak power NV circuit
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

a. Apply 1.0E–3 amps at input connector J2.

b. Verify 10.00 ± 0.05 volts at test point 56 (Adjust R23).

c. Verify 10.00 ± 0.05 volts at test point 59 (no adjustment).

*Note: Operation of the RESET button with a one mA input current will not discharge C58 completely. The result is an incorrect voltage at test point TP59.*

16. Calibrate full-scale peak power, NV signal output
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

a. Remove connector at J4 if not already removed.

b. Connect milliamp meter between TP60 (J4-22) and TP61 (J4-23).

c. Set J2 input signal to 1.0E–3 amps.

d. Remove input signal at J2.

e. Depress reset switch.  
   Verify 4 milliamp output (Adjust R140).

f. Depress reset switch again, then

g. Connect input signal at J2.  
   Verify 20 milliamps output (Adjust R143).

h. Repeat steps d thru g until no adjustment is necessary.

17. Check full-scale peak power, NV drift
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

a. Apply 1.0E–8 amps at input connector J2.

b. Observe the drift rate between TP60 and TP61.  
   Verify rate does not exceed 0.1 volt per minute.

c. Observe test point 38. Depress reset.  
   Drift rate should be less than 100 mV/min.

18. Check full-scale integral power, NVT circuit
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

a. Increase input to 1.0E–6 amp and depress reset switch.

b. Verify ramp rate at TP38 should be 15 sec per volt (Adjust R42).

19. Check full-scale integral power, NVT signal output
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

a. Remove connector at J4, if not already removed.

b. Connect milliamp meter between TP39 (J4-16) and TP40 (J4-17).

c. Set J2 input signal to 1.0E–6 amps.

d. Remove input signal at J2.

e. Depress reset switch.  
   Verify 0.00 ± 0.02 volts at TP38.  
   Verify 4 milliamp output (Adjust R51).

f. Depress reset switch again then,

g. Connect input signal at J2.  
   Apply test signal until 1.0 volt DC is at test point 38.  
   Verify 20 milliamps output (Adjust R54).

h. Repeat steps d thru f until no adjustment is necessary.

20. *Open switch S4-4*.  
    Replace connector at J4.  
    Reconnect detector signal and return unit to operating condition.

MAIN-3 Support System Features
==============================

I. INTRODUCTION
---------------

A. Purpose
~~~~~~~~~~
The purpose of this procedure is the calibration and functional check of the instrument control and safety system for the TRIGA reactor. Systems subject to this procedure are the pool water systems that provide moderator, cooling and shielding for the reactor core.

Three functional criteria for the procedure are:
  (1) Verify the conditions of the ICS system meet the minimum requirements  
      of the License Tech. Specs.
  (2) Verify the conditions of the ICS system meet the broader quality assurance  
      requirements of the ICS system design.
  (3) Assure no task or action of this procedure is a proposed change, test,  
      or experiment in the sense of 10CFR50.59.

B. Description
~~~~~~~~~~~~~~
The instrument control and safety system is a digital processing system that monitors analog and digital signals, displays information for the operator and logs data. Operator interactions with the system determine control of operation modes and rod positions. Safety system function is independent of the ICS system programs. This procedure provides instructions for the calibration, check and test of support systems that monitor reactor water systems. Water systems include the bulk pool water level, bulk pool temperature, water conductivity, coolant water system temperatures at the heat exchanger inlet and outlet, flow rates in the primary and secondary heat exchanger and pressure differentials between the heat exchanger tubes and shell.

C. Schedule
~~~~~~~~~~~
Schedule procedure once each year, prior to the completion of MAIN1. Plan procedure task for the month of July but no later than 15 months from previous work. The requirement to complete MAIN3 prior to MAIN1 will limit the no later than 15 months to no later than 7.5 months. SURV2 should be complete prior to implementing this procedure.

D. Contents
~~~~~~~~~~~

+-------------------------------+------+
| SECTION                       | Page |
+===============================+======+
| A. Introduction               | 4    |
| B. Pool Level                 | 4    |
| C. Pool Temperature           | 5    |
| D. Water Conductivity         | 6    |
| E. Primary Flow Rate          | 7    |
| F. Secondary Flow Rate        | 9    |
| G. Heat Exchanger Pressure    | 10   |
+-------------------------------+------+

E. Attachments
~~~~~~~~~~~~~~
1. Pool parameters - 1 page  
2. Coolant flow rates - 1 page  
3. Heat exchanger - 1 page

F. Equipment, Materials
~~~~~~~~~~~~~~~~~~~~~~~
1. ICS system keys  
2. Multi-meter – Fluke 87 or  
3. Multi-meter – Keithley 196  
4. Multi-source – Keithley 263  
5. Test instrument cables, probes, test resistors  
6. Flexible plastic tubing and fittings  
7. De-ionized water  
8. KCl reference solution

G. References, Other Procedures
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
1. UT TRIGA Mechanical System Manual (Parts 1,2,3, and 4)  
2. UT TRIGA ICS Manual (Parts 1,2,3, and 4)  
3. Interlocks and SCRAM functions – MAIN-1  
4. Pool Water System Surveillance – SURV-4

II. PROCEDURE
-------------

A. Introduction
~~~~~~~~~~~~~~~
Log all console operation for diagnostic work, maintenance, surveillance, calibration and test with the password MIRAGE.

1. Review calibration and functional check requirements.  
   Follow the instructions of each of the following sections.

2. Discontinue operation if any procedure is not successful.  
   Correction of all failures is necessary to continue routine operation.

3. Run pre-start checks to verify operable conditions. Review surveillance results.  
   Approval of the data by the reactor supervisor is necessary to continue operation.

4. File procedure records and pre-start checklist. Initial & date calibration check tag.  
   Tag location should be on key ring with the magnet key.

5. Return to normal operation.

Technical Specification references for the support systems are:

+---------+--------+-------------------------------+---------------------+
| Section | Steps  | Description                   | TS requirement      |
+=========+========+===============================+=====================+
| B       | 1–4    | Pool Water Depth              | 4.3.1b (3.3.1b)     |
| C       | 1–8    | Pool Temperature              | 4.3.1a (3.3.1a)     |
| D       | 2–4    | Water Conductivity            | 4.3.1c (3.3.1c)     |
| G       | 1–8    | Heat Exchanger Delta Pressure | 4.3.1d (3.3.1d)     |
+---------+--------+-------------------------------+---------------------+

B. Pool Water Level
~~~~~~~~~~~~~~~~~~~

1. Verify position of pool level indicator (scale).  
   Scale elevation (25.3 cm) is set at the tank equipment-mounting ring.

2. Lift up *high-level* sensor float.  
   Verify float level and hi/lo alarm indication.

3. Press down *low-level* sensor float.  
   Verify float level and hi/lo alarm indication.

4. Depress each SCRAM float switch one at a time to *alarm-level*.  
   Verify float level and verify pool level SCRAM trip indication at CSC.

C. Pool Water Temperature
~~~~~~~~~~~~~~~~~~~~~~~~~

1. Remove pool bulk temperature sensor.

2. Prepare ice water bath at 0 °C;  
   Prepare hot water bath at 100 °C with hot plate heater.

3. **CAUTION:** Do not use a mercury thermometer in the pool area.  
   Do not take thermometer on third level platform.  
   a. Measure calibration temperatures with thermometer.  
   b. Place the RTD sensor in each water bath.  
   c. Record test water temperature, and console indication.

4. Check the alarm set point by heating a solution of water.  
   Monitor water temperature and record alarm point.

5. If console indications agree with both temperatures ±4 °C, go to step 8.

6. Disconnect wire at pin 7 or 8 of AP5.  
   Connect ammeter to wire and AP5 (pin 7 to DMM+; pin 8 to DMM–).  
   a. Place temperature sensor (RTD) in ice bath,  
      Measure current; adjust zero control on AP5 to 4 mA, (0 °C).  
   b. Place temperature sensor (RTD) in hot bath,  
      Measure current; adjust span control on AP5 to 20 mA, (100 °C).  
   c. Repeat steps a and b until no further adjustments are necessary.

7. Repeat steps 3 thru 5 if zero and/or span adjustments were required.

8. Replace temperature sensor and reconnect all signal lines.  
   Record bulk pool temperature displayed on console.

D. Pool Water Conductivity
~~~~~~~~~~~~~~~~~~~~~~~~~~
(*Cell type: Titanium, cell constant is 0.1*)

1. Perform an electronic calibration with resistors. Two points (+0.5%):  
   - 13.33 kΩ → 7.5 mmho/cm → 0.133 mega-ohms/cm  
   - 00.10 M  → 1.0 mmho/cm → 1.000 mega-ohms/cm

2. Toggle display inputs with selector switch.  
   Local monitor panel connects to cell shown by selector indication.  
   Remote monitor (DAC-CSC) connects to other cell in the water system.

3. Remove selector switch cover assembly.  
   Locate cell #2 tie bar on the conductivity selector switch.  
   Remove the 3 sensor wires at tie bar. Verify wire label for later replacement.  
   Connect an 18 kΩ (±0.5%) resistor between terminals 2 & 3 (*Temp. compensation*).  
   a. Check for 1.0 micro-mho/cm,  
      Install 0.1 mega-ohm resistor between terminals 2 and 4.  
      Rotate set point dial to steady red-green LED condition.  
      Record local and console indications.  
   b. Check for 7.5 micro-mho/cm,  
      Install 13.33 kilo-ohm resistor between terminals 2 and 4.  
      Rotate set point dial to steady red-green LED condition.  
      Record local and console indications.  
   c. If reading is not correct, verify resistances,  
      Then loosen setscrews of indicator dial and reposition dial.  
   d. Return circuit connections to original condition.

4. Prepare solution of high purity de-ionized water and KCl.  
   Place 7.465 mg of KCl in 1.0 liters of de-ionized water.  
   0.0001 molar = 15 micro-mho/cm (equal to 6.67 kilo-ohms/cm)

5. Align purification skid valves to remove conductivity cells.  
   Turn off pump, close flow throttle, skid isolation, and resin tank isolation valves.

6. Remove each cell and replace with a PVC plug to prevent water drainage.  
   a. Clean any deposits from cell with tissue paper.  
   b. Rinse conductivity cell with distilled water.  
   c. Immerse sensitive part of cell in each test solution.  
   d. Dip each cell in de-ionized water for 1.0 micro-mho/cm.  
   e. Dip each cell in KCl solution for 15.0 micro-mho/cm.  
   f. If improper readings occur replace sensor and re-test.

7. Replace cells, reconnect wiring, and check for leaks.

E. Primary Flow Rate (Reactor Pool Water)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Compare no flow conditions at local gauge and console.

2. Align valves for maximum flow and start primary flow pump.

3. Compare console flow rate with local gauge indication.

4. Verify flow rates are within 10%.  
   If flow rates are within 10% skip steps 5 thru 8.  
   Return the system to the normal operating condition.

5. Local Flow Gauge Calibration (NO action necessary).  
   Flow transmitter calibration includes local and remote meters.

6. Flow Transmitter Calibration (Setup Taylor transmitter).  
   The primary flow transmitter performs a flow square root extraction.  
   a. Close both valves on flow sensor lines (at *Annubar* flow sensor).  
   b. Locate vent plugs (lo & hi) from the transmitter diaphragm chamber.  
   c. Remove front and rear covers from transmitter.  
   d. Connect ammeter in series with the flow sensor transmitter.  
      Remove the wire at the transmitter – terminal.  
      Connect ammeter + to – transmitter terminal.  
      Connect ammeter – to the loose transmitter wire.  
   e. The DAC does not process the primary flow signal.  
      A jumper module is present at DAC shelf location 1.  
      The jumper module replaces an Action Pak process module.

7. Flow Transmitter Calibration (set zero)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

a. Open cross valve on transmitter.

b. Loosen vent plug on both low and high side of transmitter.  
   Verify the system is solid water; contains no air.  
   Add water until water leaks from the vent.  
   Leave both transmitter vent plugs open.

c. Verify zero indication on local meter.  
   Verify 4 mA output at flow transmitter.  
   Verify zero at the console status display.  
   Use zero set for adjustment of **4 mA** signal.

d. Close cross valve on transmitter.

8. Flow Transmitter Calibration (set full scale)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

a. Connect fitting and tygon tube to high side transmitter vent.  
   Fill tube with water to a level **29.7" (75.4 cm)**.  
   Measure water level above the low-side vent port.  
   The water level correlates to **360 GPM (22.7 lps).**

b. Verify the low-side transmitter vent port is full of water;  
   Momentarily open the cross valve until water leaks.  
   Do not close vent at this time.

c. Readjust the high-side level to **29.7 inches**, if necessary.

d. Verify local meter 100% reading,  
   Verify transmitter output signal is **20 mA**,  
   Verify **22.7 lps** at the console display.  
   Use span set for adjustment of **20 mA** signal.

e. If either zero or span adjustments were required,  
   Remove tygon tube from high side vent port.  
   Repeat steps 7 and 8 until no further adjustments are necessary.

9. Return system to original configuration.

F. Secondary Flow Rate (Physical Plant Cooling Water)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Compare no flow conditions at local gauge and console.

2. Align valves for maximum flow and start secondary flow pump.

3. Compare console flow rate with local gauge indication.

4. Verify flow rates are within 10%.  
   If flow rates are within 10%, skip steps 5 thru 8.  
   Return the system to the normal operating condition.

5. Local Flow Gauge Calibration  
   a. Close high and low isolation valves below gauge.  
   b. Open cross connect valve, gauge should read 0.  
   c. Close cross connect.  
   d. Open both high and low pressure vents.  
   e. Connect tygon tube to high-pressure vent.  
   f. Verify low side vent filled with water.  If not, momentarily open isolation valve.  
   g. Fill tygon tube with water to a level of **110"**. Measure level from the top of low side vent. Verify gauge reads **600 gpm**.  
   h. Return system to condition prior to calibration.

6. Flow Transmitter Calibration (Setup Foxboro transmitter)  
   Includes signal square root extraction.  
   a. Close both valves on sense lines to transmitter *(at Foxboro transmitter).*  
   b. Locate vent plugs (lo & hi) from the top of the diaphragm chamber.  
   c. Loosen the lock nut and rotate transmitter head.  
      Remove both transmitter covers.  
   d. Connect ammeter in series with the flow sensor transmitter. 
      Remove the wire at the transmitter – terminal.  
      Connect ammeter + to – transmitter terminal.  
      Connect ammeter – to the loose transmitter wire.  
   e. The DAC processes the secondary flow signal.  
      - A process module is present at DAC shelf location 2.  
      - Flow process module is an Action Pak #4440(-108).  
      - The process module is a flow square root extractor.  
        Connect ammeter in series with the flow square root extractor.  
        Remove signal line to pin 7 (–) and check the input to the wire.  
        *(Output: 1–15V is present on signal line.)*

7. Flow Transmitter Calibration (set zero)
  a. Open cross valve on transmitter.
  b. Loosen vent plug on both low and high side of transmitter.  
    Verify the system is solid water; contains no air.  
    Add water until water leaks from the vent.  
    Leave both transmitter vent plugs open.
  c. Verify zero indication on local meter.  
    Verify 4 mA output at flow transmitter.  
    Verify 4 mA output at square-root extractor.  
    Verify zero at the console status display.  
    Use zero set for adjustment of **4 mA** signal.  
    Set output of transmitter first, then set output of root extractor.
  d. Close cross valve on transmitter.

8. Flow Transmitter Calibration (set full scale)
  a. Connect fitting and tygon tube to high side transmitter port.  
    Fill tube with water to a level **110" (279.4 cm)**.  
    Measure water level above the low-side vent port.  
    The water level correlates to **600 gpm (37.8 lps).**
  b. Verify the low-side transmitter vent port is full of water.  
    Momentarily open the cross valve until water leaks.  
    Do not close vent at this time.
  c. Readjust high side level to **110 inches**, if necessary.
  d. Verify transmitter and root extractor signal outputs,  
    Verify both signal outputs are **20 mA**,  
    Verify **37.8 lps** at the console display.  
    Use span set for adjustment of **20 mA** signal.  
    Set output of transmitter first, then set output of root extractor.
  e. If either span or zero adjustments were necessary,  
    Remove tygon tube from the high side vent port.  
    Repeat steps 7 and 8 until no further adjustments are necessary.

9. Return system to original configuration.

G. Heat Exchanger Differential Pressure and Capsi-photochellic Calibration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Close two 1/4-inch stainless steel valves on lines to the sensor.

2. Remove both plugs on top of the sensor.

3. Open the two valves to fill each port to the same level then close them.  
   **Caution** – Flow snubbers in flow lines slow response.  
   It may be necessary to start the primary or secondary coolant system.

4. Verify zero reading on meter.  
   Use zero set on meter face for adjustment:  
   0-inch H₂O = 0 psi: Photochellic gauge = 0 psi.

5. Connect tygon tube to high port (right) with low port (left) condition unchanged.

6. Apply column of water equivalent to approximately 5 psi.

+------+---------+--------+
| psi  | in H₂O  | cm H₂O |
+======+=========+========+
| 1    | 27.68   | 70.3   |
| 2    | 55.36   | 140.6  |
| 5    | 138.4   | 351.5  |
+------+---------+--------+

a. Verify the meter reads 5 psi.  
b. Rotate low (LO) set-point to a level 0.5 psi above indicated reading.  
   Verify ΔP alarm status at CSC.  
c. Rotate low (LO) set-point to a level 0.5 psi below indicated reading.  
   Verify ΔP ok status at CSC.

7. Reset LO set-point to 5 psi.  
   Reset HI set-point to 10 psi.  
   *(TS Limit is 7 kPa or 1 psi)*

8. Return system to original configuration.

H. Heat Exchanger Temperature Sensors
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Compare heat-exchanger inlet temperatures.  
   a. Observe inlet temperature at local gauge.  
   b. Observe inlet temperature at CSC console.

2. Compare heat-exchanger outlet temperatures.  
   a. Observe outlet temperature at local gauge.  
   b. Observe outlet temperature at CSC console.

3. If each temperature in steps 1 and 2 is within ±4 °C skip step 4.

4. Calibrate temperature circuit following procedure for bulk pool sensor.  
   *(See section IIC, page 5 of this procedure).*

MAIN-4 Area Radiation Monitor Systems
=====================================

I. INTRODUCTION
---------------

A. Purpose

This procedure describes the operation, maintenance and calibration requirements for the installed radiation monitors that consist of:
- Area Radiation Monitors
- Particulate CAM
- Gas CAM

Three functional criteria for the procedure are:
1. Verify the condition of the radiation monitoring system meet the minimum requirements of the License Technical Specifications.
2. Verify the condition of the radiation monitoring system meet the broader quality assurance requirements of the system design.
3. Assure NO task or action of this procedure is a proposed change, test, or experiment in the sense of 10CFR50.59

B. Description

The radiation monitor system is strategically positioned in the reactor facility. It provides a constant indication of radiation levels in the area, both locally and remote in the control room. Alarm functions can be set for each unit; the alarms sounds locally and in the control room.

The Particulate CAM operates continuously to sample the air in the reactor room. Air is drawn through a filter paper where radioactive particles are trapped and counted. Dual alarm set points provide visual and audible alarms.

The Gas CAM provides monitoring of the air being exhausted from the top of the reactor pool during reactor operations. It is designed primarily for detection of the noble gas portion. Alert and alarm set points provide indication of abnormal conditions.

C. Schedule

Schedule procedure twice each year, at six month intervals for those monitors that are required by Technical Specifications and annually for additional monitors.

D. Contents

A. Normal Operations  
    1. Radiation Monitors  
    2. Particulate CAM  
    3. Gas CAM  

B. Response Checks  
    1. Radiation Monitors  
    2. Particulate CAM  
    3. Gas CAM  

C. Particulate Filter Replacement  
    1. Particulate CAM  
    2. Gas CAM  

D. Calibration Requirements  

E. Attachments *(not part of this procedure but may be useful)*  
    1. Weekly/Monthly – Page 1  
    2. Gas CAM Annual – Page 2  
    3. Particulate CAM Annual – Page 3  

F. Equipment, Materials  
    1. Appropriate calibration sources  
    2. Appropriate filter papers  

G. References, Other Procedures  
    1. ANSI N323  
    2. Radiation Monitor Manual  
    3. Particulate CAM Manual  
    4. Gas CAM Manual  
    5. OPER-6 Reactor Bay Systems

II. PROCEDURE
-------------

A. Normal Operations

1. Radiation Monitoring System

- The Radiation Monitor System operates continuously and requires no operator actions.
- System server display in control room should provide system status for each monitor.

2. Particulate CAM System

- The Beta Monitor operates continuously and requires no operator actions.

  a. Check main Power switch is ON.  
  b. Check air pump switch is ON.  
  c. Check AUDIO switch is ON.  
  d. Check that a filter is in place.  
     - Filters are typically replaced weekly, or as necessary for special conditions.  
  e. Check that the MON light is on at least 50% of the time.  
     - Backgrounds of 30 cpm should keep the monitor light on 90% of the time.  

3. Gas CAM System

- The Gas Monitor System primarily operates continuously and should be verified operating prior to daily reactor operations.

  a. Ensure system lineup is per manufacturer manual.

B. Response Checks

1. Radiation Monitor System (weekly)

- Verify that system is operating correctly by verifying status for each detector that is on line.  
- Ensure minimum required per Technical Specifications are met.

2. Particulate CAM System (weekly)

a. Remove the filter assembly.  
b. Replace the filter medium.  
c. Place the check source flush with the filter assembly opening.  
d. Observe instrument and remote CSC display indicate ~4000 cpm.  
e. Replace the filter assembly; check for normal airflow ~65 lpm.  
f. Check pump exhaust filter.

3. Gas CAM System (weekly)

a. Replace air filter per manufacturer’s procedure.

C. Particulate Filter Replacement

**Note:** These filter replacement procedures shall not be used if the filter replacement is due to an alert or alarm. Refer to OPER-5.

1. Particulate CAM

a. Turn the pump switch to OFF.  
b. Lift the filter holder catch knob. Pull the holder out of the sampling chamber.  
c. Remove the filter hold-down cap and pull the filter paper off.  
d. Install new filter paper (fine side facing toward detector) and replace the hold-down cap.  
e. Lift the holder catch knob and insert the filter holder. Ensure catch drops behind holder.  
f. Restart airflow pump and ensure proper flow rate.

2. Gas CAM System

a. Follow procedure posted on equipment or in manufacturer manual.

D. Calibration Requirements

1. The instruments covered by this procedure shall be calibrated per Technical Specification requirements.  
2. The calibration will be conducted per equipment’s operation manual.

MAIN-5 Fuel Inspection and Measurement
======================================

INTRODUCTION
------------

A. Purpose  
The purpose of this procedure is to monitor for physical changes to the fuel elements. The main functional criterion for this procedure is to verify that the physical condition of fuel elements meets the minimum requirements of the License Docket 50-602 Technical Specifications.

B. Description  
Physical changes of a fuel element indicate the possible occurrence of stress on the cladding. A change in fuel phase with different temperatures, thermal expansion, or fracture of individual fuel pieces can occur to a varying degree depending on the fuel element operating history. A significant change in element length could indicate fuel element components expanding enough to fill the fission product gas gap placing stress on the end fitting welds. Cladding damage may allow the escape of fission products. The most common fuel element problem is localized swelling that may cause a bend of the fuel element such that the element will not fit through the reactor grid plate holes or be difficult to remove from the core.

C. Schedule  
Schedule completion of each procedure section at two-year intervals.

D. Contents  
PROCEDURE SECTION II.  
  A. Inspect and Measure Standard Fuel Element (SFE) .......... 4  
  B. Inspect and Measure Instrumented Fuel Element (IFE) ...... 6  
  C. Inspect Control Rod and Fuel Followed Control Rod (FFCR) and Measure FFCR element .......... 7

E. Attachments  
  1. Fuel Inspection Summary  
  2. Fuel Element Log  
  .. note:: Attachments are not part of this procedure but may be useful when performing this procedure.

F. Equipment, Materials  
  1. Fuel Inspection Stand  
  2. Reference Standard Fuel Element (SFE)  
  3. Reference Fuel Follower Control Rod (FFCR) Length Tube  
  4. Measurement Extension Rod  
  5. Probe Indicator (travel of 0" to 1" in increments 0.001" is typical)  
  6. Underwater Video Camera System  
  7. Fuel Handling Tool

G. References, Other Procedures  
  1. Docket 50-602 Technical Specifications  
  2. Emergency Response Plan and Procedure PLAN-E  
  3. Previous MAIN-5 Records  
     a. Fuel Inspection Summary  
     b. Fuel Element Log  
  4. FUEL-1 Movement of Fuel Procedure  
  5. Fuel Movement Log records  
  6. B159.xls File  
  7. SURV-1 Fuel Temperature Calibration  
  8. SURV-3 Excess Reactivity and Shutdown Margin  
  9. SURV-6 Control Rod Calibration  

PROCEDURE
---------

A. Inspect and Measure Standard Fuel Elements

.. caution:: Detectable amounts of particulate activity are associated with any abrasive contact with irradiated fuel elements. The fuel element handling tool and element measuring devices will have small amounts of removable radioactive particles.

.. note:: Inspection and measurement shall apply to all elements in the reactor core grid plate, but two to six spare SFEs should also be evaluated for future use.

MAIN-6 Rod & Drive Maintenance, Inspection
==========================================
