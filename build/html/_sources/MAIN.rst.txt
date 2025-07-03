====
MAIN
====

MAIN-1 Interlocks and Scram Features
====================================

INTRODUCTION
------------

A. Purpose
~~~~~~~~~~

This procedure is the calibration and functional check of the instrument, control and safety (ICS) system for the TRIGA reactor. Systems subject to this procedure are the the control console programs, the operation control interlocks, and the control rod safety system.

.. line-block::
   Three functional criteria for the procedure are:
   1. Verify the conditions of the ICS system to meet the minimum requirements of the License Technical Specifications.
   2. Verify the condition of the ICS system meets the broader quality assurance requirements of the ICS system design.
   3. Assure **NO** task or action of this procedure is a proposed change, test, or experiment in the sense of 10CFR50.59

B. Description
~~~~~~~~~~~~~~

   The instrument control and safety system is a digital processing system that monitors analog and digital signals, displays information for the operator, and logs data. Operators interact with the system to determine control of operation modes and rod positions. The safety system function is independent of the ICS system programs. This procedure systematically examines key program features that determine ICS system interlocks and that implement ICS system SCRAM functions.

C. Schedule
~~~~~~~~~~~

   Schedule procedure twice each year, at six month intervals not to exceed 7.5 months from previous completion of check.

D. Contents
~~~~~~~~~~~

   .. line-block::
      :ref:`A. Introduction <MAIN-1.II.A>`
      :ref:`B. Interlock Checks <MAIN-1.II.B>`
      :ref:`C. SCRAM Functions <MAIN-1.II.C>`
      :ref:`D. Instructions <MAIN-1.II.D>`
         :ref:`1.0 Operator Log on:off <MAIN-1.II.1.0>`
         :ref:`2.0 Manual Mode <MAIN-1.II.2.0>`
         :ref:`2.1 Entering Manual Mode <MAIN-1.II.2.1>`
         :ref:`2.2 Exiting Manual Mode <MAIN-1.II.2.2>`
         :ref:`2.3 Initiation and Termination <MAIN-1.II.2.3>`
         :ref:`2.4 Operation in Manual <MAIN-1.II.2.4>`
         :ref:`3.0 Auto Mode <MAIN-1.II.3.0>`
         :ref:`3.1 Entering Auto Mode <MAIN-1.II.3.1>`
         :ref:`3.2 Exiting Auto Mode <MAIN-1.II.3.2>`
         :ref:`3.3 Initiation and Termination <MAIN-1.II.3.3>`
         :ref:`3.4 Operation in Auto Mode <MAIN-1.II.3.4>`
         :ref:`4.0 Pulse Mode <MAIN-1.II.4.0>`
         :ref:`4.1 Initiating Pulse Mode <MAIN-1.II.4.1>`
         :ref:`5.0 Square Mode <MAIN-1.II.5.0>`
         :ref:`5.1 Initiating Square Mode <MAIN-1.II.5.1>`
         SCRAM Functions
         :ref:`6.0 Redundant Network <MAIN-1.II.6.0>`
         :ref:`7.0 SCRAM Mode <MAIN-1.II.7.0>`
         :ref:`7.1 CSC Program Logic <MAIN-1.II.7.1>`
         :ref:`7.2 DAC Program Logic <MAIN-1.II.7.2>`
         :ref:`7.3 NM1000 Program Logic <MAIN-1.II.7.3>`
         :ref:`7.4 Pulse Mode Features <MAIN-1.II.7.4>`

E. Attachments
~~~~~~~~~~~~~~

.. note:: 
   Attachments are not part of this procedure but may be useful when performing this procedure.

   1. ICS Interlocks
   2. ICS SCRAMS
   3. Acceptance

F. Equipment, Materials
~~~~~~~~~~~~~~~~~~~~~~~

   1. ICS system keys  
   2. Multi-meter Fluke 87 or equivalent device  
   3. Multi-source Keithley 263 or equivalent device  
   4. Test instrument cables and probes  

G. References, Other Procedures
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   1. ANSI N323  
   2. Radiation Monitor Manual  
   3. Particulate CAM Manual  
   4. Gas CAM Manual  
   5. OPER-6 Reactor Bay Systems  


PROCEDURE
---------

.. _MAIN-1.II.A:

A. Introduction
~~~~~~~~~~~~~~~

   **Log all console operations for diagnostic work, maintenance, surveillance, calibration and test with the password** `MIRAGE`.

      1. Review calibration and functional check requirements. Follow the instructions of each section.  
      2. Discontinue operation if any procedure is not successful.  
      3. Run pre-startup checks to verify operable conditions. Approval by reactor supervisor required.  
      4. File procedure records and pre-start checklist.  
      5. Return to normal operation.

   Two types of annunciation conditions may occur. One condition presents an audible alarm and the other does not. The first condition is a detection of a failure. The second condition is a warning of a system problem.

.. _MAIN-1.II.B:

B. Interlock Check Conditions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   **This section of the OCS system procedures tests interlocks. The function of each of these interlocks is a function of the digital control program.**

   D.1 Prerequisite Conditions:

   +---------+-------+-----------------------------------------------------------------------------+-------------+
   | Section | Steps | Description                                                                 | Tech Spec   |
   +=========+=======+=============================================================================+=============+
   | 1.0     | 2-7   | A correct password is a requirement for opereation of the magnet key switch |             |
   +---------+-------+-----------------------------------------------------------------------------+-------------+
   | 1.0     | 8-10  | Log **ON** allows replacement of active operator.                           |             |
   +---------+-------+-----------------------------------------------------------------------------+-------------+
   | 1.0     | 11-16 | Log **OFF** requires system to be in the SCRAM mode.                        |             |
   +---------+-------+-----------------------------------------------------------------------------+-------------+

   D.2 Manual Mode Conditions:

   +----------+----------+------------------------------------------------------------------------------------+----------------+
   | Section  | Steps    | Description                                                                        | Tech Spec      |
   +==========+==========+====================================================================================+================+
   | 2.3      | 2-5      | Change from scram to manual mode requires operator log on.                         |                |
   +----------+----------+------------------------------------------------------------------------------------+----------------+
   | 2.3      | 6-9      | Acknowledge of scram condition is necessary to restore magnet key switch action    |                |
   |          |          | and enter manual mode.                                                             |                |
   +----------+----------+------------------------------------------------------------------------------------+----------------+
   | 2.4      | 10-13,   | Simultaneous withdrawal limits up motion to one rod and allows down motion of      | 4.2.2          |
   |          | 15       | any combination.                                                                   | (3.2.2b)       |
   +----------+----------+------------------------------------------------------------------------------------+----------------+
   | 2.4      | 14       | Release of rod by magnet or air switch will momentarily interrupt power to         |                |
   |          |          | each control rod unit.                                                             |                |
   +----------+----------+------------------------------------------------------------------------------------+----------------+
   | 2.4      | 16-18    | Transient rod function as a normal rod.                                            | 4.2.2          |
   |          |          |                                                                                    | (3.2.2b)       |
   +----------+----------+------------------------------------------------------------------------------------+----------------+
   | 2.4      | 19       | "Fire" button for transient rod applies air to drive only if drive is down.        | 4.2.2          |
   |          |          |                                                                                    | (3.2.2b)       |
   +----------+----------+------------------------------------------------------------------------------------+----------------+
   | 2.4      | 20       | Rod withdrawal prohibit signal prevents operation of rods if minimum neutron       | 4.2.2          |
   |          |          | source level is not present.                                                       | (3.2.2b)       |
   +----------+----------+------------------------------------------------------------------------------------+----------------+

   D.3 Auto Mode Conditions:

   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | Section  | Steps  | Description                                                                                  | Tech Spec      |
   +==========+========+==============================================================================================+================+
   | 3.3      | 3-5    | No operator prevents entry into auto mode.                                                   |                |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 3.3      | 6-7    | Do not prevent auto mode if shim 1 and shim 2 are at the down limit.                         |                |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 3.3      | 8-9    | Rod withdrawal prohibit signal prevents operation of rods if minimum neutron source          | 4.2.2          |
   |          |        | level is not present.                                                                        | (3.2.2a)       |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 3.3      | 10,11  | Simultaneous withdrawal limits up motion to one rod excluding reg rod.                       | 4.2.2          |
   |          |        |                                                                                              | (3.2.2b)       |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 3.3      | 12     | "Fire" button for transient rod applies air to drive only if drive is down.                  | 4.2.2          |
   |          |        |                                                                                              | (3.2.2c)       |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 3.4      | 1-5    | Power demand switches determine regulating rod motion with a limit of 3-5 secs.              |                |
   |          |        | For the reactor period.                                                                      |                |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 3.4      | 7      | Rod magnet switch changes auto mode to manual mode.                                          |                |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 3.4      | 8      | Manual scram button changes auto to scram mode.                                              |                |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+

   D.4 Pulse Mode Conditions:

   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | Section  | Steps  | Description                                                                                  | Tech Spec      |
   +==========+========+==============================================================================================+================+
   | 4.1      | 1-4    | Prevent entry into pulse ready mode.                                                         |                |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 4.1      | 5-9    | Transient rod air off requirement.                                                           |                |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 4.1      | 10-11  | Reactor power level less than 1kw.                                                           | 4.2.2          |
   |          |        |                                                                                              | (3.2.2c)       |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 4.1      | 12-13  | 1 DPM limit for pulse mode.                                                                  |                |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 4.1      | 18-20  | Rod withdrawal prohibit signal prevents operation of transient rod if minimum neutron        | 4.2.2          |
   |          |        | source level is not present.                                                                 | (3.2.2a)       |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 4.1      | 21-23  | Pulse Withdrawal Interlock, no standard rod motion.                                          | 4.2.2          |
   |          |        |                                                                                              | (3.2.2d)       |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+

   D.5 Square Wave Mode Conditions:

   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | Section  | Steps  | Description                                                                                  | Tech Spec      |
   +==========+========+==============================================================================================+================+
   | 5.1      | 1-4    | Prevent entry into square ready mode.                                                        |                |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 5.1      | 5-9    | Transient rod air off requirement.                                                           |                |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 5.1      | 10-11  | Reactor power level less than 1 kw.                                                          | 4.2.2          |
   |          |        |                                                                                              | (3.2.2c)       |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 5.1      | 12-13  | 1 DPM limit for pulse mode.                                                                  |                |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 5.1      | 18-20  | Rod withdrawal prohibit signal prevents operation of transient rod if minimum neutron        | 4.2.2          |
   |          |        | source level is not present.                                                                 | (3.2.2a)       |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+
   | 5.1      | 21-23  | Pulse withdrawal interlock - no standard rod motion                                          | 4.2.2          |
   |          |        |                                                                                              | (3.2.2d)       |
   +----------+--------+----------------------------------------------------------------------------------------------+----------------+

.. _MAIN-1.II.C:

C. SCRAM Functions
~~~~~~~~~~~~~~~~~~

   **This section tests ICS safety circuit functions. SCRAM functions are independent of the digital control program. Several digital SCRAM conditions and system checks are also program-dependent.**

   D.6/7 Digital Control Program:

   +---------+--------+---------------------------------------------------------------+----------------+
   | Section | Steps  | Description                                                   | Tech Spec      |
   +=========+========+===============================================================+================+
   | 6.0     | 1–10   | Scram for data base timeout and network fault if both         |                |
   |         |        | low and high networks fail                                    |                |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.1     | 2      | Scram for CSC digital scanner timeout.                        |                |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.1     | 3–8    | Scram for CSC watchdog timeout.                               | 4.2.3          |
   |         |        |                                                               | (3.2.3f)       |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.2     | 2      | Scram for DAC digital scanner timeout.                        |                |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.2     | 3–8    | Scram for DAC watchdog timeout.                               | 4.2.3          |
   |         |        |                                                               | (3.2.3f)       |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.4     | 2      | NPP1000 pulse mode gain change relay function                 |                |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.4     | 2      | NP1000 pulse mode bypass relay function                       |                |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.4     | 2      | NM1000 pulse mode bypass relay function                       |                |
   +---------+--------+---------------------------------------------------------------+----------------+

   D.7 Fuel Temperature:

   +---------+--------+---------------------------------------------------------------+----------------+
   | Section | Steps  | Description                                                   | Tech Spec      |
   +=========+========+===============================================================+================+
   | 7.0     | 2      | FT#1 scram at 550 deg. C                                      | 4.2.3          |
   |         |        |                                                               | (3.2.3a)       |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.0     | 3      | FT#2 scram at 550 deg. C                                      | 4.2.3          |
   |         |        |                                                               | (3.2.3a)       |
   +---------+--------+---------------------------------------------------------------+----------------+

   D.7 Power Safety Channels:

   +---------+--------+---------------------------------------------------------------+----------------+
   | Section | Steps  | Description                                                   | Tech Spec      |
   +=========+========+===============================================================+================+
   | 7.0     | 4      | NPP1000 set point for high percentage power                   | 4.2.3          |
   |         |        |                                                               | (3.2.3b)       |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.0     | 4      | NPP1000 set point for high pulse peak power                   | 4.2.3          |
   |         |        |                                                               | (3.2.3b)       |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.0     | 5      | NP1000 set point for high percent power                       | 4.2.3          |
   |         |        |                                                               | (3.2.3b)       |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.0     | 9–10   | NM1000 Hi percent power or Lo high voltage                    | 4.2.3          |
   |         |        |                                                               | (3.2.3b)       |
   +---------+--------+---------------------------------------------------------------+----------------+

   D.7 Operable Systems:

   +---------+--------+---------------------------------------------------------------+----------------+
   | Section | Steps  | Description                                                   | Tech Spec      |
   +=========+========+===============================================================+================+
   | 7.0     | 6      | Scram for manual pushbutton                                   | 4.2.3          |
   |         |        |                                                               | (3.2.3d)       |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.0     | 7      | Scram for magnet key switch                                   | 4.2.3          |
   |         |        |                                                               | (3.2.3e)       |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.0     | 8      | Magnet supply voltage and ground detection                    |                |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.0     | 11–12  | NM1000 Hi percent power or Lo high voltage                    | 4.2.3          |
   |         |        |                                                               | (3.2.3c)       |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.0     | 13     | NPP1000 set point for high voltage loss                       | 4.2.3          |
   |         |        |                                                               | (3.2.3c)       |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.0     | 14     | NP1000 set point for high voltage loss                        | 4.2.3          |
   |         |        |                                                               | (3.2.3c)       |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.0     | 17     | Scram for low pool level condition sensors                    |                |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.3     | 2      | Scram NM1000 communication fault                              |                |
   +---------+--------+---------------------------------------------------------------+----------------+
   | 7.3     | 4      | Scram for NM1000 data base timeout.                           |                |
   +---------+--------+---------------------------------------------------------------+----------------+

