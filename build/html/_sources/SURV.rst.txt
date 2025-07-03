====
SURV
====

SURV-1 Fuel temperature Calibration
===================================

I. PURPOSE
----------

   The purpose of this procedure is to verify that each thermocouple within an instrument fuel element is operable.

II. DISCUSSION
--------------

   Calibration of the fuel temperature monitoring system consists of two separate procedures.  
   This procedure demonstrates the function of the thermocouple sensors.  
   Procedures in MAIN-2 calibrate the electronic circuit with a DC voltage source equivalent to the thermocouple temperature response.  
   Standard reference tables document the temperature versus voltage response of the chromel-alumel type K thermocouple junctions.

   A temperature calibration must be done once each year.

III. REFERENCE
--------------

   .. line-block::
      MAIN-2  
      Type K reference data

IV. EQUIPMENT
-------------

   Galvanometer or microvolt meter

V. Instructions
---------------

   1. Verify one instrument fuel element is in the B or C ring.

   2. Disconnect thermocouple lead junctions at reactor bridge. Measure and record resistance between leads and between each lead and ground.

   3. Attach a millivolt measurement device and measure the junction voltage of each thermocouple. Use a reference junction in an ice bath.

   4. Convert thermocouple voltage to temperature and compare with bulk pool ambient temperature.

   5. Reconnect thermocouple leads. Confirm correct lead connections.

   6. Verify completion of ICS calibration for calibration, measurement and test of both fuel temperature channels.

   .. line-block::
      Type K reference junction
      NIST - monograph #125

SURV-2 Reactor Power Calibration
================================

I. INTRODUCTION
---------------

A. Purpose
~~~~~~~~~~

   The Reactor Thermal Power Calibration procedure determines the heat output of the TRIGA reactor by measurement of the change in the bulk pool water temperature.

B. Description
~~~~~~~~~~~~~~

   Accurate knowledge of the reactor power level depends on the total amount of water in the pool and several corrections.  
   The corrections adjust for conditions that cause the pool-reactor system to deviate from an adiabatic condition.  
   Power calibration depends on the pool constant that is a function of the pool water volume.  
   A change in volume equivalent to a 10-centimeter water depth will cause a 1.2% change in the pool constant.

C. Schedule
~~~~~~~~~~~

   A reactor thermal power calibration must be completed once each year.  
   Measurements should be done in July but shall not exceed longer than 15 months from preceding measurement.

D. Contents
~~~~~~~~~~~

   .. line-block::
      :ref:`A. Thermal Power Calibration Experiment <SURV-2.II.A>`
      :ref:`B. Thermal Power Evaluation <SURV-2.II.B>`
      :ref:`C. Power Instrumentation Adjustments <SURV-2.II.C>`

E. Attachments
~~~~~~~~~~~~~~

   *Note: Attachments are not part of this procedure but may be useful when performing this procedure.*

   .. line-block::
      1. Power Calibration Data
      2. Thermal Power Calibration check sheet

F. Equipment, Materials
~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      Temperature measuring system Example - RTD array  
      (Optional) Data acquisition Software  
      (Optional) Math software such as Mathcad

G. References, Other Procedures
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   GA Publication: "Power Calibration for TRIGA Reactors" by W.L. Whittemore, J. Razvi and J.R. Shoptaugh Jr. February 1988.

II. PROCEDURE
-------------

.. _SURV-2.II.A:

A. Thermal Power Calibration Experiment
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   Routine thermal power calibrations should be done at or near full power. Typically performing the calibration at 900 kW indicated is preferred so as to maintain some margin below the scram set points. If a major core reconfiguration was made, several calibrations at stepwise increasing powers of about 300 kW, 600 kW, and then 900 kW should be performed.

   1. Install or verify installed pool water temperature measurement system near center of pool.  

      .. note::
         Example of measurement system - RTD array points are at depths of 1.2 and 3 meters. Use average of readings.

   2. Ensure temperature measurement systems are working properly.

   3. Record air and shield temperatures.

      a. Room air temperature (approximate measurement point): At pool railing 1 m above pool deck, south rail.  
      b. Shield concrete temperature (approximate measurement point): In conduit near shield surface at level 2 under NM

   4. Adjust pool depth to 8.10 meters with bulk pool temperature at approximately ~20°C.

   5. Install pool stirrer mechanism into the reactor pool and secure with safety line. Initiate operation of the stirrer.

   6. Sub-cool pool using coolant system to target based on desired reactor power. Target temperature should result in the average of the pool temperature prior to start of the calibration and the final pool temperature after the conclusion of the power part of the experiment to equal the measured shield temperature.

      Example: T(pool ambient) - T(target Δ/2) = T(sub cool)

   7. Secure operation of pool purification and coolant pumps. Close pool water and purification isolation valves.

   8. Close pool surface argon purge valve.

   9. Turn off pool lights.

   10. Wait 1 hour after securing systems and sub-cooling pool water. Take 3 pool water temperatures 5 minutes apart after stabilization. Record these on Power calibration data sheet.

   11. Complete reactor startup checks including electronic Pre-start checks.

   12. Initiate logging of reactor power indications on all 3 power monitoring channels at 2 minute intervals.  

   13. Operate reactor at 900 kW or target power for 30 minutes. Power level is to be measured by NPP channel.

      a. The operation mode for startup should be manual.
      b. Startup rate should be equivalent to a 20-second period.
      c. Record at power time (to nearest tenth of a minute).
      d. Observe NPP channel to control power level.
      e. Shift to auto mode when at 900 kW or target power.

   14. Continue recording pool temperature data during time at power at 1 minute interval.

   15. Shutdown Reactor by manual scram at end of 30 minutes and record scram time.

   16. Continue to record pool temperatures for 60 minutes after shutdown at 1 min intervals.

   17. Return pool conditions to normal operating conditions.

   18. Complete shutdown checklist.

