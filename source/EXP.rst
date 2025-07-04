===
EXP
===

EXP-PTS Pneumatic Transfer System
=================================

I. INTRODUCTION
---------------

A. PURPOSE
~~~~~~~~~~

    The purpose of this procedure is to assure safe, routine operation of an experiment facility that produces radioactive materials.

B. DESCRIPTION
~~~~~~~~~~~~~~

    The Nuclear Engineering Teaching Laboratory (NETL) Pneumatic Transfer System (PTS),
    sometimes referred to as a "rabbit" system, is used to transport sample vial (rabbits or carriers)
    between a fume hood in room 3.102 and the TRIGA Reactor Core in room 1.104. This
    procedure details the operation of the system and the requirements that must be met in order to
    use it for the production of radioisotopes and/or Neutron Activation Analysis (NAA).

    The pneumatic transfer system shuttles samples by air changes of air pressure between two
    system end points, a loading port and the irradiation terminal. Controls for the system allow
    manual operation or automatic operation with preset times for the irradiation period. This system
    enhances the production of short half-life radioactive materials.

    Two different size irradiation terminals and transport tubes are available. Each terminal and
    transport tube system requires different transport capsule sizes. The outside diameter of both
    terminal sizes is designed to fit in a standard fuel element position. The two terminals have
    different internal diameters, a large diameter for use with General Atomic standard reusable
    capsules of high-density polyethylene, and a small interior diameter for use with disposable low-
    density polyethylene capsules. Two small diameter irradiation terminals are available that
    provide different characteristic neutron flux profiles. One terminal is a standard terminal for
    thermal neutron irradiation. The other terminal has a cadmium lining for epithermal neutron
    irradiation.

C. SCHEDULE
~~~~~~~~~~~

    This procedure applies to each use of the PTS at any time that an irradiation terminal is in a
    reactor grid plate location and the reactor is at power.

D. CONTENTS & Attachments
~~~~~~~~~~~~~~~~~~~~~~~~~

    PTS Schematic

E. EQUIPMENT, MATERIALS
~~~~~~~~~~~~~~~~~~~~~~~

    PTS Components

    1.) Transport tube and control system 
        a) Large tube transport system, GA Terminal  
        b) Small tube transport system, standard Terminal  
        c) Small tube transport system, Cd-lined Terminal  

    2.) Loading port, Insert Tube and Sample Clip 

    3.) Transport, carrier (rabbits) capsules  
        GA standard capsules     large tube system  
        Emerald capsules         large tube system  
        Adanac capsules          small tube system 

    4.) Control lockout key  

    5.) CO2 fill gas for tube  

F. REFERENCES, OTHER PROCEDURES
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

    1.) UT TRIGA SAR Report (Chapter 8)  

    2.) UT TRIGA PTS Description
        Experiment Authorization:  

        +-------------+---------------------------------------+
        | 3.2.1a,b,c  | large tube system                     |
        +-------------+---------------------------------------+
        | 3.2.2a,b,c  | small tube system, standard terminal  |
        +-------------+---------------------------------------+
        | 3.2.3a,b,c  | small tube system, Cd lined terminal  |
        +-------------+---------------------------------------+

G. NOTES:
~~~~~~~~~

II. PROCEDURE
-------------

    **USE OF THE NETL PNEUMATIC TRANSFER SYSTEM**

1. Determine which type of irradiation terminal and transport tube system is needed.  

   a) Large tube transport system, GA Terminal. There is no maximum power limit for use of the large tube GA transfer tubes and terminal. Transport capsules for the GA terminal are reusable 20 to 25 times. A periodic inspection of the transport capsule should be done to avoid capsule breakage during irradiation.  
   b) Small tube transport system, standard Terminal. There is no maximum power limit.  
   c) Small tube transport system, Cd-lined Terminal. The maximum power limit for the small tube terminals is 500 kW. This limit is based on terminal temperature and vial temperature characteristics necessary to assure vial deformation does not cause the vial to become stuck in the core terminal. Transport capsules are not reusable.