.. _MAIN-1.II.D:

D. Instructions
~~~~~~~~~~~~~~~

.. _main-1.ii.1.0:

   **1.0 OPERATOR LOG ON/OFF**

   (1) Complete successful power up sequence. Refer to Acceptance Test Procedures, section 1.0 steps (1-3)

   (2) Initiate the operator log in sequence by pressing "F5" functions key. A menu should appear.

      Menu>Reactor Operator Log On/Off Utility...

   (3) Select item 1, "Operator Log In," by pressing the "1" key. A prompt should appear below the menu.

      Prompt > Please enter your password ->

   (4) Enter an invalid password "ABCDEF". A message should momentarily appear below menu.

      Message > Invalid Password...Permission Denied!

   (5) Initiate the operator log in sequence by pressing the "F5" function key. A menu should appear.

      Menu > Reactor Operator Log On/Off Utility...

   (6) Select item 1, "Operator Log In," by pressing the "I" key. A prompt should appear below the menu.

      Prompt > Please enter your password ->

   (7) Enter a valid password "MIRAGE". A message should momentarily appear below the menu.

      Message > Accepted — Welcome to the Triga Control System

   (8) Initiate the operator log in sequence by pressing the "F5" function key. A menu should appear.

      Menu > Reactor Operator Log On/Off Utility...

   (9) Select item 1, "Operator Log In, "by pressing the "I" key. A prompt should appear below the menu.

      Message > Replace Operator #_? (Y/N)

   (10) Respond "N" to prompt to continue.

   (11) Press switch to start the Prestart Checks sequence. Verify the Prestart Checks completes successfully.

   (12) Switch Magnet Key Switch to "RESET" (RSET), then"ON". The system will enter the Manual mode.

   (13) Initiate the operator log in sequence by pressing the "F5" function key. A menu should appear.

      Menu > Rector Operator Log On/Off Utility...

   (14) Select item 2, "Operator Log Off', by pressing the "2" key. A message should momentarily appear below the menu.

      Message > Reactor Active, Cannot log out!

   (15) Return system to SCRAM mode by switching Magnet Key Switch to "off".

   (16) Initiate the operator log in sequence by pressing "FS" function key. A menu should appear.

      Menu > Reactor Operator Log On/Off Utility...

   (17) Select item 2, "Operator Log Off', by pressing the "2" key. A message should momentarily appear below the menu.

      Message > Operator Log off...Goodbye!

   (18) Press the <spacebar> to return to the Standard Display, STW.

      Maintain a record of the operator, hours and energy. Note that a correction is needed for any "pseudo" data present if any calibration or testing activities generate power level data. This data should always be the total for the password applicable to this procedure.

.. _MAIN-1.II.2.0:

2.0 MANUAL MODE

   Complete the checks of section 1.0.

.. _main-1.ii.2.1:

2.1 ENTERING THE MANUAL MODE

   The manual mode will be entered when all the following conditions exist:

      (a) No SCRAM conditions are present.
      (b) An operator is logged in
      (c) Key switch for magnet current is 1 the "ON" position.
      (d) Auto Preset mode is completed successfully.

   Consult Acceptance Test Procedures, System Startup (section 1.0), Operator Log On/Off (section 2.0) and SCRAM Conditions (section 4.0) for these items.

.. _main-1.ii.2.2:

2.2 EXITING THE MANUAL MODE

   The Manual mode will be exited when any of the following conditions exist:

      (a) ASCRAM condition occurs.
      (b) The Pulse mode is invoked.
      (c) The Auto mode is invoked.
      (d) The Square Wave mode is invoked.

   Consult Acceptance Test Procedures, SCRAM (section 4.0), Pulse (section 6.0), Auto (section 7.0), and Square Wave (section 8.0) mode for these items.

.. _main-1.ii.2.3:

2.3 INITIATION AND TERMINATION OF MANUAL MODE

   (1) Power up the system and allow the system to compete its startup sequence indicated by the reactor animation and STW (Standard Text Window) screens being displayed.

      (a) The Reactor Display mode should be "SCRAM".
      (b) All the Reactor Mode pushbutton lights should be off.
      (c) Auto-wind down of all rod drives is invoked in the SCRAM mode.
      (d) Magnet Power — Air Supply to the rod drives should be off. Off indicated by the corresponding indicator boxes below the graphic rod drives being black on the reactor Display (graphic display).

   (2) Clear all SRAM conditions and acknowledge and SCRAM or warning messages in the AW (alarm window) by pressing the "ACKNOWELDGE" button. (ACK)

   (3) Operate the "MAGNET POWER" key switch from "ON" to "RESET" to "ON". The Reactor Control Console should beep indicating an invalid operation has been attempted. A message should appear in the AW and the SCw.

      Message > SCRAM - Please Log In

   (4) Acknowledge the SCRAM message by pressing the "ACK" button. "SCRAM -— Please Log In "message should be cleared form both the AW and he SCW.

   (5) Initiate the operator login sequence by pressing the "5" function key. A menu and prompt should appear.

      Menu > Reactor Operator Log On/Off Utility

   (6) Select item 1, "Operator Log In," by pressing the "I" key. A prompt should appear below menu.

      Prompt > Please enter your password -> 

   (7) Press the "Manual SCRAM" button. A message should appear in the AW and the SCW. Do not acknowledge the error condition.

      Message > SCRAM — Console Pushbutton

   (8) Attempt to invoke the Manual mode by operating the "MAGNET POWER? key switch from "ON" to "RSET" to "ON".

      (a) Do not acknowledge scram message.
      (b) The system should re-enter the "SCRAM" mode.
      (c) The SCRAM condition message will still exist.

   (9) Acknowledge the SCRAM message by pressing the "ACK" button. "SCRAM - console pushbutton" message should be cleared from both the AW and SC.

   (10) Attempt to invoke the manual mode by operating the "MAGNET POWER" key switch again. This time, the Manual mode should be invoked.

      (a) The manual mode will be indicated by the "MANUAL" push button light coming on.
      (b) Reactor Display mode will indicate "Steady State".
      (c) Magnet Power indicator boxes on graphic rod drives turn ycllow.
      (d) Rod magnet power will indicate on the Reactor Display.
      (e) Air Supply to the Transient rod drive will not be applied by entering the Manual mode so its Air Supply status box below its graphic rod drive will remain unlit.

   (11) Compiete procedures of the next section then terminate operation by operation of the "MAGNET POWER" key switch to the "OFF" position. Verify the conditions of step (1) exist.

.. _main-1.ii.2.4:

2.4 OPERATION WITHIN THE MANUAL MODE

   (1) Invoke the Manual mode as described above.

      (a) The display animation includes a representation of the Drive, Magnet, and the Rod. All should move in unison.
      (b) The rod position is represented by a number between 0 and 960.
      (c) Any rod position should be attainable via "UP" and "DOWN" buttons.

   (2) Press and hold the Reg Rod "UP" button. Verify the Reg rod and graphic Reg rod begin to withdraw out from the reactor core and the numeric rod position increases in value.

   (3) Release the Reg rod "UP" button. Verify the Reg rod and the graphic rod drive stop moving and the numeric readout stops increasing, The actual position of the rod drive and the graphic representation should correspond.

   (4) Press and release the "UP" button. There should be no appreciable delay between release of button and termination of change in numerical number.

   (5) Press and hold the Reg rod "DOWN" button. Verify the Reg rod and graphic Reg rod begin to insert back in to the core and the numeric rod position below the graphic rod drive decreases in value.

   (6) Release the Reg rod "DOWN" button. Verify the Red rod and the graphic rod drive stop moving and the numeric readout stops decreasing. The actual position of the rod drive and the graphic representation should correspond.

   (7) Press and release the "DOWN" button. There should be no appreciable delay between release of button and termination of change in numerical number.

   (8) Press and hold the Reg rod "UP" button. Simultaneously press the Reg rod "DOWN" button. Motion should stop. 

      \*Motion cannot be restarted until both buttons have been released and one or the other is activated again.

   (9) Press and hold the Reg rod "DOWN" button. Simultaneously press the Reg rod "UP" button. Motion should stop.
      
      \*Motion cannot be restarted until both buttons have been released and one or the other is activated again.

   (10) Press and hold the Reg rod "UP" button to test the simultaneous withdrawal logic. Simultaneously press any other rod "UP" button and verify Reg rod and animation movement stops and other rod drive does not start.

      \*Motion cannot be restarted until both buttons have been released and omor the other is activated again.

      Repeat this step for all other rod "UP" buttons.

   (11) Move the Shim rods off the bottom so there will be room to move down.

   (12) Press and hold the Reg rod ""UP" button. Simultancously press any or all "DOWN" down buttons. The Reg rod should continue it's outward motion while other rod or rods should move downward. Release all buttons and all rod movements should stop.

   (13) Press and hold the Reg rod "DOWN" button. Simultaneously press any or all other rod "DOWN" buttons, The Reg rod and all other rods should continue move downward. Release all buttons and all rod movements should stop.

   (14) Press the Reg rod "MAGENT" current button to SCRAM rod. If the button is held longer than 1 second, the yellow box representing the Reg rod's magnet current will go black as long as the button is held depressed. When the button is released, the magnet current is restored and the Reg rod magnet box is illuminated.

   (15) Repeat steps (2) through (14) for each Shim rod.

   (16) At this point, the Transient Rod and Drive Mechanism should be fully down and the Air Supply Off. The Air Supply status box below the graphic Transient Rod Drive Mechanism should be greyed out indicating Air is not applied.

   (17) Press "FIRE" button to apply airto the Transient Rod Drive Mechanism. The Transient rod should move approximately 4 inch and the Air Supply status box should change to yellow indicating air is applied.

   (18) Repeat steps (2) through (14) for the Transient rod. For the Transient rod, the "MAGNET" button is replaced by an "AIR" button.

   (19) To reapply Air, the "FIRE" button must be pressed with the rod drive at the bottom limit. Verify this safety feature by attempting to turn the Air back on while the Transient rod drive is in Auto-wind down operation.

   (20) Activate the NM1000 Rod Withdrawal Prohibit signal, "RWP!", by pulling the neutron source (ensure below 2 cps) and verifying that Reg rod, Shim 1, Shim 2 and Transient rod cannot be withdrawn from the core by pressing their associated rod "UP" buttons. Ensure a warning message appears in the AW and the WAW

      Message > Minimum Source Interlock

   Reinstall the source.

.. _main-1.ii.3.0:

3.0 AUTO MODE

   The Auto Mode automatically controls the reactor power to be equal to the Demand Power set inte the "Demand Power" thumbwheel switches. Control is accomplished by a PID algorithm controlling the position and speed of the Reg rod. 

   If the reactor power is at some value above or below the demand power and the Auto mode is invoked, the Auto mode algorithms will move the Reg rod to bring reactor power equal to the demand power setting.

   The Reg red control is always by computer in the Auto mode.

   The checks in this section require the operation of the reactor at power. Exclude these checks until completion of all startup processes and the basic acceptance for power operations.

.. _main-1.ii.3.1:

3.1 ENTERING THE AUTO MODE

   The Auto mode is entered if:

   (a) While in manual mode, the "AUTO" mode button is pressed manually.
   (b) The Square Wave ramp up sequence is completed successfully.

.. _main-1.ii.3.2:

3.2 EXITING THE AUTO MODE

   The Auto mode is exited if:

   (a) The Manual! mode is selected, or
   (b) Any rod is scrammed, or
   (c) Any SCRAM condition exists.

.. _main-1.ii.3.3:

3.3 INITIATION AND TERMINATION OF THE AUTO MODE

   (1) Power up the system and allow the system to complete its startup sequence indicated by the reactor animation and the STW screens being displayed.

   The Reactor Display mode should be in "SCRAM, all Reactor Mode lights off, all Magnet Power and Air indicators lights should be extinguished on Reactor Display and below graphic rod drives.

   (2) Clear all SCRAM conditions and acknowledge any SCRAM or warning messages in the AW by pressing the "ACK" button.

   (3) Press the "AUTO" mode pushbutton to invoke the Auto mode. Verify that the system does not change modes and the system beeps once indicting an invalid operation is being attempted.

   (4) Initiate the operator login sequence by pressing the "F5" functions key. A menu and prompt should appear:

      Menu > Reactor Operator Log On/Off Utility

   Select Operator log in by pressing key "1"

      Prompt > Please enter your password

   Enter "MIRAGE"

   (5) Repeat step (3).

   (6) Turn the MAGNET power key switch to the RESET position. Clear all SCRAM and Warning messages and place the system into the Manual mode.

   (7) Set Auto mode Demand thumbwheel to "O000E0". Press the "AUTO" mode pushbutton to invoke the Auto mode.

   (8) Activate the NM1000 Rod Withdrawal Prohibit signal, "RWP1", by removing the neutron source. Verify that the Reg, Shim 1, Shim 2, and Transient rods cannot be withdrawn from the core by pressing the associated rods "UP" button.

   Set demand power above current power and ensure the Reg rod does not move. A warning message should appear in the AW and WAW for Shim and Transient rods only.

      Message > Minimum Source Interlock

   (9) Restore neutron source.

   (10) Apply Transient rod air. Press and hold the transient rod "UP" button to test the simultaneous withdrawal logic. Press other rod "UP" button except Reg rod and verify Transient rod drive stops and the other rod does not move.

      \*Movement cannot be restarted until both buttons have been released and the drive "UP" button is pressed again.

   Repeat this step for the rod except the Reg rod.

   (11) Repeat step 10 for each Shim rod.

   (12) Return all rods to full down position and remove air from Transient rod by pressing "AIR" button. Depress AUTO button and verify it enters AUTO mode.

   Raise Transient drive cylinder to about 50 units. Attempt to fire transient rod by pressing "FIRE" button. Verify rod does not fire and "AIR" light does not come on.

   Return Transient drive to full down position.

   (13) Turn the MAGNET power key switch to the RESET position. Clear all the SCRAM and warning messages and place the system into the Manual Operate mode.

   (14) Start up the reactor in the manual! mode toa power level of about 50 watts using the banked rod configuration,

   (15) Set the "Demand Power" thumbwheel switches to match the current power being produced by the reactor.

   (16) Press the "AUTO" mode pushbutton to invoke the auto mode. Verify the "AUTO" mode light comes on and the "MAN" light goes off and the Reactor Display should indicate Auto mode.

   (17) Press the "MAN" pushbutton to invoke the Manual mode. Verify the "Man" light illuminates and the "AUTO" light distinguishes. The Reactor Display should indicate Steady State mode.

   (18) Move the Reg Rod Drive Mechanism to full insertion with the remaining rods and thumbwheels set per items (14) and (15) above. Invoke the auto mode and the system should stay in the AUTO mode.

.. _main-1.ii.3.4:

3.4 OPERATION WITHIN THE AUTO MODE

   (1) Set the "Demand Power" thumb-wheel above the current power level. Verify the reactor power changes to the demand level. Confirm a 3 to 5 second period limit of the power response.

   (2) Set the "Demand Power" setting below power level. Verify the reactor power changes to the demand power and the period is negative.

   (3) Vary the setting of the "Demand Power" thumbwheel above and below the current power level. Adjust the position of the Transient and Shim rods as necessary to limit the power level less than 1 KW. Verify the Reg rod servos down to 0% and up to 100%.

   (4) Set the "Demand Power" level to 50 W, and remain in auto mode. Change position of Transient and Shim rods manually. Verify 50 W is maintained by up and down movement of Reg rod to compensate for the up and down movement of Transient and Reg rods.

   (5) Adjust the position of Shim 1, Shim 2, and Transient rods to balance the power profile of the reactor, maintaining Reg rod near mid position.

   (6) Operate in Auto mode for about 20 minutes. Observe any Auto mode drift and verify ability of power to maintain within +/- 10 percent.

   (7) While in Auto mode, press the magnet power switch or air button of a control rod. Verify mode changes to Manual. Return system to Auto mode and repeat for each remaining rod.

   (8) Reenter Auto mode, then press the "MANUAL SCRAM" button. Verify system changes to "SCRAM" mode and all mode lights extinguish.

.. _main-1.ii.4.0:

4.0 PULSE MODE

   The Pulse Ready Mode is initiated from the Manual mode by pressing the "PULSE" mode button and entering a pulse ID string. The pulse is initiated from the Pulse Ready mode by pressing the "FIRE" button. 5000 power reading are taken during the 4 second pulse period.

.. _main-1.ii.4.1:

4.1 ENTERING THE PULSE READY MODE

   (1) Place the system in SCRAM mode. Press the "PULSE" button on the control console. You should hear a beep; the system should remain in the SCRAM mode.

   (2) Place the system in AUTO mode. Press the "PULSE" button. You should hear a beep; the system should remain in AUTO mode. Return the system to MANUAL mode.

   (3) Place the system in SQUARE WAVE READY mode. Press the "PULSE" button. You should hear a beep; the system should remain in SQUARE WAVE READY mode.

   (4) Place the system in MANUAL mode.

   (5) Press "AIR" button on the control console. If transient rod air supply was on, it will turn offand the Transient rod will fall to the bottom of the reactor core. The rod drive will then wind down automatically to its bottom position.

   (6) Press the "FIRE" button to turn on the air pressure to the Transient rod.

   (7) Press the "PULSE" button. You should hear a beep and the system should remain in the MANUAL mode. A warning message should appear in the AW and WAW.

      Message > Trans Rod Air must be off!

   (8) Remove the air supply to the Transient rod by pressing the "AIR" button.

   (9) Acknowledge the warning message by pressing the "ACK" button. The warming message on the AW and WAWW should disappear.

   (10) Raise the reactor power above IkW. Press the "PULSE" button. You should hear a beep and the system should remain in MANUAL mode. A warning message should appear in the AW and WAW.

      Message > Power too high to pulse!

   (11) Lower the reactor power below 1 kW. Acknowledge the warning message by pressing the "ACK" button. The warning message on the AW and the WAW should disappear.

   (12) Introduce a positive period of about 15 seconds to the reactor. While the 15 second period is occurring, press the "PULSE" button. You should heara beep. The system should remain in MANUAL mode. A warning message should appear in the AW and the WAW.

      Message > Period too short to pulse!

   (13) Acknowledge the warning message by pressing the "ACK" button. The warning message on the AW and the WAW should disappear.

   (14) Prepare the system to enter the PULSE READY mode by creating the following conditions:

      (a) System in MANUAL mode.
      (b) Reactor power is less than 1 kW.
      (c) The rate of change of reactor power is less than 1 DPM.
      (d) The Transient rod air pressure is off and the Transient rod is down.
      (e) Position Reg and Shim rods at about 50 units.

   (15) Press the "PULSE" button. Verify the PULSE button illuminates and the STW should be replaced by:

      Message > Enter Pulse ID String -->

   (16) Enter a string of characters to identify the pulse followed by a carriage return. (MAIN 1-MM/YY. The STW should reappear.

   (17) Move Transient rod drive to about 50 units. (Air must be off)

   (18) Activate the NM1000 Rod Withdrawal Prohibit signal, "RWP1" by pulling the neutron source. (Wait for PWR to lower below 2mw)

   (19) Press the "FIRE" button to apply air to the Transient rod drive mechanism. The Transient rod should not move. The "AIR" light should not illuminate and a warning message should appear in the AW and the WAW;

      Message > Minimum Source Interlock

   (20) Restore the neutron source.

   (21) With system in PULSE mode, attempt to drive Reg rod out using "UP" button on console. Verify the Reg rod does not move up but will move down.

   (22) Repeat step (21) for Shim 1 rod.

   (23) Repeat step (21) for Shim 2 rod.

   (24) Fire Pulse with all rods withdrawn to about 50 units and measure the time the pulse rod remains withdrawn (shall be less than 15 seconds).

   (25) Return from Pulse mode to Scram mode.

.. _main-1.ii.5.0:

5.0 SQUARE WAVE MODE

   The square wave mode is initiated from the MANUAL mode by pressing the "Square Wave" button. The mode combines the reactor control features of both pulse and auto mode. A pulse performed with sufficient reactivity to reach demand power for the auto control of the reactor power level. The PID algorithm controls the duration of the operation until a manual SCRAM shutdown terminates the mode.

   Interlocks which prevent entry into Square Wave Ready mode are tested in steps (1) through (13) of this section.

.. _main-1.ii.5.1:

5.1 ENTERING THE SQUARE WAVE READY MODE

   (1) Place the system in SCRAM mode. Press the "SQUARE WAVE" button on the control console. You should hear a beep; the system should remain in SCRAM mode.

   (2) Place the system in AUTO mode. Press the "SQUARE WAVE" button. You should hear a beep; the system should remain in AUTO mode. Return system to MANUAL mode.

   (3) Place the systemin PULSE READY mode. Press the "SQUARE WAVE" button. You should hear a beep; the system should remain in PULSE READY mode.

   (4) Place the system in MANUAL mode.

   (5) Press the "AIR" button on the control console. If the transient rod air supply was on, it will turn off and the transient rod will fall to the bottom of the reactor core. The rod drive will then wind down automatically to its bottom-most position.

   (6) Press the "FIRE" button to turn on the air pressure to the transient rod,

   (7) Press the "SQUARE WAVE" button. You should hear a beep; the system should remain in MANUAL mode. A warning message should appear in the AW and the WAW:

      Message > Trans Rod Air must be off

   (8) Remove the air supply to the transient rod by pressing the "AIR" button.

   (9) Acknowledge the warning message by pressing the "ACK" button. The warning message on the AW and WAW should disappear.

   (10) Raise reactor power above 1 kW. Press the "SQUARE WAVE" button. You should hear a becp; a warning message should appear in the AW and WAW:

      Message > Power too high to pulse

   (11) Lower the reactor power below 1 kW. Acknowledge the warning message by pressing the "ACK" button. The warning message on the AW and WAW should disappear.

   (12) Introduce a positive period of about 15 seconds to the reactor. While the 15 second period is occurring, press the "SQUARE WAVE" button. You should hear a beep; the system should remain in MANUAL mode. A warning message should appear in the AW and WAW;

      Message > Period too short to pulse

   (13) Acknowledge the warning message by pressing the "CK" button. The warning message on the AW and WAW should disappear.

   (14) Prepare the system to enter the SQUARE WAVE modc by ensuring the following:

      (a) System is in MANUAL mode.
      (b) Reactor power is less than 1 kW.
      (c) The rate of change of reactor power is less than 1 DPM.
      (d) The Transient rod air pressure is off and the transient rod is all the way down.
      (e) The Reg rod and both Shim rods are positioned at about 50 units.

   (15) Press the "SQUARE WAVE" button. The mode should read "SQUARE WAVE READY" on the graphic display and the Square wave button should be illuminated.

   (16) Move the Transient rod drive to about 50 units. Ensure Air is off.

   (17) Activate the NM1000 Rod Withdrawal Prohibit signal "RWP1", by pulling the neutron source.

   (18) Press "FIRE" button to apply Air to Transient Rod Drive Mechanism. The Transient rod should not move, the "AJR light should not illuminate and a warning message should appear in the AW and WAW;

      Message > Minimum Source Interlock

   (19) Restore the neutron source.

   (20) With the system in the Square wave ready mode, attempt to drive the Reg rod out. Verify the Reg rod does not move up but will move down.

   (21) Repeat step (20) for Shim 1 and Shim 2 rods.

   (22) Return to MANUAL mode. 

.. _main-1.ii.6.0:

6.0 NETWORK

   (1) Verify the network (boards, cables and terminators) is installed in the CSC and the DAC and that both the CSC and DAC power is off. The CSC instrument power switches initiates power to the CSC and DAC. The DAC power switch controls power to the DAC rack only.

   (2) Switch the DAC power switch to off. Power up the CSC. Observe that the CSC memory test and the operating system boot up properly, and that the application bootup sequence starts. Verify that during the application bootup sequence, the CSC bootup fails the network test.

      Message > Network Test Cycle ##: Network looks dead

   (3) Verify the test number increments every 5 seconds indicating the test is being repeated.

   (4) Power up the DAC. Allow sufficient time for the DAC to complete its memory test, boot its operating system, and start its application bootup sequence (maximum of 3minutes). At this point the CSC network test cycle should complete successfully.

      Message > Network Test Cycle ##: Network looks OK

   Make boot log entry

   (5) Verify the CSC completes its boot by observing the Rector Display and Standard Display screens being displayed.

   (6) Verify that none of the following network failure messages appear in the AW, WAW or SCW;

      (a) SCRAM, Database Timeout
      (b) Hi IC-NET Comm Fault
      (c) SCRAM — NET Fault, Please Reboot

   (7) Verify the network is operating by changing some DAC input such as reactor room door status. Observe the change on the AW and STW.

   (8) Locate the CSC network plug. The plug is accessed from the rear of the CSC control console computer.

   (9) Place the system in Manual (Steady State) mode and remove the terminator plug from the CSC Network board. Verify;

      (a) A "Hi IC-NET Comm Fault" messaged queued in the AW
      (b) A"SCRAM — NET Fault, Please Reboot" message is queued in AW.
      (c) A"SCRAM — Database Timeout" message qucucd in AW,
      (d) A "Hi IC-NET Comm Fault" message is displayed in the WAW.
      (e) A"SCRAM-NET Fault, Please Reboot" message is displayed on SCWw.
      (f) A "SCRAM-Database Time out" message is displayed in SCW.
      (g) The reactor is SCRAMMED,
      (h) The Reactor Display mode is SCRAMMED.
      (i) The "MAN" pushbutton light is extinguished.

   (10) Restore the network plug to the CSC network board and reboot both the CSC and the DAC by turning the power off both units for 10 seconds and then repowering the units. Verify that the system successfully reboots and the network is totally operational as outlined above.

.. _main-1.ii.7.0:

7.0 SCRAM MODE

   (1) Clear all SCRAM and warning messages and place the system into the Manual Operate mode (use KEY RSET to clear any SCRAMS not cleared by "ACK" button).

   (2) Simulate a Fuel Temp #1 SCRAM by using the CSC SCRAM test switch. Verify that the following conditions occur, including SCRAM at indication of 550°C.

      (a) A message appears in the AW and the SCW.

      Message > SCRAM ~— Fucl Temp #1 Hi

      (b) The reactor to be SCRAMMED.
      (c) The Reactor Display to be SCRAMMED.
      (d) The mode changes to SCRAM and the MAN pushbutton light extinguishes.
      (e) Magnet and air turn off and rod drives wind down.

   (3) Repeat step (1) and (2) for Fuel Temp #2 TC.

   (4) Repeat step (1). Simulate an NPP1000 #1 % Power Hi SCRAM condition to the DAC by using the CSC Scram Test Switch. Verify:

      (a) A message appears in the AW and SCW.

      Message > SCRAM — NPP1000 Power "Hi"

      (b) The reactor to be SCRAMMED.
      (c) The Reactor Display to be SCRAMMED.
      (d) The MAN pushbutton light to be extinguished.

   (5) Repeat (1) and (4) for NP1000 % Power Hi SCRAM.

   (6) Repeat step (1). Switch the Magnet Power key switch to "OFF". Verify that the following conditions occur:

      (a) The message "SCRAM ~ Key Switch Off" to appear in the AW and SCW.
      (b) The reactor to be SCRAMMED.
      (c) The Reactor Display to be SCRAMMED.
      (d) The MAN pushbutton light extinguished.

   (7) Repeat step (1). Press manual SCRAM switch. Verify that the following conditions occur:

      (a) The message "SCRAM — Console Pushbutton" appear in AW and SCW.
      (b) The reactor to be SCRAMMED.
      (c) The Reactor Display to be SCRAMMED.
      (d) The MAN pushbutton light to be extinguished.

   (8) Test the ground fault detect circuit by a momentary ground of the supply and return lines of the scram circuit. Ground each circuit one at a time. A message appears in AW,

      Message > Mag Power Grounded — Hi Side
      Message > Mag Power Grounded — Lo Side

   (9) Repeat step (1). Simulate an NM1000 % Power Hi SCRAM condition to the DAC using the Operation Mode 5 by pressing "F5 0 F8 5 ENTER". Verify this causes:

      (a) A message appears in the AW and the SCW.

         Message > SCRAM —NM 1000 Power Hi
         
      (b) The reactor to be SCRAMMED.
      (c) The Reactor Display to be SCRAMMED.
      (d) The MAN pushbutton light to be extinguished.

   (10) Reset F5 pressing "F5 0 F8 0 ENTER".

   (11) Repeat step (1). Simulate an NM1000 HV loss condition to the DAC by removing connector JI from the HV distribution and monitoring module in the NM1000 preamp cabinet. Verify this causes the following: 

      (a) A message appears in the AW, SCW and WAW.

         Message > SCRAM —NM1000 Power Hi

      (b) The reactor to be SCRAMMED.
      (c) The Reactor Display to be SCRAMMED.
      (d) The MAN pushbutton light extinguishes.

   (12) Reconnect J1 and press "F7 90 ENTER".

   (13) Repeat step (1). Simulate high voltage scram conditions in the NPP1000 by using the Scram Test Switches. Verify the following conditions occur:

      (a) A message appears in the AW and the SCW.

         Message > SCRAM — NPP1000 HV Lo

      (b) The reactor to be SCAMMED.
      (c) The Reactor Display to be SCRAMMED.
      (d) The MAN pushbutton light extinguishes.

   (14) Repeat step (1). Repeat step (13) for the NP 1000.

   (15) Repeat step (1). Momentarily disconnect AC power from the NPP1000 and NP!000. Verify the following conditions occur:

      (a) A message appears in the AW and the SCW.

         Message > 

            SCRAM — NPP1000 HV Lo
            SCRAM — NPP1000 Power Hi
            SCRAM — NP1000 HV Lo
            SCRAM — NP1000 Power Hi

      (b) The reactor to be SCRAMMED.
      (c) The Reactor Display to be SCRAMMED.
      (d) The MAN pushbutton light extinguishes.

   (16) Repeat step (1). Move each switch float to the DAC "Pool Water Lo" input. Verify that the following conditions occur:

      (a) A message appears in the AW and the SCW. 

         Message >SCRAM -— Pool Water Lo

      (b) The reactor to be SCRAMMED.
      (c) The reactor Display to be SCRAMMED.
      (d) The MAN pushbutton light extinguishes.

   (17) Test operation of external scrams (positive scram bus).

   (18) Test operation of external scrams (negative scram bus).

.. _main-1.ii.7.1:

7.1 CSC PROGRAM LOGIC FAILURE

   (1) Repeat step (1) of Section 7.0

   (2) Momentarily disconnect the communication cable at the CSC computer (HS) to disrupt the CSC DIS064 Digital Scanner board. (Wait for at least 10 seconds). Verify this causes the following:

      (a) A message appears in the AW and the SCW.

         Message > SCRAM — CSC Watchdog Timeout
         SCRAM — CSC DIS64 Timeout

      (b) The reactor to be SCRAMMED.
      (c) The reactor display to be SCRAMMED.
      (d) The MAN pushbutton light extinguishes.

   Reconnect HS.

   (3) Repeat step (1) of Section 7.0. Test CSC Watchdog trip relay with console test switch. Verify the following:

      (a) A message appears in the AW and the SCW.

         Message > SCRAM — CSC Watchdog Timeout.

      (b) The reactor to be SCRAMMED.
      (c) The Reactor Display to be SCRAMMED.
      (d) The MAN pushbutton light extinguishes.

   (4) Repeat step (1) of Section 7.0. Enter "CTRL-ALT-2 on the keyboard to switch to the command window. The prompt should be visible.

      Prompt > Login

   (5) Enter the command "root" followed by "sin—n1" followed by <return>. The CSC operating system should list the current process table. Look for the ## associated with "usr/ga/sc".

   (6) Enter the command "/bin/kill -n1##" where ## is the sc PID obtained from the process table. This should kill the scanner process and trigger the CSC Watchdogs.

   (7) Enter the command "CTRL-ALT-I to return to status window.

   (8) Enter the command "CTR-C" to reboot the DAC and restart the CSC software.

   (9) Verify the following:

      (a) Red SCRAM button illuminates.
      (b) The reactor SCRAMs as the control rods drop.
      (c) The Reactor Display does not change to SCRAM.
      (d) The MAN pushbutton does not extinguish.

   (10) Reboot.

.. _main-1.ii.7.2:

7.2 DAC PROGRAM LOGIC FAILURE

   (1) Repeat step (1) of Section 7.0.

   (2) Momentarily disconnect the communication cable at the DAC computer (H26) to disrupt the DAC DIS064 Digital scanner board. Wait for at least 10 seconds. Verify this causes the following, then reconnect H26.

      (a) A message appears in the AW and SCW.

         Message > SCRAM — DAC DIS64 Timeout

      (b) The reactor to be SCRAMMED.
      (c) The reactor display to be SCRAMMED.
      (d) The MAN pushbutton light is extinguished.

   (3) Repeat step (1) of Section 7.0. Test DAC Watchdog trip relay with console test switch. Verify the following:

      (a) A message appears in the AW and the SCW.

         Message > SCRAM — DAC Watchdog Timeout.

      (b) The reactor to be SCRAMMED.
      (c) The Reactor Display to be SCRAMMED.
      (d) The MAN pushbutton light is extinguished.

   (4) Repeat step (1) of Section 7.0. On the CSC keyboard enter "CTR-ALT-2" on the keyboard to switch the display to the command window. The prompt should be visible.

      Prompt > Login

   (5) Enter the command "root" followed by "sin —n2" followed by <return>. The DAC operating system (mode 2) should list the current process table. Look for the ## associated with usr/ga/scn’"’.

   (6) Enter the command "/bin/kill —n2 ##" when "##" is the scn PID number obtained from the process table. This should kill the scanner process and trigger the DAC Watchdogs.

   (7) Enter the command "CTRL-ALT-1" to return to status window.

   (8) Enter the command "CTRL-C" to reboot the DAC and restart the CSC software.

   (9) Verify the following:

      (a) A message appears in the AW and the SCW.

         Message > SCRAM - Database Timeout.
         
      (b) The reactor to be SCRAMMED.
      (c) The Reactor Display to be SCRAMMED.
      (d) The MAN pushbutton light to be extinguished.

   (10) Re-boot.

.. _main-1.ii.7.3:

7.3 NM1000 PROGRAM LOGIC FAILURE

   Check and test NM1000 System by simulation of NM1000 Fault conditions to the DAC.

   (1) Repeat step (1) of section 7.0.

   (2) Disconnect the communication cable at the NM1000. Cable designation is A5-P2 on circuit board in NM1000 Processor Cabinet. Verify that a message appears in the AW:

      Message > SCRAM NM1000 Comm Fault

   Reconnect A5-P2 to the circuit board. Clear fault condition using "F7 90 Enter".

   (3) Repeat section 7.0 step (1).

   (4) Change the value of a stack constant in the NM1000. Press "F4 3", then enter new value of 3 or 4 (whichever is not current value) by pressing "F8 # ENTER". Verify that a message appears in the AW:

      Message > NM1000 Stack Fault

   Reset the value to the original value by pressing "F4 3" and then enter the original value by pressing "F8 # ENTER". Clear the fault condition using "F7 90 ENTER".

.. _main-1.ii.7.4:

7.4 PULSE MODE FUNCTIONS (No actions necessary)

   (1) Operational test of the NPP1000 scram in step 7.0 (4) verifies circuit performance for the peak pulse power trip. Check of the circuit gain change occurs in step 7.4 (2). Measurement of the gain change is done by calibration procedure (MAIN 2).

   (2) The Pulse mode scram circuit relays for NPP!000 gain change, NP1000 bypass and the NM1000 bypass are subject to functional test as part of the prestart check sequence. Successful completion of the sequence requires the NPP1000, NP1000, and the NM1000 to actuate scram trips with a preset input signal.

   A Hi Power trip for the NPP1000 will occur only if the gain change relay is in the non-pulse configuration. A Hi Power trip of the NP1000 will occur only if the bypass is in the non-pulse mode. A Hi Power trip of NM1000 will occur only if the bypass relay is in the non-pulse mode.

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

   .. line-block::
      :ref:`A. Introduction <MAIN-2.II.A>`  
      :ref:`B. Magnet Power Supply <MAIN-2.II.B>`  
      :ref:`C. Fuel Temperature Channels <MAIN-2.II.C>`  
      :ref:`D. NM1000 Wide Range Channel <MAIN-2.II.D>`  
      :ref:`E. Power Monitoring Channels <MAIN-2.II.E>`
         :ref:`NP1000 Safety Channel <MAIN-2.II.E.NP1000>`  
         :ref:`NPP1000 Safety Channel <MAIN-2.II.E.NPP1000>`  
         :ref:`NPP1000 Safety Channel (pulse circuits) <MAIN-2.II.E.NPP1000.Pulse>`

E. Attachments
~~~~~~~~~~~~~~

   .. line-block::
      1. Magnet circuit and fuel temp
      2. NM1000 wide range channel
      3. NP(P)1000 % safety channels

F. Equipment, Materials
~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
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

   .. line-block::
      1. UT TRIGA Mechanical System Manual (Parts 1,2,3, and 4)  
      2. UT TRIGA ICS Manual (Parts 1,2,3, and 4)  
      3. Interlocks and SCRAM functions (MAIN-1)  
      4. NM1000 Wide Range Channel (UT Installation)  
      5. NPP1000 NP1000 Safety Channel (UT Installation)  
      6. AIO16 Board Alignment (Keithley) (UT Installation) 
      DAS16 programs: INSTALL, QBCAL, QBCALF, QBCALG, QBCALGA

II. PROCEDURE
-------------

.. _main-2.ii.a:

A. Introduction
~~~~~~~~~~~~~~~

   Log all console operation for diagnostic work, maintenance, surveillance, calibration and test with the password MIRAGE.

   1. Review calibration or functional check requirement. Follow instructions of each of the following sections. Refer to Maintenance Manuals if necessary for adjustments.

   2. Discontinue operation if any procedure is not successful. Correction of all failures is necessary to continue routine operation.

   3. Run pre-start checks to verify operable conditions. Review surveillance results. Approval of the data by the reactor supervisor is necessary to continue operation.

   4. File procedure records and pre-start checklist. Initial and date calibration check tag. Tag location should be on key ring with magnet key.

   5. Return to normal operation.

   Technical Specification references for the instrument systems are:

   +---------+------------------+-------------------------------------------------+-----------------------------+
   | Section | Steps            | Description                                     | TS requirement              |
   +=========+==================+=================================================+=============================+
   | B       |                  | Magnet Power Supply:                            |                             |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 1-3              | Monitor magnet power supply levels              |                             |
   |         |                  | Note: Test of trip operation not done here      |                             |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 4-5              | Monitor shorts of magnet power supply lines     |                             |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | See MAIN1        | Calibration (analog adjustment and trip test)   | 4.2.3 (3.2.3a-d)            |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | See MAIN1        | Calibration (no analog adj., circuit test only) | 4.2.3 (3.2.3d-f)            |
   +---------+------------------+-------------------------------------------------+-----------------------------+

   +---------+------------------+-------------------------------------------------+-----------------------------+
   | C       |                  | Fuel Element Temperature                        |                             |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 1-5              | Electrical function of TC junction sensor       |                             |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 6-9              | Temperature calibration of monitor circuit      | 4.2.4 (3.2.4a)              |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 10               | Trip set-point calibration of monitor circuit   | 4.2.3 (3.2.3a)              |
   +---------+------------------+-------------------------------------------------+-----------------------------+

   +---------+------------------+-------------------------------------------------+-----------------------------+
   | D       |                  | NM1000 Wide Range Channel:                      |                             |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 1-3              | Verify configuration status and power supplies  |                             |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 4-6              | Test calibration of counter operating modes     | 4.2.4 (3.2.4b)              |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 5 (c)            | Test Hi% power level trip set points            | 4.2.3 (3.2.3b)              |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 8-10             | Test HV power supply trip set points            | 4.2.3 (3.2.3c)              |
   +---------+------------------+-------------------------------------------------+-----------------------------+

   +---------+------------------+-------------------------------------------------+-----------------------------+
   | E       |                  | NP(P)1000 Power Safety Channels:                | 4.2.4 (3.2.4b)              |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 4-5              | Calibrate power level circuit                   | 4.2.4 (3.2.4b)              |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 6-7              | Calibrate trip power level trips                | 4.2.3 (3.2.3b)              |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 9                | Calibrate high voltage level trips              | 4.2.3 (3.2.3c)              |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 12,14,15-17,20   | Calibrate pulse power peak                      | 4.2.4 (3.2.4c)              |
   +---------+------------------+-------------------------------------------------+-----------------------------+
   |         | 13,14,18-19,20   | Calibrate pulse power integral                  | 4.2.4 (3.2.4d)              |
   +---------+------------------+-------------------------------------------------+-----------------------------+

.. _main-2.ii.b:

B. Magnet Power Supply
~~~~~~~~~~~~~~~~~~~~~~

   Refer to GA Operation and Maintenance Manual (E117-1004) for adjustments to the magnet supply circuits. See Volume 1, section 4, pages 38-41.

   1. Locate magnet power supply (DAC shelf 1).

   2. Connect voltmeter leads to the magnet power supply.

   3. Monitor console annunciation for magnet supply lo or hi voltage. Configuration set points for magnet supply voltage are 18 and 23 volts. ICS System monitoring of the magnet supply voltage uses a 4 to 20 mA signal.

      a. Measure as found magnet voltage.

      b. Adjust source voltage for low voltage detection (18.0 volts). Verify that the system detects low voltage. Record trip level.

      c. Adjust source voltage for high voltage detection (23.0 volts). Verify that the system detects high voltage. Record trip level.

      d. If signal levels are not correct (step b or c), then Check calibration of voltage to current conversion (4 to 20 mA module).
      
      e. Reset magnet supply voltage to 20.0 volts. Verify that the circuit detects no magnet supply problems.

   4. Test ground detection circuit. Trip is set to detect a 10 kilo-ohm short to ground. Check trip at Action Pak #16, LED will indicate status of trip.

      a. Short the positive terminal of the magnet power supply. The short is to ground thru test potentiometer set to 9 kilo-ohms. Verify console annunciation. If OK remove short, skip step 5.

      b. Short the negative terminal of the magnet power supply. The short is to ground thru test potentiometer set to 9 kilo-ohms. Verify console annunciation. If OK remove short.

   5. Adjust short detection trip levels. Readjust test potentiometer to 10 kilo-ohms. Apply shorts at magnet power supply terminals.

      .. line-block::
         a. Short positive terminal to ground thru test potentiometer.  
            Adjust Action Pack *span* potentiometer:  
               first CCW until the Hi trip LED is OFF,  
               then CW until the Hi trip LED is ON.  
            *Remove short.*

         b. Short negative terminal to ground thru test potentiometer  
            Adjust Action Pack *zero* potentiometer:  
            - first CW until the Lo trip LED is OFF,  
            - then CCW until the Lo trip LED is ON.  
            *Remove short.*

         c. Repeat steps a and b until no further adjustments are necessary.

         d. Repeat step 4 to verify console annunciations.

.. _main-2.ii.c:

C. Fuel Temperature Circuits
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Refer to GA Operation and Maintenance Manual (E117-1004) for adjustments to the fuel temperature circuit.

.. line-block::

   1. Record pool water temperature. Use control console status window.

   2. Mercury thermometers may not be used on the third level reactor platform.

   3. Do steps 4-10 for each fuel temperature channel, #1 and #2.  
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

      a. Set source input to simulate 0 °C (V = 0.0mV - Vref)  
         e.g., at 32 °C Vref is 1.285mV and V = -1.285mV.

      b. Verify continuous illumination of first LED of console bar graph.  
         Verify reactor console indicates 0 °C ± 2.

      c. Set source input to simulate 500 °C (V = 20.64mV - Vref).  
         Verify full scale indication (5th LED) on bar graph.  
         Verify reactor console indicates 500 °C ± 5.

   9. Verify the control console status box.

      a. Adjust source to represent 495 °C (V = 20.427mV - Vref).  
         Verify FT display box is black.

      b. Adjust source to represent 505 °C (V = 20.853mV - Vref).  
         Verify FT display box is red.

   10. Verify fuel temperature trip levels.

      a. Test module trip at 550 °C (V = 22.772mV - Vref).  
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

.. _main-2.ii.d:

D. NM1000 System Calibration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Refer to GA Operation and Maintenance Manual (E117-1000) for alignment of unit if adjustments are necessary.

Note: Some constants (*italics*) change at the time of a power calibration. Values shown are approximate.

   .. line-block::
      1. Verify values of data constants in processor stacks.  
         To display data press "Fn x",  
         where "n" is the stack tens digit and "x" is the ones digit.

   +--------------------+------------+
   | Computed Values    |            |
   +====================+============+
   | 10 percent power   |            |
   +--------------------+------------+
   | 11 percent power   |            |
   +--------------------+------------+
   | 12 period          | 100        |
   +--------------------+------------+
   | 13 period          | 100        |
   +--------------------+------------+
   | 14 mode            |            |
   +--------------------+------------+
   | 15 relay status    |            |
   +--------------------+------------+

   +----------------+---------+-------------------+----------+
   | Single Detector|         | Campbell Detector |          |
   +================+=========+===================+==========+
   | 20 DET counts  |         | 30 CMB Counts     | 120      |
   +----------------+---------+-------------------+----------+
   | 21 alpha offset| 0.00    | 31 noise offset   | -2.00E+02|
   +----------------+---------+-------------------+----------+
   | 23             |         | 33 Linear Factor  |3.70E-01  |
   +----------------+---------+-------------------+----------+
   | 25 DET pp const| 8.33E-8 | 35 CMB pp const   | 4.20E-08 |
   +----------------+---------+-------------------+----------+
   | 29 DET XOVR    | 1.20E+6 | 39 CMB XOVR       | 1.95E+03 |
   +----------------+---------+-------------------+----------+

   +----------------+---------+-------------------+-----------+
   | Trip Set-points|         | Operation Mode    |           |
   +================+=========+===================+===========+
   | 40 Lo Level    | 2.00E-7 | 50 Operation Mode | 0         |
   +----------------+---------+-------------------+-----------+
   | 41 Hi Level    | 1.08E+2 | 51 Fit Trip Mode  | Lo LVL    |
   +----------------+---------+-------------------+-----------+
   | 42 Float       | 1.00E-1 | 59 Version Number | 4.05      |
   +----------------+---------+-------------------+-----------+
   | 43 Rate        | 3.00E+0 |                   |           |
   +----------------+---------+-------------------+-----------+

   2. Check power supply test points for nominal values.

      +-------------------+---------------------+------------------------------+
      | Designation       | Preamplifier        | Microprocessor Test          |
      +-------------------+----------+----------+-------------+----------------+
      |                   | Test     | Common   |    Test     |  Common        |
      +===================+==========+==========+=============+================+
      | PS1 +15 volts     | +        | -        | TB1-1       | TB1-4          |
      +-------------------+----------+----------+-------------+----------------+
      | PS2 -15 volts     | -        | +        | TB1-8       | TB1-5          |
      +-------------------+----------+----------+-------------+----------------+
      | PS3 +5 volts      | +        | -        | TB1-12      | TB1-10         |
      +-------------------+----------+----------+-------------+----------------+
      | HVPS +800 volts   | HV       | Mon      | N/A         | N/A            |
      +-------------------+----------+----------+-------------+----------------+

   .. line-block::
      3. Clear all alarms.  
         Press keys "F7 9 0 ENTER".  
         Trips display at stack location 15 (F, L, H, R).  
         Keypad lamps A1 and A2 should be extinguished.

      4. Test Count Rate mode as directed in steps a-d.  
         **PA-15 discriminator is set for 0.1% (1.0 kilowatts) = 1.2 × 10⁶ cps.** 
         Compare stack 20 to expected test cps and stack 10 to expected power in each test.

         (Test cps - alpha offset) × count rate power constant = % Power  

         where:
            alpha offset: stack 21 = 0.0  
            count rate power constant: stack 25 = 8.33E-08

   +--------------+----------+----------------+----------+
   | Mode         | Stack 50 | % Power Expect | Test cps |
   +==============+==========+================+==========+
   | Counter LO   | 1        | 1.00E-5        | 120      |
   +--------------+----------+----------------+----------+
   | Counter MID  | 2        | 8.00E-4        | 9600     |
   +--------------+----------+----------------+----------+
   | Counter HI   | 3        | 2.84E-2        | 341000   |
   +--------------+----------+----------------+----------+

      .. line-block::
         a. Execute counter low test mode.  
            Press "F5 F8 1 ENTER".

         b. Note status of low power level trip in stack location 15.  
            Press "F1 5", letters F and L should display.

         c. Execute counter mid test.  
            Press "F5 F8 2 ENTER".

         d. Execute counter high test.  
            Press "F5 F8 3 ENTER".

   .. line-block::
      5. Test Campbell mode as directed in steps a-c.  
         **Detector DC current is set for ~1.2 amps at 90% (900 kilowatts).**  
         Compare stack 30 to expected test cps and stack 10 to expected power in each test.

         (test cps - noise offset) × Linear factor × Campbell power constant = % Power  

         where:
            noise offset: stack 31 = -200
            linear factor: stack 33 = 0.370
            Campbell power constant: stack 35 = 4.20E-08

   +--------------+----------+----------------+----------+
   | Mode         | Stack 50 | % Power Expect | Test cps |
   +==============+==========+================+==========+
   | Campbell LO  | 4        | 5.32           | 18300    |
   +--------------+----------+----------------+----------+
   | Campbell HI  | 5        | 112.25         | 84800    |
   +--------------+----------+----------------+----------+

         a. Execute Campbell low test.  
            Press "F5 F8 4 ENTER".

         b. Execute Campbell high test.  
            Press "F5 F8 5 ENTER".

         c. Note status of high power level trip in stack location 15.  
            Press "F1 5", letters L and H should display.

   .. line-block::
      6. Reset normal mode operation.  
         Press keys "F5 F8 0 ENTER".

      7. Wait 10 seconds, then clear all alarms.  
         Press keys "F7 9 0 ENTER".

      8. Connect digital multi-meter to high voltage test point:  
         HV Mon, of the High Voltage Power Supply  
         (HV = HV Mon Reading × 100)

      9. Test under voltage trip and over voltage trip:

         a. Adjust HV ADJUST on power supply to 750 volts (7.50V at HV Mon).  
            Trip indicated by A1 and A2 lamps on keypad display.  
            Inspect stack location 60 (Press "F6 0 ENTER").  
            Press "F7 9 0 ENTER" to clear.

         b. Adjust HV ADJUST to 850 volts (8.50V at HV Mon).  
            - Repeat same checks as above.

      10. Adjust HV ADJUST for nominal 800 volts (8.00 at HV Mon).

      11. Clear all trips.  
         Press keys "F7 9 0 ENTER".

.. _main-2.ii.e:

E. NP(P)1000 Power Safety Channels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _main-2.ii.e.np1000:

.. _main-2.ii.e.npp1000:

   .. line-block::
      4. Check zero calibration

         a. Disconnect input signal to unit at J2.  
            Jumper U8 pins 8 & 9 (**NPP1000 unit only**).

         b. Measure voltage at test point 63.  
            Value should be less than ±100 micro-volts (Adjust R131).

         c. Measure voltage at test point 56.  
            Value should be less than ±100 milli-volts (Adjust R131).  
            NPP should be slightly negative, about -5 mV.

         d. Press manual reset button to clear trip conditions if necessary.  
            Remove jumper at U8 pins 8 & 9 (**NPP1000 unit only**).

         e. Measure voltage between test points 57(+) and 58(-).  
            Value should be 0.00 volts.  
            The sign of the voltage will depend on the lead placement (Adjust R120).  
            Verify CSC display and bar graph read 0%.

      5. Check full-scale calibration

         a. Apply current source at input connector J2.  
            - NP1000: 8.33E-4 amps (1.00E-03 amp = 120%; 10 volts)  
            - NPP1000: 5.00E-7 amps (6.00E-07 amp = 120%; 10 volts)

         b. Measure voltage at test point 63 and point 56.  
            Value should be 8.33 ± 0.05 volts DC  
            - **NP**: Adjust **R23 only**  
            - **NPP**: Adjust **R27 only** (Pulse Mode: Use R23 for pulse mode. See step 15.)

         c. Measure voltage between test points 57(+) and 58(-).  
            Value should be 8.33 ± 0.05 volts  
            The sign of the voltage will depend on the lead placement (Adjust R123).  
            Verify CSC display and bar graph read 100%.

         d. Remove current source.
            Repeat steps 4 and 5 if adjustments are necessary, if not proceed to step 6.

      6. Check trip calibrations

         a. Apply current at input connector J2.  
            Calibration current is 9.0E-4 amps (5.5E-7 NPP).

         b. Verify percent power (NV) trip LED illuminates.

         c. Decrease input current at J2.  
            Calibration current is 8.5E-4 amps (5.0E-7 NPP).

         d. Verify trip LED extinguishes.

      7. Check trip set-point calibration

         a. Connect voltmeter to TP56. Increase current at J2.

         b. Record channel trip current and voltage found at TP56.

         c. Trip should be at 8.75E-4 amps (5.25E-7 NPP). (Adjust R79)

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

.. _main-2.ii.e.npp1000.pulse:

Continue for **NPP1000 only**

   .. line-block::
      12. Zero alignment, NV

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

         a. Jumper U7 pin 1 to ground.  
            Short capacitor C30 with a clip lead.

         b. Measure voltage 0 ± 0.02V at test point 38.  
            Use test point 10 as reference ground.  
            Adjust R47 for minimum offset.

         c. *Remove jumper(s) in step 13a.*

      14. *Close switch S4-4.*  
         Calibrate circuit full-scale, NV and NVT.

      15. Calibrate peak power NV circuit

         a. Apply 1.0E-3 amps at input connector J2.

         b. Verify 10.00 ± 0.05 volts at test point 56 (Adjust R23).

         c. Verify 10.00 ± 0.05 volts at test point 59 (no adjustment).

      *Note: Operation of the RESET button with a one mA input current will not discharge C58 completely. The result is an incorrect voltage at test point TP59.*

      16. Calibrate full-scale peak power, NV signal output

         a. Remove connector at J4 if not already removed.

         b. Connect milliamp meter between TP60 (J4-22) and TP61 (J4-23).

         c. Set J2 input signal to 1.0E-3 amps.

         d. Remove input signal at J2.

         e. Depress reset switch.  
            Verify 4 milliamp output (Adjust R140).

         f. Depress reset switch again, then

         g. Connect input signal at J2.  
            Verify 20 milliamps output (Adjust R143).

         h. Repeat steps d thru g until no adjustment is necessary.

      17. Check full-scale peak power, NV drift

         a. Apply 1.0E-8 amps at input connector J2.

         b. Observe the drift rate between TP60 and TP61.  
            Verify rate does not exceed 0.1 volt per minute.

         c. Observe test point 38. Depress reset.  
            Drift rate should be less than 100 mV/min.

      18. Check full-scale integral power, NVT circuit

         a. Increase input to 1.0E-6 amp and depress reset switch.

         b. Verify ramp rate at TP38 should be 15 sec per volt (Adjust R42).

      19. Check full-scale integral power, NVT signal output

         a. Remove connector at J4, if not already removed.

         b. Connect milliamp meter between TP39 (J4-16) and TP40 (J4-17).

         c. Set J2 input signal to 1.0E-6 amps.

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

.. line-block::
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

   .. line-block::
      :ref:`Introduction <main-3.ii.a>`
      :ref:`Pool Water Level <main-3.ii.b>`
      :ref:`Pool Temperature <main-3.ii.c>`
      :ref:`Water Conductivity <main-3.ii.d>`
      :ref:`Primary Flow Rate <main-3.ii.e>`
      :ref:`Secondary Flow Rate <main-3.ii.f>`
      :ref:`Heat Exchanger Pressure sensors <main-3.ii.g>`

E. Attachments
~~~~~~~~~~~~~~

   .. line-block::
      1. Pool parameters
      2. Coolant flow rates
      3. Heat exchanger

F. Equipment, Materials
~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. ICS system keys  
      2. Multi-meter - Fluke 87 or  
      3. Multi-meter - Keithley 196  
      4. Multi-source - Keithley 263  
      5. Test instrument cables, probes, test resistors  
      6. Flexible plastic tubing and fittings  
      7. De-ionized water  
      8. KCl reference solution

G. References, Other Procedures
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. UT TRIGA Mechanical System Manual (Parts 1,2,3, and 4)  
      2. UT TRIGA ICS Manual (Parts 1,2,3, and 4)  
      3. Interlocks and SCRAM functions - MAIN-1  
      4. Pool Water System Surveillance - SURV-4

II. PROCEDURE
-------------

.. _main-3.ii.a:

A. Introduction
~~~~~~~~~~~~~~~

Log all console operation for diagnostic work, maintenance, surveillance, calibration and test with the password MIRAGE.

   .. line-block::
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
   | B       | 1-4    | Pool Water Depth              | 4.3.1b (3.3.1b)     |
   +---------+--------+-------------------------------+---------------------+
   | C       | 1-8    | Pool Temperature              | 4.3.1a (3.3.1a)     |
   +---------+--------+-------------------------------+---------------------+
   | D       | 2-4    | Water Conductivity            | 4.3.1c (3.3.1c)     |
   +---------+--------+-------------------------------+---------------------+
   | G       | 1-8    | Heat Exchanger Delta Pressure | 4.3.1d (3.3.1d)     |
   +---------+--------+-------------------------------+---------------------+

.. _main-3.ii.b:

B. Pool Water Level
~~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. Verify position of pool level indicator (scale).  
         Scale elevation (25.3 cm) is set at the tank equipment-mounting ring.

      2. Lift up *high-level* sensor float.  
         Verify float level and hi/lo alarm indication.

      3. Press down *low-level* sensor float.  
         Verify float level and hi/lo alarm indication.

      4. Depress each SCRAM float switch one at a time to *alarm-level*.  
         Verify float level and verify pool level SCRAM trip indication at CSC.

.. _main-3.ii.c:

C. Pool Water Temperature
~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. Remove pool bulk temperature sensor.

      2. Prepare ice water bath at 0 °C;  
         Prepare hot water bath at 100 °C with hot plate heater.

      3. CAUTION: Do not use a mercury thermometer in the pool area.  
         Do not take thermometer on third level platform.  
         a. Measure calibration temperatures with thermometer.  
         b. Place the RTD sensor in each water bath.  
         c. Record test water temperature, and console indication.

      4. Check the alarm set point by heating a solution of water.  
         Monitor water temperature and record alarm point.

      5. If console indications agree with both temperatures ±4 °C, go to step 8.

      6. Disconnect wire at pin 7 or 8 of AP5.  
         Connect ammeter to wire and AP5 (pin 7 to DMM+; pin 8 to DMM-).  
         a. Place temperature sensor (RTD) in ice bath, Measure current; adjust zero control on AP5 to 4 mA, (0 °C).  
         b. Place temperature sensor (RTD) in hot bath, Measure current; adjust span control on AP5 to 20 mA, (100 °C).  
         c. Repeat steps a and b until no further adjustments are necessary.

      7. Repeat steps 3 thru 5 if zero and/or span adjustments were required.

      8. Replace temperature sensor and reconnect all signal lines.  
         Record bulk pool temperature displayed on console.

.. _main-3.ii.d:

D. Pool Water Conductivity (Cell type: Titanium, cell constant is 0.1)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::

      1. Perform an electronic calibration with resistors. Two points (+0.5%):  
         13.33 kΩ → 7.5 mmho/cm → 0.133 mega-ohms/cm  
         00.10 M  → 1.0 mmho/cm → 1.000 mega-ohms/cm

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
         c. If reading is not correct, verify resistances, Then loosen setscrews of indicator dial and reposition dial.  
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

.. _main-3.ii.e:

E. Primary Flow Rate (Reactor Pool Water)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
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
            Remove the wire at the transmitter - terminal.  
            Connect ammeter + to - transmitter terminal.  
            Connect ammeter - to the loose transmitter wire.  
         e. The DAC does not process the primary flow signal.  
            A jumper module is present at DAC shelf location 1.  
            The jumper module replaces an Action Pak process module.

      7. Flow Transmitter Calibration (set zero)

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

.. _main-3.ii.f:

F. Secondary Flow Rate (Physical Plant Cooling Water)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
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
            Remove the wire at the transmitter - terminal.  
            Connect ammeter + to - transmitter terminal.  
            Connect ammeter - to the loose transmitter wire.  
         e. The DAC processes the secondary flow signal.  
            - A process module is present at DAC shelf location 2.  
            - Flow process module is an Action Pak #4440(-108).  
            - The process module is a flow square root extractor.  
            Connect ammeter in series with the flow square root extractor.  
            Remove signal line to pin 7 (-) and check the input to the wire. *(Output: 1-15V is present on signal line.)*

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

      a. Connect fitting and tygon tube to high side transmitter port. Fill tube with water to a level **110" (279.4 cm)**. Measure water level above the low-side vent port. The water level correlates to **600 gpm (37.8 lps).**
      b. Verify the low-side transmitter vent port is full of water. Momentarily open the cross valve until water leaks. Do not close vent at this time.
      c. Readjust high side level to **110 inches**, if necessary.
      d. Verify transmitter and root extractor signal outputs, Verify both signal outputs are **20 mA**, Verify **37.8 lps** at the console display. Use span set for adjustment of **20 mA** signal. Set output of transmitter first, then set output of root extractor.
      e. If either span or zero adjustments were necessary, Remove tygon tube from the high side vent port. Repeat steps 7 and 8 until no further adjustments are necessary.

      9. Return system to original configuration.

.. _main-3.ii.g:

G. Heat Exchanger Differential Pressure and Capsi-photochellic Calibration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. Close two 1/4-inch stainless steel valves on lines to the sensor.

      2. Remove both plugs on top of the sensor.

      3. Open the two valves to fill each port to the same level then close them.  
         Caution - Flow snubbers in flow lines slow response.  
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
   +------+---------+--------+
   | 2    | 55.36   | 140.6  |
   +------+---------+--------+
   | 5    | 138.4   | 351.5  |
   +------+---------+--------+

   .. line-block::
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

   .. line-block::
      1. Compare heat-exchanger inlet temperatures.  
         a. Observe inlet temperature at local gauge.  
         b. Observe inlet temperature at CSC console.

      2. Compare heat-exchanger outlet temperatures.  
         a. Observe outlet temperature at local gauge.  
         b. Observe outlet temperature at CSC console.

      3. If each temperature in steps 1 and 2 is within ±4 °C skip step 4.

      4. Calibrate temperature circuit following procedure for bulk pool sensor.  
         (See section IIC, page 5 of this procedure).

MAIN-4 Area Radiation Monitor Systems
=====================================

I. INTRODUCTION
---------------

A. Purpose
~~~~~~~~~~

   .. line-block::
      This procedure describes the operation, maintenance and calibration requirements for the installed radiation monitors that consist of:
      - Area Radiation Monitors
      - Particulate CAM
      - Gas CAM
      Three functional criteria for the procedure are:
      (1) Verify the condition of the radiation monitoring system meet the minimum requirements of the License Technical Specifications.
      (2) Verify the condition of the radiation monitoring system meet the broader quality assurance requirements of the system design.
      (3) Assure NO task or action of this procedure is a proposed change, test, or experiment in the sense of 10CFR50.59

B. Description
~~~~~~~~~~~~~~

   The radiation monitor system is strategically positioned in the reactor facility. It provides a constant indication of radiation levels in the area, both locally and remote in the control room. Alarm functions can be set for each unit; the alarms sounds locally and in the control room.

   The Particulate CAM operates continuously to sample the air in the reactor room. Air is drawn through a filter paper where radioactive particles are trapped and counted. Dual alarm set points provide visual and audible alarms.

   The Gas CAM provides monitoring of the air being exhausted from the top of the reactor pool during reactor operations. It is designed primarily for detection of the noble gas portion. Alert and alarm set points provide indication of abnormal conditions.

C. Schedule
~~~~~~~~~~~

   Schedule procedure twice each year, at six month intervals for those monitors that are required by Technical Specifications and annually for additional monitors.

D. Contents
~~~~~~~~~~~

   .. line-block::
      :ref:`A. Normal Operations <main-4.ii.a>`
         1. Radiation Monitors  
         2. Particulate CAM  
         3. Gas CAM  

      :ref:`B. Response Checks <main-4.ii.b>`
         1. Radiation Monitors  
         2. Particulate CAM  
         3. Gas CAM  

      :ref:`C. Particulate Filter Replacement <main-4.ii.c>`
         1. Particulate CAM  
         2. Gas CAM  

D. Calibration Requirements  
~~~~~~~~~~~~~~~~~~~~~~~~~~~

E. Attachments *(not part of this procedure but may be useful)*  
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. note::
      Attachments are not part of this procedure but may be useful when performing this procedure.

   .. line-block::
      1. Weekly/Monthly
      2. Gas CAM Annual
      3. Particulate CAM Annual

F. Equipment, Materials  
~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. Appropriate calibration sources  
      2. Appropriate filter papers  

G. References, Other Procedures  
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. ANSI N323  
      2. Radiation Monitor Manual  
      3. Particulate CAM Manual  
      4. Gas CAM Manual  
      5. OPER-6 Reactor Bay Systems

II. PROCEDURE
-------------

.. _main-4.ii.a:

A. Normal Operations
~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. Radiation Monitoring System
      The Radiation Monitor System operates continuously and requires no operator actions.
      System server display in control room should provide system status for each monitor.

      2. Particulate CAM System
      The Beta Monitor operates continuously and requires no operator actions.
         a. Check main Power switch is ON.  
         b. Check air pump switch is ON.  
         c. Check AUDIO switch is ON.  
         d. Check that a filter is in place.  
            Filters are typically replaced weekly, or as necessary for special conditions.  
         e. Check that the MON light is on at least 50% of the time.  
            Backgrounds of 30 cpm should keep the monitor light on 90% of the time.  

      3. Gas CAM System
      The Gas Monitor System primarily operates continuously and should be verified operating prior to daily reactor operations.
         a. Ensure system lineup is per manufacturer manual.

.. _main-4.ii.b:

B. Response Checks
~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. Radiation Monitor System (weekly)
         a. Verify that system is operating correctly by verifying status for each detector that is on line. Ensure minimum required per Technical Specifications are met.

      2. Particulate CAM System (weekly)
         a. Remove the filter assembly.  
         b. Replace the filter medium.  
         c. Place the check source flush with the filter assembly opening.  
         d. Observe instrument and remote CSC display indicate ~4000 cpm.  
         e. Replace the filter assembly; check for normal airflow ~65 lpm.  
         f. Check pump exhaust filter.

      3. Gas CAM System (weekly)
         a. Replace air filter per manufacturer's procedure.

.. _main-4.ii.c:

C. Particulate Filter Replacement
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. note::
      These filter replacement procedures shall not be used if the filter replacement is due to an alert or alarm. Refer to OPER-5.

   .. line-block::
      1. Particulate CAM
         a. Turn the pump switch to OFF.  
         b. Lift the filter holder catch knob. Pull the holder out of the sampling chamber.  
         c. Remove the filter hold-down cap and pull the filter paper off.  
         d. Install new filter paper (fine side facing toward detector) and replace the hold-down cap.  
         e. Lift the holder catch knob and insert the filter holder. Ensure catch drops behind holder.  
         f. Restart airflow pump and ensure proper flow rate.

      2. Gas CAM System
         a. Follow procedure posted on equipment or in manufacturer manual.

.. _main-4.ii.d:

D. Calibration Requirements
~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. The instruments covered by this procedure shall be calibrated per Technical Specification requirements.  
      2. The calibration will be conducted per equipment's operation manual.

MAIN-5 Fuel Inspection and Measurement
======================================

INTRODUCTION
------------

A. Purpose  
~~~~~~~~~~

   The purpose of this procedure is to monitor for physical changes to the fuel elements. The main functional criterion for this procedure is to verify that the physical condition of fuel elements meets the minimum requirements of the License Docket 50-602 Technical Specifications.

B. Description  
~~~~~~~~~~~~~~


   Physical changes of a fuel element indicate the possible occurrence of stress on the cladding. A change in fuel phase with different temperatures, thermal expansion, or fracture of individual fuel pieces can occur to a varying degree depending on the fuel element operating history. A significant change in element length could indicate fuel element components expanding enough to fill the fission product gas gap placing stress on the end fitting welds. Cladding damage may allow the escape of fission products. The most common fuel element problem is localized swelling that may cause a bend of the fuel element such that the element will not fit through the reactor grid plate holes or be difficult to remove from the core.

C. Schedule
~~~~~~~~~~~

   Schedule completion of each procedure section at two-year intervals.

D. Contents
~~~~~~~~~~~

   .. line-block::
      PROCEDURE SECTION II. 
      :ref:`A. Inspect and Measure Standard Fuel Elements <main-5.ii.a>`  
      :ref:`B. Inspect and Measure Instrumented Fuel Elements <main-5.ii.b>`  
      :ref:`C. Inspect Control Rod and Fuel Follower Control Rod (FFCR) and Measure FFCR element <main-5.ii.c>`

E. Attachments
~~~~~~~~~~~~~~

   .. line-block::
      1. Fuel Inspection Summary  
      2. Fuel Element Log  

   .. note:: Attachments are not part of this procedure but may be useful when performing this procedure.

F. Equipment, Materials
~~~~~~~~~~~~~~~~~~~~~~~

   1. Fuel Inspection Stand  
   2. Reference Standard Fuel Element (SFE)  
   3. Reference Fuel Follower Control Rod (FFCR) Length Tube  
   4. Measurement Extension Rod  
   5. Probe Indicator (travel of 0" to 1" in increments 0.001" is typical)  
   6. Underwater Video Camera System  
   7. Fuel Handling Tool

G. References, Other Procedures
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
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

II. PROCEDURE
-------------

.. _main-5.ii.a:

A. Inspect and Measure Standard Fuel Elements
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. caution:: 
      Detectable amounts of particulate activity are associated with any abrasive contact with irradiated fuel elements. The fuel element handling tool and element measuring devices will have small amounts of removable radioactive particles.

   .. note::
      Inspection and measurement shall apply to all elements in the reactor core grid plate, but two to six spare SFE's should also be evaluated for future use.

   1. Prepare equipment and personnel for inspection tasks.
      a. Locate Previous MAIN-5 Fuel Element Measurement Records.
      b. Locate Fuel Moves Log and B159.xls to determine element serial numbers and locations.
      c. Setup underwater video camera system at the pool.
      d. Verify that a gamma sensitive survey instrument is present near the pool surface.

      .. caution:: 
         Lower surfaces of the inspection stand will have surface contamination. Contamination of 2000 to 10000 dpm/cm² can occur when fuel element cladding comes in contact with inspection stand components.

      e. Install fuel inspection stand in the pool.
         1) Secure inspection stand to side of pool (typically with C-clamps).
         2) Tie off all items that could potentially fall in pool.
      f. Mount probe indicator on the inspection stand.

   2. Calibrate probe indicator.
      a. Insert Reference Standard Fuel Element into the fuel inspection position of the inspection stand (i.e., not in the go/no-go gauge).

      .. note::
         Each of the upper fins of the Reference SFE have different reference positions for instrument calibration; this procedure uses only the lowest reference position.

      b. Lower the Measurement Extension Rod to the Reference SFE resting it at the lowest reference position (this is the 0.0" reference).
      c. Adjust the probe indicator mounting hardware such that the Measurement Extension Rod fits between the probe indicator pin and the Reference Fuel Element 0.0" reference.
      d. Ensure all probe indicator mounting hardware is tight.
      e. Adjust the position of the probe indicator so the probe indicator is near the middle of its travel range (approximately 0.5"), then set the indicator to zero (repeat as necessary).

      .. note::
         Adjusting the probe indicator to the middle of its travel range will allow measurement data for elements that are reported to be less than the reference in length.

      f. Remove and reinsert the Measurement Extension Rod to check for a consistent zeroed measurement on the probe indicator; re-adjust as necessary.
      g. Remove the Reference Fuel Element from the inspection stand.

   3. Inspect and Measure.

         .. note::
            SFE Series with 5-digit serial numbers are about 1 inch longer than previous SFEs. These elements, also known as ‘streamlined' or ‘torps', use the Reference SFE, but require a separate calibration setup and adjustment for zero. Plan inspections for minimal readjustment of inspection stand and probe indicator to maximize efficiency (i.e., do the ‘torps' separate).

         a. Place video camera assembly in pool for observation of element.

      .. caution:: 
         Raise fuel elements in the pool only as high needed to insert into the inspection stand, this will minimize personnel exposure from the irradiated fuel element.

      .. caution:: 
         Do not to bump or jar the inspection stand or probe indicator setup.

      b. Repeat probe indicator calibration step II.A.2 if inspection stand is disturbed, at the beginning of each measurement day, or if measurements appear to deviate consistently from previous results.
      c. Move each standard fuel element per FUEL-1 Movement of Fuel Procedure.
      d. Verify Element serial number etched or stamped on side of top flute
         1) Compare to Fuel Move Log and B159.xls file for the correct location and inspection information.
         2) If the fuel element is flagged as disqualified, remove the element from service.
         3) No additional inspection or measurement is needed for the failed element.
      e. Observe the surface and ends of the element for abnormalities.

         .. caution:: 
            Never force or drop a fuel element through the go/no-go gauge. To do so could damage the gauge, rupture the cladding, or jam the element in the gauge. To pass the bow and swelling test, the element should pass through the go/no-go gauge while being lowered to a seated position.

         .. warning::
            If there is evidence of fuel element damage that releases radionuclides to the confinement area at concentrations of greater or equal to 100 DAC, consult the Emergency Response Plan and PLAN-E for notification of unusual event.

         .. note::
            If the element becomes jammed in the gauge, attempt to remove it gently. If the element cannot be removed, contact the reactor manager.

         f. Check element diameter and bend by passing through the go/no-go assembly.

         .. note::
            The 15" fuel region should pass through gauge without significant binding.

         g. Record go/no-go results in Fuel Element Log.

      .. note::
         If the element passes freely through the gauge, it is within the allowable 1/16" (0.0625 in., 1.59 mm) bend tolerance.

      .. warning::
         If the element fails the go/no-go tolerance test, it has excessive bow or swelling and SHALL NOT be reinserted into the reactor core grid plate.

      h. If the element fails the go/no-go tolerance test, it does not meet the requirements of the License Technical Specifications.
         1) Remove the element from service.
         2) No additional inspection or measurement is needed for the failed element.
      i. If the element passes the go/no-go tolerance test, move the element to the fuel inspection position of the inspection stand.
      j. View the element with the camera (rotate the element as needed to view all surfaces) and note all significant defects (scratches, corrosion, bulges, pits, etc.) in the Fuel Element Log.
      k. If the element is found to have significant defects, it does not meet the requirements of the License Technical Specifications.
         1) Remove the element from service.
         2) No additional measurement is needed for the failed element.
      l. If the element passes the visual inspection, measure the element length (elongation) using the Measurement Extension Rod and previously zeroed probe indicator.

   .. note::Element length is a measure of difference from the Reference Standard Fuel Element measured in thousandths of an inch (0.001") and may be positive or negative.

         1) Make at least two measurements at one position on the fin.
         2) Using the inspection stand rotation mechanism, rotate the element approximately 120 degrees and repeat measurements.
         3) Rotate the element an additional approximately 120 degrees and repeat measurements.
         4) Record the largest reading in the Fuel Element Log for all measurements taken.

      .. caution:: 
         If a fuel element is found to have corrosion, mechanical damage, elongation of more than 1/10 in. over original length, or does not pass the go/no-go test, the fuel element SHALL NOT be reinserted in the reactor core grid plate.

      m. If element has elongation more than 1/10" (0.100", 2.54mm), it does not meet the requirements of the License Technical Specifications, remove the element from service.
      n. If measurement error is suspected:
         1) Re-measure the element while evaluating previous measurement history files and
         2) Troubleshoot for measurement problems or
         3) Recalibrate and
         4) Reevaluate element for service.
      o. Repeat calibration step II.A.2 after measuring approximately 10 fuel elements.

   4. Compare measurement data of each element to previous measurements to look for trends.

   5. Update B159.xls file.
      a. Fuel location data.
      b. Date of last inspection.
      c. Disqualified flag for any elements failing inspection.

   6. Update FUEL-1 required documents.

   7. Using proper contamination control techniques, remove fuel inspection stand and associated equipment from the pool and pool deck area if no further measurements are required.