.. _SURV-2.II.B:

B. Thermal Power Evaluation
~~~~~~~~~~~~~~~~~~~~~~~~~~~

   1. Calculate power using the slope method based on the time rate of temperature changes during the at power portion of the run. Use least squares fit of temperature data to determine the slope at constant power.  

      .. note::
      
         20.74°C/MW·HR is NETL TRIGA II constant. Divide by 2 for 30 minutes run and multiply by %MW. 
         Example: (20.74°C/MW·HR / 2) x 0.9 = 9.33°C change in temperature. 
         This is what you should expect to see for a 30 minute run at 900 kW.

   2. Verify pool calibration by temperature change from initial time power reached to 30 minutes at power for each temperature system used.

      a. Calculate pool temperature when power reaches desired power level.
      b. Calculate pool temperature 30 minutes at desired power.
      c. Calculate the total temperature change during constant power production.

   3. Compare results of slope method and temperature methods. Comparison of the two temperature analysis methods should be within 2% of each other.

   4. Compare current data with data from previous calibrations.

      a. Water, air and concrete, temperatures prior to power level test
      b. Initial pool temperature at startup.
      c. Final pool temperature at shutdown
      d. The reactor operation time and power level indication.

   5. Thermal power measurement accuracy should be ≤ 5%. Measurement errors should be less than 5% at one standard deviation.

.. _SURV-2.II.C:

C. Power Instrumentation Adjustments
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   1. Senior reactor operator shall approve acceptance or adjustment of power channels. All power channels should read within 2% of the calculated thermal power.

   2. Adjust each chamber indication to the value of the thermal power test.

      a. Instrumentation power channels shall be adjusted to within 2%.
      b. Adjust detector chamber position with reactor in manual mode only.

   3. Adjustment of the NP and NPP should be by movement of detector position.

   4. Adjustment of the NM is typically by change of only the digital calibration constants. If a large NM adjustment is required the chamber should be repositioned following the same procedures used for initially setting up the channel, including positioning the chamber to read the specified current followed by setting the digital constants.

   5. If adjustment of the NM digital constants was required, the calibration signal potentiometers in the Campbell amplifier may require adjustment to allow the prestart checks Mode 4 and 5 to pass and the shutdown crossover should be observed to verify a smooth transition. Refer to initial channel set up procedures if adjustments are required.

   6. Repeat procedure if the calibration requires more than a 10% adjustment between thermal power calculation and any power channel. Apply power calibration comparison to each power chamber (NM, NP. & NPP).

   7. Reevaluate pool constant if there is any significant change of pool water volume. A significant change may occur if the mass of other materials in the pool changes.

SURV-3 Excess Reactivitiy and Shutdown Margin
=============================================

I. INTRODUCTION
---------------

A. Purpose
~~~~~~~~~~

   The purpose of this procedure is to ensure the excess reactivity and shutdown margin meet the requirements for normal and maintenance operations.

B. Description
~~~~~~~~~~~~~~

   This procedure ensures that the reactor operates in a safe condition in respect to the Technical Specifications requirements.  
   Excess reactivity and Shutdown Margin directly relate to reactor safety by defining the available control capability of the reactor.

C. Schedule
~~~~~~~~~~~

   This procedure MUST be conducted once a year, not to exceed 15 months.  
   Measurements SHOULD be conducted after major core changes or excessive burnup.

D. Contents
~~~~~~~~~~~

   .. line-block::
      :ref:`A. Requirements <SURV-3.II.A>`
      :ref:`B. Calculate Shutdown Margin and Excess Reactivity for Normal Operations <SURV-3.II.B>`
      :ref:`C. Calculate Shutdown Margin for Rod Maintenance <SURV-3.II.C>`

E. Attachments
~~~~~~~~~~~~~~

   .. note::
      Attachments are not part of this procedure but may be useful when performing this procedure.

   1. Shutdown Margin and Excess Reactivity Calculation Sheet

F. Equipment, Materials
~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      Reactor Core system  
      Reactor Pool system  
      Instrument Control and Safety System

G. References, Other Procedures
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      Docket 50-602 Technical Specifications  
      TRIGA Control Rod Calibration  
      Reactor Core Load Configuration

II. PROCEDURE
-------------

.. _SURV-3.II.A:

A. Requirements
~~~~~~~~~~~~~~~

   1. Verify the reactor core is in a cold clean critical condition.  

      a. Check logbook for previous operation history.  
      b. No power operations above 10 kW in past 3 days.  
      c. Remove all experiment facilities. If removal is not possible, compensate in calculations.

   2. Perform a routine pre-start check.

.. _SURV-3.II.B:

B. Calculate Shutdown Margin and Excess Reactivity for Normal Operations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   1. Conduct a routine Startup to 50 watts. Bank all rods.

   2. Calculate reactivity for each rod position using the most current Rodworth curves.

      +----------+-----------+-------------------+
      | Rod      | Position  | Reactivity (S)    |
      +==========+===========+===================+
      | Transient|           |                   |
      +----------+-----------+-------------------+
      | Shim 1   |           |                   |
      +----------+-----------+-------------------+
      | Shim 2   |           |                   |
      +----------+-----------+-------------------+
      | Reg      |           |                   |
      +----------+-----------+-------------------+
      |          |  Total    |                   |
      +----------+-----------+-------------------+

   3. Determine if Shutdown Margin meets technical specification  
      (Minimum > 0.2% Δk/k = $0.29).  

      Value determined in Step 2 - Most reactive rod > 0.2% Δk/k ($0.29)

      .. note:: 
         Ensure you compensate for any experiments remaining in core.

   4. Determine if excess reactivity meets Technical Specification (Max < 4.9% Δk/k = $7.00)

      Total Rodworth of all rods - Value determined in Step 2 < 4.9% Δk/k ($7.00)

.. _SURV-3.II.C:

C. Calculate Shutdown Margin for Rod Maintenance
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   1. Remove fuel estimated to decrease reactivity enough to meet the reactivity of the second most reactive rod.

   2. Conduct a routine Startup to 50 watts. Bank all rods.

   3. Calculate reactivity for each rod position using the most current Rodworth curves.

      +----------+-----------+-------------------+
      | Rod      | Position  | Reactivity (S)    |
      +==========+===========+===================+
      | Transient|           |                   |
      +----------+-----------+-------------------+
      | Shim 1   |           |                   |
      +----------+-----------+-------------------+
      | Shim 2   |           |                   |
      +----------+-----------+-------------------+
      | Reg      |           |                   |
      +----------+-----------+-------------------+
      |          |  Total    |                   |
      +----------+-----------+-------------------+

   4. Determine if Shutdown Margin meets specification (Minimum > 0.2% Δk/k = $0.29).

      Value determined in Step 2 - (Most reactive + 2nd most reactive rod) > 0.2% Δk/k ($0.29)

      .. note:: 
         Ensure you compensate for any experiments remaining in core.

   5. If value does not meet Technical Specification for Shutdown Margin, remove fuel to compensate for removal of remaining amount of reactivity and repeat Steps 2 through 5 as necessary.

SURV-4 Reactor Water Systems Surveillance
=========================================

I. PURPOSE
----------

   This procedure details weekly, monthly, and annual surveillances of reactor water system parameters.  
   Periodic reviews of system operation are intended to identify abnormal parameters or deteriorating characteristics so that corrective or repair actions can be taken.

II. DISCUSSION
--------------

   The reactor water system consists of three subsystems which must function properly for reactor operation. The three systems are the the purification loop, the coolant loop, and the reactor pool.
   Periodic checks of the pool system verify that pool water level is acceptable, no water leakage is evident, no foreign materials are introduced, all instrumentation is working properly, and no system hardware has failed or been damaged.
   Purification system periodic checks verify acceptable water purity (conductivity and pH), water flow rate, and performance of filter and ion exchange bed.
   Coolant system periodic checks verify proper operation of pumps, heat exchanger, controls, and pressure/flow monitoring instrumentation.

III. REFERENCE
--------------

   .. line-block::
      1. Docket 50-602 SAR  
      2. NETL Operations Manual Part 1, Section 9  
      3. GA UT TRIGA Mechanical Operation and Maintenance Manual Part 7  
      4. MAIN-3 Calibration and Function Checks of the ICS System Support Features  
      5. Reactor Water Systems, Operation Procedure, OPER-4

IV. CONTENTS
------------

   .. line-block::

      Surveillance Procedure
      :ref:`Weekly Checklist Instructions <SURV-4.II.A>`
      :ref:`Monthly Checklist Instructions <SURV-4.II.B>`
      :ref:`Annual Checklist Instructions <SURV-4.II.C>`

V. PROCEDURE
------------

   .. line-block::
      Perform **weekly checks** (Section A) of operable systems within 10 days of the previous check.  
      Perform **monthly checks** (Section B) of operable systems within 6 weeks of the previous check.  
      Perform **annual checks** (Section C) of operable systems within 15 months of the previous check. The annual checklist must include the comletion of the procedure in reference (4).

   If a water system is inoperable at the schedule time, the appropriate checks are to be done when the system status changes to operable. 

.. _SURV-4.II.A:

A. Weekly Checklist Instructions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   1. Pool System

      a. Inspect pool surface for abnormal deposits. Clean appearance of entire pool surface for deposits or accumulation of material. If surface is not clean check water skimmer, adjust and clean water skimmer to control surface deposits.
      b. Record bulk pool temperature, fuel temperature, and level. Verify fuel temperature is similar to past temperature.
      c. Replace pool water evaporation losses with makeup supply of deionized water. Record start level, stop level, and fill volume for reactor pool. Normal pool level is 8.10 ± 0.05 m.
      
         i.  Connect makeup supply line and open makeup water supply valves when the pool level is near or below the 8.05 meter level.
         ii. Verify makeup water system conductivity lamps illuminate during fill.
         iii. Close makeup water supply valves when the pool level reaches the 8.15 meter level, disconnect and cap makeup supply line.
         iv. Multiply pool level change by 49.4 l/cm to obtain volume change in liters.

   2. Purification System

      a. Check inlet/outlet conductivity at demineralizer.
      b. Check system flowrate 22-38 lpm (6-10 gpm) and pressure drop across filter 84-168 kPa (12-24 psi). Adjust flow control valve to compensate for increase in filter pressure drop.
      c. Check operation of skimmer. Remove debris accumulations.

   3. Coolant System

      No routine weekely surveillance is necessary for coolant water system operation.