2. The user must have completed the NETL Radiation Safety Training Course and be familiar with the operation of the controls for the Pneumatic Transfer System. The Reactor Supervisor or his designee shall train new users of the system.

3. Submit an "Operation Request" and "Irradiation Request" defining the reactor operating requirements and type of samples. Specify type of use of the Pneumatic Transfer System as radioisotope production or Neutron Activation Analysis (NAA).

4. Each sample shall be characterized as **solid** or **non-solid** (such as fine powders, volatile compounds, liquids or gases).  

   a) All solid samples shall be contained within a primary vial with a thermal type seal.  
   b) The transport or carrier capsule does not provide a thermal seal for solid or non-solid samples.  
   c) A secondary thermal type containment is a requirement for each non-solid sample. A secondary containment may consist of a plastic bag with a heat type thermal seal.

5. Samples to be irradiated in the small tube terminal must be packaged in the appropriate carrier vial. The system design is for a 0.650 inch diameter capsule in a 0.685 diameter transport tube. Each carrier vial must pass through a test port. Limiting operating temperature for low-density polyethylene is 85°C.  

   a) Use Adanac type carrier vials that have a smooth cap, a double ridge for cap retention, and a smooth flush cast bottom.  
   b) Do not use similar vials made by Emerald (formerly Olympic) which have a molded strip across the cap and a molded name in the bottom.  
   c) Test each transport capsule prior to use in the PTS loading port.  

   **USE ONLY A CAPSULE THAT PASSES THROUGH THE TEST PORT**

6. The user must establish communication with the Reactor Operator via the Reactor Control Room Intercom System. A radiation monitor must be available to monitor the radiation dose prior to handling samples after irradiation in the reactor core.  

   a) Announce the insertion of each sample into the reactor.  
   b) Measure the radiation dose of each sample prior to removal from the loading port.

7. The Lockout Key at the control unit located in the Reactor Control Room will be turned ON by the Reactor Operator when personnel and irradiation conditions are ready. A six minute time period provides purge of the pneumatic tube system with CO2. During the purge period both the RED LED and the GREEN LED illuminate for six minutes. At the end of pneumatic tube system operation turning the Lockout Key OFF will light the RED LED and GREEN LED for two minutes.

8. Select the appropriate irradiation period using the BCD switch: 

    a) 

    +--------------+----------------------------------------------------+
    | BCD setting  | Action                                             |
    +==============+====================================================+
    | 0            | Manual operation of insert and remove functions    |
    +--------------+----------------------------------------------------+
    | n            | Automatic operation of insert and remove functions |
    +--------------+----------------------------------------------------+

      The carrier will be inserted and removed by pressing the corresponding switch. At present, a timer limits the irradiation time to 10 minutes for "safety" reasons. The manual mode does not use the sample sensors to control operation. A fixed (5) five-second carrier return time is set so that a sensor failure to detect the sample does not prevent shutdown of the fan.  

   b) `<n>` is the setting for automatic operation, the carrier will be inserted for a preset number of seconds of irradiation and then removed by the PLC timer action. A (2) two-second delay is built into the automatic sequences to avoid accidental insertion of the sample. This is partly a precaution for the lack of tactile feedback in the switch.  

    +---+------------------+
    |  n| irradiation time |
    +===+==================+
    |  1| 10. seconds      |
    +---+------------------+
    |  2| 0.5 minutes      |
    +---+------------------+
    |  3| 1.0 minutes      |
    +---+------------------+
    |  4| 2.0 minutes      |
    +---+------------------+
    |  5| 3.0 minutes      |
    +---+------------------+
    |  6| 5.0 minutes      |
    +---+------------------+
    |  7| 10. minutes      |
    +---+------------------+

   c) Pressing the Insert Switch will reset (turn off) the LED lights. Holding the switch for two seconds or pressing the switch a second time after a two second delay will activate the fan and valves for insertion of the sample.  
   d) Pressing the Remove Switch will immediately return the sample to the load port. A timer will return the carrier if the Remove Switch is not pressed. The carrier sensors must detect the carrier for the proper operation of the automatic cycle.