.. _main-5.ii.b:

B. Inspect and Measure Instrumented Fuel Element (IFE)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. note:: 
      Inspection and measurement of IFE Series with 4- or 5-digit serial numbers are the same as SFEs, with the exception that the fuel handling tool will not be used for movement in the pool. Instead, the conduit pipe housing the thermocouple wires will be used to relocate the element to the inspection stand.

   .. caution:: 
      IFE thermocouple leads are subject to damage while relocating for fuel inspection. Inspect and repair any damaged lead insulation.

   .. note:: 
      The Reference SFE is the zero reference for IFE measurement.

   .. note:: 
      Inspection and measurement shall apply to all IFEs in the reactor core grid plate.

   1. Follow Procedure Section A. Inspect and Measure Standard Fuel Element for IFEs.

   2. Prior to returning to routine reactor operation, perform SURV-1 Fuel Temperature Calibration Procedure to verify proper operation of thermocouples.

.. _main-5.ii.c:

C. Inspect Control Rod and Fuel Followed Control Rod (FFCR) and Measure FFCR Element
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. note:: 
      Inspection and Measurement of FFCR Elements is the same as SFEs, with the exceptions that the fuel handling tool will not be used, the Reference FFCR Length Tube will be used instead of the Reference SFE, and the procedure will require removal of control rod drives. Inspection and Measurement shall apply to all FFCR Elements in the reactor grid plate. 

   .. note:: 
      The transient rod does not have any fuel and will only be visually inspected.

   1. Remove sufficient fuel from the core for minimum shutdown condition.

   .. warning:: 
      Minimum shutdown margin must be greater than 0.2% Δk/k, with removal of the two most reactive rods.

   2. Prepare equipment and personnel for inspection tasks.

      .. caution:: 
         Detectable amounts of particulate activity are associated with any abrasive contact with irradiated fuel elements. The fuel element handling tool and element measuring devices will have small amounts of removable radioactive particles.

      a. Locate Previous MAIN-5 Fuel Element Measurement Records.
      b. Locate Fuel Moves Log B159.xls to determine element serial numbers and locations.
      c. Setup underwater video camera system at the pool.
      d. Verify that a gamma sensitive survey instrument is present near the pool surface.

      .. caution:: 
         Lower surfaces of the inspection stand will have surface contamination. Contamination of 2000 to 10000 dpm/cm² can occur when fuel element cladding comes in contact with inspection stand components.

      e. Install fuel inspection stand in the pool.
         1) Secure inspection stand to side of pool (typically with C-clamps).
         2) Tie off all items that could potentially fall in pool.
      f. Mount the probe indicator to the inspection stand.

   3. Calibrate the probe indicator.

      a. Insert the Reference FFCR Length Tube into the fuel inspection position of the inspection stand (i.e., not in the go/no-go gauge).
      b. Lower the Measurement Extension Rod to the Reference FFCR Length Tube resting it on the edge of the tube.
      c. Adjust the probe indicator mounting hardware such that the Measurement Extension Rod fits between the indicator pin and the Reference FFCR Length Tube.
      d. Ensure all probe indicator mounting hardware is tight.
      e. Adjust the probe indicator position such that the probe indicator is near the middle of its travel range (approximately 0.5"); then zero the indicator (repeat as necessary).

      .. note:: 
         Adjusting the probe indicator to the middle of its travel range will allow measurement data for elements that are reported to be less than the reference in length.

      .. caution:: 
         The Measurement Extension Rod should be near vertical to avoid side effect error.

      f. Remove and reinsert the Measurement Extension Rod to check for a consistent zeroed measurement on the probe indicator.
      g. Remove Measurement Extension Rod and the Reference FFCR Length Tube from the inspection stand; re-adjust as necessary.

   .. caution:: 
      Remove only one control rod at a time. Reinstall each control rod prior to removal of another. Take care to NOT drop items into the pool.

   4. Remove rod drive from bridge mount.

      a. Transient Rod Drive
         1) Secure air pressure valve at top of pool.
         2) Release air pressure in rod drive.
         3) Remove drive cable at connector.
         4) Cut tie wraps securing cable to tube.
         5) Remove rod drive compressed air hose.
         6) Loosen bolts securing support frame to drive bridge.
         7) Lift support frame with overhead crane.
      b. Stepper Motor Drives
         1) Turn power OFF to rod drive translator.
         2) Remove rod drive cover housing.
         3) Disconnect motor power cable at drive motor unit.
         4) Locate rod down limit switch assembly.
         5) Remove limit switch actuator, spring, and washer.
         6) Remove four screws securing drive drawtube to pedestal.
         7) Lift drive drawtube assembly from the pedestal.

   .. caution:: 
      Damage to components may occur as the FFCR draw tube passes thru the deck plate penetration. Great care must be taken to prevent damaging drive switch actuator mechanism. Do not apply excessive torque on the FFCR during removal from the core.

   5. Move each FFCR element per FUEL-1 movement procedure.

   6. Remove control rod drive and control rod from core.

      a. Lift rod drive assembly until the bolts securing extension rod are accessible.
         1) The bolts secure the upper and lower sections of the extension rod.
         2) Lift rod drive assembly manually or with the overhead crane.

   .. caution:: 
      The regulating rod and shim rods are stainless steel with a fuel follower. These control rods will be highly radioactive.

      .. note:: 
         The transient rod may be removed from the pool for inspection, it is aluminum clad with no fuel follower.

      .. warning:: 
         Be careful to NOT drop bolts in the pool.

      b. Remove connecting bolts.
         1) Attach and use line (rope) as needed to lower the remaining section of extension rod and FFCR back down through bridge.
         2) Relocate control rod assembly in pool as necessary for inspection.
      c. Inspect extension rods, control rod, fuel follower, and connections.
         1) Look for evidence of wear, deterioration, or corrosion.
         2) Replace any suspect roll pins or connecting bolts.
         3) Photographs or x-rays should be made of suspect areas.

   7. Inspect and Measure

      .. caution:: 
         Raise fuel elements in the pool only as high as needed to insert into the inspection stand, this will minimize personnel exposure from the irradiated fuel element.

      .. caution:: 
         Do not to bump or jar the inspection stand or probe indicator setup.

      a. Place video camera assembly in pool for observation of element.
      b. Repeat probe indicator calibration step II.C.3 if inspection stand is disturbed, at the beginning of each measurement day, or if measurements appear to deviate consistently from previous results.
      c. Verify FFCR Element serial number etched or stamped on side of top flute
         1) Compare to Fuel Move Log and B159.xls file for the correct location and inspection information.
         2) If the fuel element is flagged as disqualified, remove the element from service.
         3) No additional inspection or measurement is needed for the failed element.
      d. Observe the surface and ends of the element for abnormalities.

      .. caution:: 
         Never force or drop a fuel element through the go/no-go gauge. To do so could damage the gauge, rupture the cladding, or jam the element in the gauge. To pass the bow and swelling test, the element should pass through the go/no-go gauge while being lowered to a seated position.

      .. warning:: 
         If there is evidence of fuel element damage that releases radionuclides to the confinement area at concentrations of greater or equal to 100 DAC, consult the Emergency Response Plan and PLAN-E for notification of unusual event.

      .. note:: 
         If the element becomes jammed in the gauge, attempt to remove it gently. If the element cannot be removed, contact the reactor manager.

      e. Insert FFCR element into the go/no-go gage.

      .. note:: 
         If FFCR element fits into the gauge without significant binding, then the element passes the go/no-go bend test.

      f. Record go/no-go results in Fuel Element Log.

      .. warning:: 
         If the element fails the go/no-go tolerance test, it has excessive bow or swelling and shall not be reinserted into the reactor core grid plate.

      g. If the FFCR element fails the go/no-go tolerance test, it does not meet the requirements of the License Technical Specifications.
         1) Remove the element from service.
         2) No additional inspection or measurement is needed for the failed element.
      h. If the FFCR element passes the go/no-go tolerance test, move the FFCR element to the fuel inspection position of the inspection stand.
      i. View the element with the camera (rotate the element as needed to view all surfaces) and note all significant defects (scratches, corrosion, bulges, pits, etc.) in the Fuel Element Log.
      j. Inspect the poison section of the FFCR and note abnormalities in the Fuel Element Log.
      k. If the element is found to have significant defects, it does not meet the
         requirements of the License Technical Specifications.
         1) Remove the element from service.
         2) No additional measurement is needed for the failed element.
      l. If the element passes the visual inspection, measure the element length (elongation) using the Measurement Extension Rod and zeroed probe indicator.

         .. note:: 
            FFCR length is a measure of difference from the Reference FFCR Length Tube measured in thousandths of an inch (0.001") and may be positive or negative.

         1) Take at least two measurements at one position on the fin.
         2) Using the inspection stand rotation mechanism, rotate the element approximately 120 degrees and repeat measurements.
         3) Rotate the element an additional approximately 120 degrees and repeat measurements.
         4) Record the largest reading in the Fuel Element Log for all measurements taken.

      .. caution:: 
         If a FFCR is found to have corrosion, mechanical damage, elongation of more than 1/10 in. over original length, or does not pass the go/no-go test, the FFCR SHALL NOT be reinserted in the Reactor core grid plate.

      m. If measurement error is suspected:
         1) Re-measure the element while evaluating previous measurement history files and
         2) Troubleshoot for measurement problems or
         3) Recalibrate and
         4) Reevaluate element for service.
      n. If element has elongation more than 1/10" (0.100", 2.54mm), it does not meet the requirements of the License Technical Specifications, remove the element from service.

   8. Compare measurement data of each element to previous measurements to look for trends.

   9. Inspection and measurement shall apply to all FFCR elements in the reactor core.

   10. Update B159.xls file.

      a. Fuel location data.
      b. Date of last inspection.
      c. Disqualified flag for any elements failing inspection.

   11. Update FUEL-1 required documents.

   12. Repeat FFCR element measurements with significant deviations from recorded history.

   13. Reinstall FFCR assembly by executing the removal steps in reverse order.

   14. Using proper contamination control techniques, remove fuel inspection stand and associated equipment from the pool and pool deck area at completion of FFCR inspection and measurement.

   15. Perform SURV-6 Rod Control Rod Calibration

      a. Control Rod Worth
      b. Control Rod Withdrawal, Insertion, and Drop Time Measurements

   16. Perform SURV-3 Excess Reactivity and Shutdown Margin.

   17. Review inspection results and rod worth prior to resuming routine reactor operation.