.. _SURV-4.II.B:

B. Monthly Checklist Instructions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   1. Reactor Pool System  

      a. Check position of purification and coolant system suction and discharge lines. Siphon break holes in suction and discharge lines above the 7.60 meter level protect against accidental pool water loss. Suction lines should not extend below the 6.30 meter level. 
      b. Inspect pool by visual observation. Check for presence of improper materials and evidence of deterioration or damage to pool liner including beam penetrations. 
      c. Measure pool pH using low ion pH paper or equivalent.  
      d. Inspect overflow drains for blockage and acceptable discharge area. Inspect the seal between the pool liner and concrete shield for damage. Repair any damage with acceptable material.  
      e. Inspect pool covers and acrylic liners for evidence of damage; repair or replace acrylic if necessary.  
      f. Test Pool Level Sensor. Mechanically displace level floats and check for appropriate abnormal level indications, and scram indications.  
      g. Inspect accessible beam ports (do not remove covers or experiments) for evidence of moisture and pool leakage.  
      h. Review pool water makeup volumes.  
      i. Take 20 ml pool water sample at two month intervals (odd months) perform gross alpha/beta count, record results on checklist.
      j. Take 20 mL fuel storage well sample from wells containing fuel at the month intervals (even months)

   2. Pool Purification System

      a. Review conductivity; change resin > 2 μmho/cm (RWP required)  
      b. Check flowmeter/differential pressure; replace filter < 22 lpm  
      c. Check pump seals and piping for leaks

   3. Pool Coolant System

      a. Startup coolant system. Adjust temperature controller setpoint 5.5°C (10°F) below pool temperature. Allow readings to stabilize and record local readings. Review current readings with respect to previous data for trends of system deterioration.
      b. Check primary and secondary pump seals for evidence of leakage.
      c. Shutdown system and return temperature setpoint to initial setting, 18.3°C (65°F).

.. _SURV-4.II.C:

C. Annual Checklist Instructions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   1. Reactor Pool System

      a. Verify pool level and pool temperature checks are complete (per procedure in Reference 4).
      b. Test Bulk Pool Temperature Sensor. Place temperature probe in hot water bath and verify alarm at ≤48°C (118°F).
      c. Test low pool level alarm signal circuit to security. Notify security of intended test, mechanically displace float, verify security alarm indication.
      d. Test pool radiation alarm signal circuit to security. Notify security of intended test, alarm pool radiation monitor using source, verify security alarm indication.
      e. Remove covers from beam tubes without experiments and check for evidence of water or moisture. Inspect beam tubes with experiments for indications of water leakage or corrosion. A review of each experiment installation should be made each 2 years to determine whether to inspect the beam tube.
      f. Check operation of beam tube shutter control rod isolation valves and beam tube purge isolation valves. Operation should require minimal effort.
      g. Take 500 ml pool water sample: Prepare sample for gamma spectroscopy analysis by evaporation or use a standard geometry configuration. Perform gamma spectroscopy analysis. Attach results to checklist.

   2. Pool Purification System

      a. Verify conductivity cell calibration are complete (per procedure in Reference 4).
      b. Inspect piping from purification skid to pool suction and discharge for damage. Check pipe supports.
      c. Inspect makeup water system piping for leakage or damage.

   3. Pool Coolant System

      a. Verify flow, differential pressure and temperature instrumentation calibration (per procedure in Reference 4). Check local pool water and chilled water instrumentation readings with system shutdown (not operated in past 48 hours). Check pressures for values typical of hydrostatic head in the pool water piping and typical of blending station pressures on the chilled water system. Temperatures in both systems should be approximately in equilibrium with ambient room temperature.
      b. Start coolant system and check whether local values agree with remote readings.
      c. Inspect piping from coolant transfer room to pool for damage. Check pipe supports.

SURV-5 Air Confinement System Surveillance
=============================================

I. INTRODUCTION
---------------

A. Purpose
~~~~~~~~~~

   This procedure details monthly and annual surveillance of the air confinement system parameters. Periodic reviews of system operation are intended to identify abnormal parameters or deteriorating characteristics so that corrective or repair actions can be taken.

B. Description
~~~~~~~~~~~~~~

   The air confinement system encloses the reactor bay. An HVAC system, argon purge system, fume/sort hood, access doors and construction joints provide the pathways for air flow into and out of the reactor bay. Periodic checks of the reactor room boundary and door weather-strip determine the condition of the most significant leakage paths. Less significant leakage paths, such as construction joints, should be examined at the time of maintenance or repair to any joint. HVAC system periodic checks verify that the system components necessary for control of reactor bay negative pressure, isolation damper closure, fan shutdown, and acceptable exhaust stack velocity are functioning properly. Argon purge system periodic checks verify that the fan, pre-filters, HEPA filters, valves, and associated control system components are functioning properly. Fume/sort hood checks verify exhaust duct isolation dampers are functioning properly.