9. Turn on exhaust fan for the fume hood in room 1.102.

10. Examine the carrier and the cap for cracks. Carrier and cap must be free of cracks. Insert sample vial into the carrier. Test sample carrier in test port. The mass of the sample shall not exceed 5 grams.

11. Load the carrier containing the sample into the pneumatic terminal port with the carrier cap pointing downward. Close the compartment and latch the load port lid.

12. Both lights are off for the loading of the first sample. For all subsequent samples illumination of the GREEN LED should indicate that the sample is at the loading port.

13. To send the sample carrier and start irradiation, push the Insert Switch.  
    a) The GREEN LED goes out, while the sample is in transit.  
    b) The RED LED illuminates when the carrier reaches the pool sensor at the reactor pool.

14. Conclusion of the irradiation timer or pressing the Remove switch returns the sample.  
    a) The RED LED goes out as the carrier exits the pool.  
    b) The GREEN LED goes on as the carrier reaches the loading terminal.  
    c) Both RED and GREEN lights illuminate during the fan coast down time with the carrier at the loading terminal. As the fan stops, the RED LED extinguishes while the GREEN LED stays lit.

15. Enter sample and carrier data in the log book kept in room 3.102. The logbook shall contain the date, time, sample ID and the carrier dose rate at the loading port (at 30 centimeters).  
    a) If the dose rate is less than 100 mrem/hr at 30 cm, remove the carrier from the loading terminal and proceed with sample analysis.  
    b) If the dose rate is more than 100 but less than 500 mrem/hr at 30 cm, the carrier shall be removed from the loading terminal and shielded till the dose drops below 100 mrem/hr at 30 cm.  
    c) If the dose at the end of irradiation is more than 500 mrem/hr at 30 cm, the user shall keep a distance of at least four (4) feet away from the loading port until the dose drops to 500 mrem/hr.

16. If the carrier is not returned at the end of the preset irradiation time, push the Remove Switch. If the carrier does not reach the loading port within 10 seconds, contact the Reactor Operator immediately.

17. In case of any malfunction (failure of a sample to return, carrier broken, etc.) or unusual system behavior, immediately notify the Reactor Operator and the Reactor Health Physicist.

18. If the carrier fragments on its way back to the loading terminal, the user shall:  
    a) Inform the Reactor Operator immediately.  
    b) Collect the fragments from the loading port.  
    c) Do **NOT** send any carrier without the approval of the Reactor Operator.

19. If the carrier sample leaks (causes contamination to the loading port) the user shall:  
    a) Inform the Reactor Operator immediately.  
    b) Remove the carrier from loading port.  
    c) Do **NOT** send any carrier without the approval of the Reactor Operator.

20. If the carrier return is successful, proceed with the next sample as needed.  

After the last carrier is irradiated, inform the Reactor Operator of the conclusion of the work. The GREEN and RED LED’s will illuminate for two minutes when the Lockout Key is turned off by the Reactor Operator.

EXP-BP3.1 Neutron Activation Analysis
=====================================

I. PURPOSE
----------

    The purpose of a neutron activation analysis experiment is to determine
    the constituent elements of a material by inducing neutron capture and decay
    reactions in the isotopes of stable elements.

II. DESCRIPTION
---------------

    Analysis of the radiation energies of the unstable radioactive isotopes
    that occur by neutron capture reactions provides information that
    qualitatively identifies the elements in a sample and quantitatively
    determines the amount of the corresponding stable elements. This
    description applies to three types of materials with irradiation times of one
    hour to 60 hours. Material types are biological, geological and
    engineering.

    Long-lived nuclides are those radionuclides that will occur by
    irradiating samples in the Rotary Specimen Rack (RSR) and at the Center Tube
    Facility (CTF). One consequence of the irradiation time is sample handling
    hazards that depend on the sample decay time.

    In the case of the CTF, sample encapsulation must be water tight and
    consist of two encapsulation boundaries. Sample encapsulations must be
    compatible with the experiment facility environment, air or water. If a
    fuel element core position (FECP) or external core irradiation tube (ECIT)
    is available the sample requirements are the same as for the RSR and CTF.