MAIN-6 Rod & Drive Maintenance, Inspection
==========================================

I. INTRODUCTION
---------------

A. Purpose
~~~~~~~~~~

   .. line-block::
      The purpose of Rod Drive Inspection and Maintenance activities is monitoring and maintaining
      the condition of control rod drives.

      Three functional criteria for the procedure are:  
      (1) Verify the conditions of the rod drives meet the minimum requirements of the License Tech. Specs.  
      (2) Verify the conditions of the rod drives meet the broader quality assurance requirements of the ICS system design.  
      (3) Assure no task or action of this procedure is a proposed change, test, or experiment in the sense of 10CFR50.59.

B. Description
~~~~~~~~~~~~~~

   Control rod drives must meet specific operation requirements for proper operation. Periodic inspections will identify potential problems by visual observation of physical conditions of the control rod and its drive system. Maintenance that corrects deficiencies found during an inspection or failure of the control to calibrate or operate correctly will return the control rod system to acceptable working status. Acceptable working status means the control rod system will operate, as its original design specifications require. All replacement parts for rod drive system maintenance shall meet or exceed the requirements of the original system installation.

C. Schedule
~~~~~~~~~~~

   Schedule procedure once each year. Refer to MAIN5 to complete the inspection of CFFRs. Plan procedure task for the month of January but no later than 15 months from previous work.