C. Schedule
~~~~~~~~~~~

   Measurements of the reactor room air confinement system must be done monthly and annual intervals. Functional checks are done monthly intervals. Annual calibration measurements should be done in October but shall not exceed longer than 15 months from preceding measurement.

D. Contents
~~~~~~~~~~~

   .. line-block::
      :ref:`A. Confinement System Inspection <SURV-5.II.A>`
      :ref:`B. Monthly Check Instructions <SURV-5.II.B>`
      :ref:`C. Annual Check Instructions <SURV-5.II.C>`

E. Attachments
~~~~~~~~~~~~~~

   .. line-block::
      Monthly Checklist
      Annual Checklist

F. Equipment, Materials
~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      Check Source  
      UT TRIGA Facilities

G. References, Other Procedures
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      1. Docket 50-602 SAR  
      2. OPER-5, Air Confinement System, Operation Procedure  
      3. Fume/Sort Hood Operating Procedure  
      4. NETL Operations Manual Part 1, Section 9  
      5. GA UT TRIGA Mechanical Operation and Maintenance Manual Part 7  
      6. MAIN-3, ICS System Support Features

II. PROCEDURE
-------------

.. _SURV-5.II.A:

A. Confinement System Inspection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   1. Perform monthly checks (Section B) of operable systems within 6 weeks of previously scheduled check.
   2. Perform annual checks (Section C) of operable systems within 15 months of previously scheduled check.

   If confinement system is inoperable at the schedule time, the appropriate checks are to be done when the system status changes to operable.

.. _SURV-5.II.B:

B. Monthly Check Instructions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   The monthly isolation test of the HVAC, Argon Purge, and Fume/Sort hood in this section should be done concurrently.

   1. Confinement Boundary

      a. Check confinement boundary integrity. Observe the function of reactor bay access doors, the condition of observation area windows, and the condition of seals at other room penetrations.
      b. Check operation of the CSC annunciator indicating an opened or closed status for the doors to the reactor bay.

   2. HVAC System

      a. Change HVAC system mode to REACTOR ON per OPER-5
      b. Verify normal indications on Control Room Panel (CRP). Open panel to document manometer readings. Compare with previous data for trends indicating system performance. See Reference 2 Attachment for normal readings.
      c. Test operation of isolation dampers:
         
         Notify PRC Physical Plant Chilling Station (471-3770) of the test.

         i. Using radioactive check source, initiate alarm (trip point is at 10,000 cpm which is ≤ 2x10⁻⁹ µCi/cc) on air particulate monitor.
         ii. Verify SUPPLY DAMPER and RETURN DAMPER status lights on Control Room Panel indicate CLOSED position within 30 seconds of alarm initiation. The lamps for the HVAC SUPPLY FAN ON and RETURN FAN ON should also extinguish.
         iii. Remove check source at monitor, place CRP HVAC isolation switch to ISOLATE. Depress HVAC RESET button on CRP.
         iv. Verify system will not restart and remains in isolation mode.

      d. Restart system in REACTOR OFF mode.
         
         Contact BRC Physical Plant Personnel if HVAC recovery is unsuccessful.

         i. Place HVAC ISOLATION switch in OPERATE. Set mode switch to REACTOR OFF. Depress HVAC RESET button on CRP.
         ii. Verify SUPPLY DAMPERS and RETURN DAMPERS are OPEN.
         iii. Verify REACTOR MODE OFF, SUPPLY FAN ON, and RETURN FAN ON lamps illuminate.

         If either fan (AHU-3 or RF-2) is not on, check for the source of the trip in the penthouse and reset.

   3. Argon Purge System

      a. Startup argon purge system with the pool surface and beam port purge valves open.
      b. Check purge exhaust velocity on manometer in Control Room Panel and check filter pressure drop on magnehelic gauges in 4.1M4.

         Compare to normal values in Reference 2 Attachment.

      c. Test operation of Argon Isolation. Notify PRC Physical Plant (471-3770) of the test.

         i. Using radioactive check source, initiate alarm (trip point is at 10,000 cpm) on the air particulate monitor.
         ii. Verify Argon Purge Fan On status lamp indicates off within 30 seconds of alarm initiation.
         iii. Remove check source at monitor and depress HVAC reset button inside CRP. Argon Purge fan should resume normal operation.

      d. Shutdown argon purge system.
      e. Schedule replacement of the filters based on pressure drop indications. A Radiation Work Permit is required for opening the filter caisson.

         i. Initiate plans to change the filters when the pressure drops reach near fully loaded values:

            1.0" H₂O - 95% filter, 2.25" H₂O HEPA filter.

         ii. Do not change the final HEPA filter without recertification of filter system efficiency.

         The maximum acceptable leakage is 0.05% for 0.3 micron particles.

      f. Check alignment of each valve at the argon beam port purge collection manifold.

   4. Fume/Sort Hood

      a. Start Fume/Sort Hood per procedure.
      b. Verify normal operating conditions.
      c. Test operation of isolation dampers. Notify PRC Physical Plant (471-3770) of the test.

         i. Using radioactive check source, initiate alarm (trip point is at 10,000 cpm) on air particulate CAM.
         ii. Verify lamps on the CRP and the fume/sorting hood control panel indicate fan motor off and smoke damper closed within 30 seconds of alarm indication.
         iii. Remove check source at monitor and depress HVAC reset button inside CRP. Fume/Sorting hood should resume normal operation.

      d. Shut down Fume/Sorting hood per procedure.