**Experiment Requirements:**  
    - Rotary Specimen Rack in graphite reflector, or  
    - Center Tube Facility Irradiation Tube.

III. REFERENCES
---------------

    - Fixed RWP # yr-xxxF - Reactor unloading  
    - Fixed RWP # yr-xxxF - Sample processing  
    - Experiment Authorization B3.1
      
        - B3.1.A Biological Samples  
        - B3.1.B Geological Samples  
        - B3.1.C Engineering Samples  


IV. PROCEDURE FOR SAMPLE IRRADIATION
------------------------------------

1. User must complete request forms to schedule operation. The necessary
   forms are the "Operation Request" form and "Sample Radiation or Exposure"
   form. Forms are available from the Reactor Supervisor.

   The experiment authorization contains an "Irradiation of Material
   Worksheet". The worksheet provides guidance to assure that a request meets
   the requirements of the NAA experiment authorization.

2. Sample preparation and encapsulation are the responsibility of the user.
   Encapsulations must meet the requirements for this class of experiments.

   Every effort should be taken to avoid any sample leakage. A leaking
   sample may cause the loss of one sample or the loss of an entire batch of
   samples if measurements indicate that unsafe handling conditions exist.

3. The reactor operator shall inform the user of any change to the
   scheduled irradiation date and time.

4. Loading and unloading samples in the reactor requires the actions of a
   reactor operator and the health physicist.

   The experimenter with the approval of the reactor operator may assist
   with the loading of samples into irradiation rabbits and reactor experiment
   facilities. However, the experimenter must have had radiation safety
   training to assist with the unloading of any sample from an experiment
   facility.

   A unique sample identification name or number will be recorded with the
   loading and unloading date and time of each sample within any experiment. A
   log record of the samples is kept in the "Sample Log (in-core)" or "Exposure
   Log (ex-core)". User may submit an extra sheet with the same format to list
   more samples.

5. Notify the Reactor Operator or his representative of the loading.
   Record the loading of each sample. Record each sample identification and
   the reactor irradiation position.

   A record must exist of the samples or an entry for each sample must be
   made in the sample log. Controls on the sample type and size are set by the
   NAA Experiment Authorization.

6. Notify the Health Physicist or his representative of the unloading.
   Review each sample identification and the reactor irradiation position.
   Measure and record the radiation dose at 30 cm for the unloading of each
   sample.

   - If the sample radiation dose rate is less than 100 mrem/hr @ 30 cm then
     the sample may be made available to process as necessary for the experiment.

   - If the sample radiation dose rate is more than 100 mrem/hr @ 30 cm but
     less than 500 mrem/hr, a swipe must be taken to check for leakage of the
     sample encapsulation. If the sample radiation dose rate is more than 500
     mrem/hr @ 30 cm the sample may not be taken from the reactor pool until decay
     to a level acceptable for removal.

   - Leaking samples shall not be made available for experiment measurements.
     Encapsulation of a leaking sample may provide recovery of the sample for
     experiment measurements.

7. An RWP (rm 1.104 pool) will exist for removal of samples from the pool
   and storage prior to processing.

8. Sample transfer from the reactor pool to the processing area shall use a
   sample carrier to control contamination and radiation exposure. Sample
   transfer between the Reactor Bay (1.104) and Sample Handling Lab (3.102)
   shall use the sample pass-thru port.

   Exceptions may be made by the reactor supervisor for special conditions
   or when sample geometry prohibits such transfers.

9. An RWP (rm 3.102 west) will exist for process handling, storage,
   counting and handling for counting. The HP shall take necessary steps to
   prepare areas for that task according to the HP procedure # HP-6.

10. Sample batches shall be in a container with labeling that identifies the
    experimenter, the project, the samples and radioactive material. Samples not
    in the container must be in the counting process with a label at the
    detection system that indicates the presence of radioactive materials.

11. Samples at the completion of a project will be set aside for disposal.
    The experimenter shall provide the samples and if necessary analysis to
    assist with the ultimate disposition of the samples.