D. Contents
~~~~~~~~~~~

:ref:`A. General Instructions <main-6.ii.a>`
:ref:`B. Standard Rod Drive Inspection <main-6.ii.b>`
:ref:`C. Stepper Rod Drive Inspection <main-6.ii.c>`
:ref:`D. Transient Rod Drive Inspection <main-6.ii.d>`
:ref:`E. Control Rod Drive Test <main-6.ii.e>`

E. Attachments
~~~~~~~~~~~~~~

   Drive Inspection Summary

F. Equipment, Materials
~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. Transient rod and drive  
      2. Reg rod, drive and translator  
      3. Shim 1 rod and drive  
      4. Shim 2 rod and drive  

G. References, Other Procedures
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. SURV-6 Control Rod Calibration  
      2. OPER-6 Reactor Bay Systems  
      3. ICS Operation and Maintenance Manual, Chapters 5, 6 and 7  


II. PROCEDURE
-------------

.. _main-6.ii.a:

A. General Instructions
~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      Repair rod drive mechanism with the supervision of a senior reactor operator.

      1. Perform repair using available documents.  
         Refer to General Atomic procedures in supplied manuals as guidance.  
         Refer to drawings, circuit diagrams, and functional descriptions as guidance.

      2. Replace parts with identical part to the original part.  
         A substitute part shall have equivalent or superior specifications.  
         All substitutions shall meet the requirements of 10cfr50.59 and ADMN2.

      3. Execute steps necessary to qualify the system as operational.  
         Approve results of work prior to resumption of routine reactor operation.