.. _SURV-5.II.C:

C. Annual Check Instructions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   1. Confinement Boundary

      a. Inspect and repair any significant damage to weather-strip seals on the five doors to the reactor bay or other penetration seals.
      b. Check the condition of air movement control barriers at the five pipe penetration ports through the platform at the pool surface.

   2. HVAC System

      a. Inspect reactor bay isolation dampers. During the corresponding monthly inspection (HVAC system shutdown and isolation dampers closed), remove the inspection panels and inspect each of the six isolation dampers. Verify dampers appear to be in the shut position and do not show evidence of damage or deterioration.
      b. Repeat step 2c of monthly HVAC system checks except test function of both manual isolation button on first level of reactor bay and HVAC ISOLATE switch on the Control Room Panel instead of CAM alarm.
      c. Inspect HVAC System ducts for evidence of damage.

   3. Argon Purge System

      a. Check operation of pool, beam port, dilution and isolation valve for evidence of malfunction.
      b. During corresponding monthly inspection, (Argon purge system off and isolation damper closed) check position of valve shaft at filter bank inlet and verify damper closed.
      c. Schedule inspection of the filter system every two years. A Radiation Work Permit is required for opening the filter caisson.

         i. Replace the pre-filter during each biennial inspection.
         ii. Perform a visual inspection of the 95% filter. Replace filter if physical deterioration is apparent.

   4. Fume/sorting hood

      a. During corresponding monthly inspection of fume/sorting hood system (hood fan shutdown and dampers closed) remove access panel at smoke damper and inspect damper condition. Also check valve shaft at hood filter outlet for closed alignment position.
      b. Initiate plans to change the filters when the pressure drops reach near fully loaded values.


SURV-6 Control Rod Calibration
==============================

I. INTRODUCTION
---------------

A. Purpose
~~~~~~~~~~

   The Control Rod Calibration Procedure benchmarks the primary system for reactor control and safety.

B. Description
~~~~~~~~~~~~~~

   Knowledge of control rod worth is necessary to assure the appropriate performance of the reactor control system and demonstrate compliance with Technical Specification limits. Both routine operating conditions and the safety functions of the control rods depend on accurate calibration data. Two separate methods of measurement are available to provide calibration data. The Rod Drop Experiment determines the approximate integral control rod worth by observation of the change in reactor power level as a function of time after the rod drop. This experiment provides the initial estimate of a rod’s worth and may be used after major core rearrangements to predict approximate rod worth. The experiment may also verify the total rod worth after minor core changes. The second method of rod calibration is the Positive Period Experiment. This method provides the most accurate measurement of the differential rod worth. This experiment determines both the total control rod worth and the shape of the control rod position versus control rod worth curve. The Positive Period method should be used for normal control rod calibration.

   Measurement of the rod drop times verify the performance of the system safety function per Technical Specification requirement. The SCRAM switch or relay in the safety circuit initiates the safety circuit action dropping all control rods. Individual rod switches initiate the drop of each individual rod. Rod position switches sense when the rods reach the full down position. Proper performance of the safety system is indicated if all rods reach the full down position in the specified time limit.

   Measurement of the control system rod removal rate coupled with the control rod peak differential worth establishes the maximum reactivity insertion rate of each control rod. This rate is limited as specified in the Technical Specifications to allow the safe control of the reactor in manual or auto mode.

C. Schedule
~~~~~~~~~~~

   Control rod calibrations are to be done at least once each year and after any significant change to the reactor core configuration. Annual calibration measurements should be done in January or July but shall not exceed longer than 15 months from preceding measurement.

   Measurement of control rod drop time and reactivity insertion rate should be done annually, not to exceed 15 months from preceding measurement, and/or after control rod or drive maintenance, reactor core reconfiguration, or movement of fuel adjacent to the standard rod drives.

D. Contents
~~~~~~~~~~~

   .. line-block::
      :ref:`A. Rod Drop Procedure <SURV-6.II.A>`
      :ref:`B. Positive Period Procedure <SURV-6.II.B>`
      :ref:`C. Control Rod Drop Time and Removal Rate Measurement <SURV-6.II.C>`

E. Attachments
~~~~~~~~~~~~~~

   .. line-block::
      1. Reactivity vs. Power Ratio Plot
      2. Positive Period Data Sheet
      3. Stable Period Wait Time
      4. Inhour curve - Reactivity vs. Period Plot
      5. Rod Drop Time / Withdrawal Rate Data Sheet

F. Equipment, Materials
~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      TRIGA ICS System with control rod drives  
      Data Analysis Software such as "MathCAD"  
      Digital Stopwatch  
      Digital Storage Oscilloscope

G. References, Other Procedures
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      MAIN-6, Rod & Drive Maintenance, Inspection  
      Attachments 1 & 3:  
      A. Edward Profio, "Experimental Reactor Physics",  John Wiley and Sons Inc., 1976, pp 712, 716  
      Attachment 4: 
      General Atomics Data Sheet

II. PROCEDURE
-------------

.. _SURV-6.II.A:

A. Control Rod Worth Estimate by Rod Drop Method
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   Use to estimate initial control rod worth following new core start-up. May be useful following substantial core reconfigurations.

   1. The reactor core condition should be cold and clean prior to measurement of rod worth. Perform ICS system pre-start checks. The reactor coolant system pumps should be off during control rod calibration.

   2. Commence Startup of the reactor:

      a. Position the control rod being evaluated at the desired position - full up if the entire rod worth is desired to be estimated in one step, or partially withdrawn at selected increasing withdrawn locations if several drops are to be made.

      b. Position the two rods closest to the rod being evaluated at a banked elevation, position the control rod farthest from the rod being calibrated at about 900 units to allow fine control of its reactivity for achieving criticality.

      c. Adjust control rods for criticality at a low power level such as 50 to 500 watts. The power should not be so high as to see a fuel temperature increase above ambient (i.e., less than 1 Kilowatt).

      d. Remove the neutron source and readjust for criticality. The delayed neutrons should be allowed to come into equilibrium as evidenced by the indicated power remaining constant to within ±2% for a minimum of 3 to 5 minutes without further rod movement.

   3. Setup data recording system to record reactor linear power as a function of time or use stopwatch and indication on linear power display to tabulate initial power and the indicated power after the control rod is dropped.

   4. Drop control rod being evaluated by actuation of magnet button (standard rod drives) or air button (transient rod drive) and document the power vs. time data. Select times to record data based on time data plotted on the graph in Attachment 1 - Ratio of neutron density after a rod drop to the initial density (at critical), as a function of subcritical reactivity.

   5. Using the data in Attachment 1, determine the reactivity associated with the rod drop based on the measured neutron density ratio (power ratio) at the specified time after the rod drop.

.. _SURV-6.II.B:

B. Control Rod Worth Measurement by Positive Period Method
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. line-block::
      Use for the annual rod worth calibration.  
      Use as the primary rod calibration method.

   1. The reactor core condition should be cold and clean prior to measurement of rod worth. Perform ICS system pre-start checks. The reactor coolant system pumps should be off during control rod calibration.

   2. Commence Startup of the reactor:

      a. Position the control rod being evaluated at the desired position - full down if the entire rod worth is to be evaluated, or at predetermined locations if the shape of the differential rod worth curve has already been established.

         i. Initial control rod calibrations or calibrations after major core reconfigurations should evaluate the entire rod worth by stepwise pulling the rod in increments correlating to reactivity steps of 15 to 20 cents over its entire travel. This will require taking 10 to 20 measurements per control rod depending on its total worth.
         ii. Once the initial control rod calibration curve shape has been established, subsequent routine control rod calibrations may be made by using only 5 or 6 appropriately selected insertions of the same reactivity magnitude as above. One or two points should be selected near the rod height correlating to the peak differential rod worth. Four additional points should be selected, two in the lower and two in the upper parts of the rod travel correlating to areas spaced roughly equally on the slope portions of the differential worth curve. The data from these measurements can then be curve fit to the shape of the differential control rod worth curve to determine the actual rod worth.

      b. Position the two rods closest to the rod being evaluated at a banked elevation, position the control rod farthest from the rod being calibrated at about 900 units to allow fine control of its reactivity for achieving criticality.

      c. Adjust control rods for criticality at a low power level of 1 to 3 Watts.

   3. Remove the neutron source and readjust for criticality. The delayed neutrons should be allowed to come into equilibrium as evidenced by the indicated power remaining constant to within ±4% for a minimum of 3.5 to 5 minutes without further rod movement. This constraint will limit measurement errors of criticality to ± ~0.25¢ per measurement.

   4. Record the Control rod positions on the Control Rod Calibration Data Sheet in Attachment 2.

   5. Pull the control rod being calibrated in one smooth movement a distance correlating to an estimated reactivity worth of 15 to 20 cents which correlates to a stable period between 58 and 37 seconds. Record the rod position stop point on data sheet. (To minimize rod position hysteresis, if you inadvertently pull the rod too far, quickly move the rod back down slightly below the target point, then raise the rod to the target point.) Refer to previous calibration data to estimate the number of units to move the rod. Typical movements are 90 to 100 units for the initial and final pull at the full down or full up endpoints, decreasing rapidly to 20 to 40 units per pull in the mid range of rod travel. The reactivity per pull is limited to allow the reactor to attain a stable period prior to taking the power vs. time data thus reducing measurement errors. The time to reach a stable period is called the wait time. The wait times for 5% error are 20 to 35 seconds, for a 1% error they increase to 50 to 65 seconds respectively for 37 to 58 second stable periods. A table showing measurement errors as a function of the wait time required to attain a stable period is shown in Attachment 3.

   6. Observe the power increase as indicated on the digital readout of the auto ranging linear power channel on the Animation Window. Use a stopwatch set to measure time intervals with respect to the start time. Start the primary stopwatch when the power passes the 60 watt point. Record the time when the power passes the 90 watt level, the 600 watt level, and the 900 watt level (time points should be marked at the first instant the power reaches the target value on the digital display). Time data at powers above the 1 Kilowatt level shall not be used as temperature feedback will create errors above this level.

   7. Drive control rods other than the rod being calibrated down to decrease the reactor power. Leave the control rod being calibrated at the point to which it was withdrawn in step 5 if the entire rod is being stepwise calibrated. If the curve fit method is being used, reposition the rod being calibrated to its next starting point.

   8. Repeat steps 2 through 7 until the remainder of the rod is completed or sufficient data points for curve fitting are obtained.

   .. note::
      As long as the power level is not allowed to fall below the source interlock the source may be continuously left out of the core until all the data points desired are obtained. Each sequence through this process will take approximately 15 minutes if everything is done with attention to detail so plan accordingly.

   9. Analyze data either manually or via software program. Using the time data recorded, calculate the stable period resulting from each rod pull. Then use the reactivity equation or inhour curve in Attachment 4 to determine the reactivity associated with each rod pull.

   10. A senior operator should review and approve the rod calibration data. If significant changes in rod worth are indicated, a review of the implications on excess reactivity and shutdown margins should also be initiated.

.. _SURV-6.II.C:

C. Control Rod Withdrawal, insertion, and drop time measurements
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   1. Perform ICS system pre-start checks if not already completed.

   2. Setup drop time measurement system. The magnet power supply voltage level controlled by the console scram switch should be used to start the timing. A signal from the control rod down limit switch should be monitored to indicate when the rod has reached the full down position.

      a. Measurement equipment should be a storage oscilloscope or an electronic timer with signal start-stop features. Use of a stopwatch to measure rod drop time, manually started at the time the scram button is depressed and stopped at the time the rod visually hits bottom is also acceptable but not the preferred method of measurement.

      b. Measurement resolution for oscilloscope sweep should be set to 100 ms/div, vertical gain should be set to 5 V/div. Vertical signal probe should be set to X 10 for the transient rod, and X 1 for all other rods. Scope should be set to Auto trigger mode while setting up, and changed to single trigger or normal mode when taking the data.

      c. Connect start signal (scope trigger) to the Regulating rod positive magnet power (see table below for connection location). Set the scope trigger to DC coupling on a negative slope at a level of about 10 volts. The nominal magnet power high side is +13 volts and the low side is -6 volts.

      d. Connect the signal (Channel 1) to the rod drive down limit switch (see table below for connection location) of the drive being evaluated.

      +------------------+-----------+---------------------------+
      | Scope Input      | DAC Tie   | Description               |
      | Channel          | Bar       |                           |
      +==================+===========+===========================+
      | Trigger          | TB 5-3    | Reg Magnet Pwr (+13V)     |
      | CH 1             | TB 8-8    | TR rod down limit         |
      | CH 1             | TB 8-16   | Shim 1 rod down limit     |
      | CH 1             | TB 8-24   | Shim 2 rod down limit     |
      | CH 1             | TB 9-32   | Reg rod down limit        |
      +------------------+-----------+---------------------------+

   3. Withdraw control rod being measured about 60 units and test drop the rod to verify the scope setup.

   4. Fully withdraw the rod being evaluated, measuring the time it takes to move from full down to full up using a stopwatch. Record data on Attachment 5.

   5. Drop the control rod to trigger and record a trace by initiation of the scram button. Drop time is measured from the time the scope triggered until the rod reaches full down, as evidenced by the transition of the signal on the rod down switch. Some rods may show a bounce after the initial bottom transition, typical drop time recorded is the time measured to when the rod remains full down as indicated on the trace. Record data on Attachment 5.

   6. Repeat steps 2d through 5 for each remaining rod.

   7. Calculate measured reactivity insertion rate and record data on Attachment 5:

      a. Obtain peak differential rod worth near rod midpoint for each rod from the control rod calibration data.  
      b. Calculate insertion rate (< 0.2 % Δk/k/sec) as follows:

         rate (% Δk/k/sec) = rate (units/sec) * worth (¢/unit) * (0.7% Δk/k / 100¢)

   8. Document any relevant notes, comments, or observations on Attachment 5 data sheet.

SURV-7 Pulse Characteristic Comparison
======================================

I. PURPOSE
----------

   The purpose of this procedure is to monitor the core performance for a reference pulse reactivity insertion.

II. DESCRIPTION
---------------

   The pulsing characteristics of the TRIGA reactor release large amounts of energy, 20M Joules, in a very short time period <0.5 seconds. Some variation of the peak power, energy release and fuel temperatures will occur as a function of fuel history. In fact long term full power runs with few pulses may differ from many pulses with no long term full power runs.

   No pulse program should proceed without a comparison of reference pulse characteristics. A $3 reference pulse at least once each year or prior to resumption of pulsing if no annual pulse has been made will provide pertinent data to verify that the peak power, energy release, and fuel temperatures are within acceptable limits.

   The pulse characteristics are to be done annually or prior to the resumption of any pulsing program if the time interval to the previous pulse exceeds one year.

III. REFERENCES
---------------

   Pulse records

IV. EQUIPMENT AND MATERIALS
----------------------------

V. Instructions
---------------

   1. Review present reactor system conditions with respect to previous reactor configuration. Several conditions may cause different pulse characteristics such as number of elements, history and burnup.

   2. Review previous comparative pulse data. Set rod drive air pressure at 65 psi.

   3. Specify pulse ID as "COMPARE - Month/Year."

   4. Perform reactor pulse ($2.00). Reactivity insertion should be equivalent to that of previous comparative pulse based on current rod worth measurements.

   5. Print the pulse data screen. Print the graphic pulse data. Use the same scales as used on previous comparative pulse.

   6. Document the following additional data on the printed pulse data:

      a. Core configuration; # control, # elements, # graphite, # exp.  
      b. Initial steady-state power and excess reactivity.  
      c. Worth of transient rod insertion  

   7. Review current pulse data and record core conditions. Compare with previous data for indication of a significant change in reactor core transient characteristics.

   8. Place data in Pulse Data Sheet Log.