.. _main-6.ii.b:

B. Standard Rod Drive Maintenance (Chapter 5)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   Standard rod drives are no longer in use; go to next section.

.. _main-6.ii.c:

C. Stepping Rod Drive Maintenance (Chapter 6)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::

      Perform the following actions for each non-pulse control rod drive:

      1. Remove rod drive cover.  
      2. Inspect mechanism for visual evidence of deterioration or component failure.  
      3. Observe operation of mechanical limit switches noting any abnormalities.  
      4. Verify that setscrews or locking nuts on switch actuators appear secure.  
      5. Replace rod drive cover.  
      6. Verify that bolts securing drive mechanism to bridge are secure.  

.. _main-6.ii.d:

D. Transient Rod Drive Maintenance (Chapter 7)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::

      Perform the following actions for the pulse rod drive:

      1. Inspect air supply line from drive to filter and regulator.  
      2. Check regulator filter.  
         Remove air pressure, clean or replace filter, restore air pressure.  
      3. Blow down regulator assembly and air surge tank near rod drive.  
         Blow down should remove liquid accumulations.  
      4. Check air hose for evidence of deterioration or leakage.  
      5. Check shock isolation mounts.  
      6. Verify bolts between drive mechanism and bridge are secure.  
      7. Verify power and signal cable plug connections are secure.  
      8. Inspect drive shock absorber and inside surface of cylinder.  
         a. Remove stainless steel shock absorber by rotation in clockwise direction.  
         b. Examine inside of drive cylinder using a light.  
         c. Clean with alcohol swab and check that cylinder is clean and smooth.  
         d. Coat cylinder interior walls with light application of silicone spray lubricant.  
         e. Replace shock absorber (hand tighten).  
      9. Inspect drive position threads and outside surface of cylinder.  
         a. If oxidation is apparent or if surface appears dirty,  
         b. Clean and coat cylinder exterior threads with lubricant.  
         c. Lubricant is a light coat of lubri-plate grease.  
         d. Lubricant serves as lubricant and rust preventative.  

.. _main-6.ii.e:

E. Rod Drive Test
~~~~~~~~~~~~~~~~~

   .. line-block::

      1. Refer to GA manual chapter 5, 6, or 7 for alignment of rod limit switches.  
      2. Perform operation test of rod (Refer to SURV6).  
         Measure rod drop time  
         Measure rod drive insertion and withdrawal times.  
         If transient control rod drop time is slower than normal,  
         a. Raise rod drive about five inches.  
         b. Lift piston about one inch by hand.  
         c. Apply silicone lubrication to bottom of piston guide. Access the guide thru slot in side of rod drive tube assembly.  
         d. Repeat rod drop tests.  
      3. Record the inspection result and successful completion of tests.  
         Refer to OPER6 for documentation of repairs (Reactor Maintenance Log).  
