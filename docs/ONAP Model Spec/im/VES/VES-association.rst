.. Copyright 2021
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

VES Model Associations
----------------------

MeasurementHasCodecsInUse
~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== =========== ========= ======================
**Attribute Name** **Aggreg.** **Navig.** **Type**    **Mult.** **Description**
\_codecsinuse      composite   Navig.     CodecsInUse 0..\*     Array of codecs in use
measurement        none        Not navig. Measurement 1        
================== =========== ========== =========== ========= ======================

MeasurementHasCpuUsage
~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== =========== ========= =========================
**Attribute Name** **Aggreg.** **Navig.** **Type**    **Mult.** **Description**
\_cpuUsage         composite   Navig.     CpuUsage    0..\*     Usage of an array of CPUs
measurement        none        Not navig. Measurement 1        
================== =========== ========== =========== ========= =========================

MeasurementHasDiskUsage
~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== =========== ========= ==========================
**Attribute Name** **Aggreg.** **Navig.** **Type**    **Mult.** **Description**
\_diskUsage        composite   Navig.     DiskUsage   0..\*     Usage of an array of disks
measurement        none        Not navig. Measurement 1        
================== =========== ========== =========== ========= ==========================

MeasurementHasHugePages
~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== =========== ========= =============================
**Attribute Name** **Aggreg.** **Navig.** **Type**    **Mult.** **Description**
\_Hugepages        composite   Navig.     HugePages   0..1      Array of metrics on hugePages
measurement        none        Not navig. Measurement 1        
================== =========== ========== =========== ========= =============================

MeasurementHasFilesystemUsage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

======================= =========== ========== =============== ========= ===========================================================================
**Attribute Name**      **Aggreg.** **Navig.** **Type**        **Mult.** **Description**
\_filesystemusage       composite   Navig.     FilesystemUsage 0..\*     Filesystem usage of the VM on which the xNFC reporting the event is running
measurementhasdiskusage none        Not navig. Measurement     1        
======================= =========== ========== =============== ========= ===========================================================================

MeasurementHasIpmi
~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== =========== ========= ==========================================================
**Attribute Name** **Aggreg.** **Navig.** **Type**    **Mult.** **Description**
\_ipmi             composite   Navig.     Ipmi        0..1      Array of intelligent platform management interface metrics
measurement        none        Not navig. Measurement 1        
================== =========== ========== =========== ========= ==========================================================

MeasurementHasLatencyBucketMeasure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

====================== =========== ========== ==================== ========= ====================================================================================================================================================================================================
**Attribute Name**     **Aggreg.** **Navig.** **Type**             **Mult.** **Description**
\_latencybucketmeasure composite   Navig.     LatencyBucketMeasure 0..1      Array of integers representing counts of requests whose latency in milliseconds falls within per-xNF configured ranges; where latency is the duration between a service request and its fulfillment.
measurement            none        Not navig. Measurement          1        
====================== =========== ========== ==================== ========= ====================================================================================================================================================================================================

MeasurementHasLoad
~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== =========== ========= ============================
**Attribute Name** **Aggreg.** **Navig.** **Type**    **Mult.** **Description**
\_load             composite   Navig.     Load        0..1      Array of system load metrics
measurement        none        Not navig. Measurement 1        
================== =========== ========== =========== ========= ============================

MeasurementHasMemoryUsage
~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== =========== ========= ===============================
**Attribute Name** **Aggreg.** **Navig.** **Type**    **Mult.** **Description**
\_memoryusage      composite   Navig.     MemoryUsage 0..\*     Memory usage of an array of VMs
measurement        none        Not navig. Measurement 1        
================== =========== ========== =========== ========= ===============================

MeasurementHasNicPerformance
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ============== ========= ==========================================================
**Attribute Name** **Aggreg.** **Navig.** **Type**       **Mult.** **Description**
\_nicperformance   composite   Navig.     NicPerformance 0..\*     Performance metrics of an array of network interface cards
measurement        none        Not navig. Measurement    1        
================== =========== ========== ============== ========= ==========================================================

MeasurementHasProcessStats
~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ============ ========= ====================================
**Attribute Name** **Aggreg.** **Navig.** **Type**     **Mult.** **Description**
\_processstats     composite   Navig.     ProcessStats 0..\*     Array of metrics on system processes
measurement        none        Not navig. Measurement  1        
================== =========== ========== ============ ========= ====================================

MeausrementHasMachineCheckException
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

======================= =========== ========== ===================== ========= =================================
**Attribute Name**      **Aggreg.** **Navig.** **Type**              **Mult.** **Description**
\_machinecheckexception composite   Navig.     MachineCheckException 0..1      Array of machine check exceptions
measurement             none        Not navig. Measurement           1        
======================= =========== ========== ===================== ========= =================================

IpmiHasIpmiBattery
~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== =========== ========= ============================
**Attribute Name** **Aggreg.** **Navig.** **Type**    **Mult.** **Description**
\_ipmibattery      composite   Navig.     IpmiBattery 0..1      Array of ipmiBattery objects
ipmi               none        Not navig. Ipmi        1        
================== =========== ========== =========== ========= ============================

IpmiHasIpmiBaseboardVoltageRegulator
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Array of ipmiBaseboard VoltageRegulator objects

Applied stereotypes:

=============================== =========== ========== ============================= ========= ===============================================
**Attribute Name**              **Aggreg.** **Navig.** **Type**                      **Mult.** **Description**
\_ipmibaseboardvoltageregulator composite   Navig.     IpmiBaseboardVoltageRegulator 0..1      Array of ipmiBaseboard VoltageRegulator objects
ipmi                            none        Not navig. Ipmi                          1        
=============================== =========== ========== ============================= ========= ===============================================

IpmiHas IpmiFan
~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ======== ========= ========================
**Attribute Name** **Aggreg.** **Navig.** **Type** **Mult.** **Description**
\_ipmifan          composite   Navig.     IpmiFan  0..1      Array of ipmiFan objects
ipmi               none        Not navig. Ipmi     1        
================== =========== ========== ======== ========= ========================

IpmiHasIpmiBaseboardTemperature
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Array of ipmiBaseboard Temperature objects

Applied stereotypes:

========================== =========== ========== ======================== ========= ==========================================
**Attribute Name**         **Aggreg.** **Navig.** **Type**                 **Mult.** **Description**
\_ipmibaseboardtemperature composite   Navig.     IpmiBaseboardTemperature 0..1      Array of ipmiBaseboard Temperature objects
ipmi                       none        Not navig. Ipmi                     1        
========================== =========== ========== ======================== ========= ==========================================

IpmiHasIpmiGlobalAggregateTemperatureMargin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

====================================== =========== ========== ==================================== ========= ========================================
**Attribute Name**                     **Aggreg.** **Navig.** **Type**                             **Mult.** **Description**
\_ipmiglobalaggregatetemperaturemargin composite   Navig.     IpmiGlobalAggregateTemperatureMargin 0..1      ipmi global aggregate temperature margin
ipmi                                   none        Not navig. Ipmi                                 1        
====================================== =========== ========== ==================================== ========= ========================================

IpmiHasIpmiHsbp
~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ======== ========= =========================
**Attribute Name** **Aggreg.** **Navig.** **Type** **Mult.** **Description**
\_ipmihsbp         composite   Navig.     IpmiHsbp 0..1      Array of ipmiHsbp objects
ipmi               none        Not navig. Ipmi     1        
================== =========== ========== ======== ========= =========================

IpmiHasIpmiNic
~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ======== ========= ========================
**Attribute Name** **Aggreg.** **Navig.** **Type** **Mult.** **Description**
\_ipminic          composite   Navig.     IpmiNic  0..1      Array of ipmiNic objects
ipmi               none        Not navig. Ipmi     1        
================== =========== ========== ======== ========= ========================

IpmiHasIpmiProcessor
~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ============= ========= ==============================
**Attribute Name** **Aggreg.** **Navig.** **Type**      **Mult.** **Description**
\_ipmiprocessor    composite   Navig.     IpmiProcessor 0..1      Array of ipmiProcessor objects
ipmi               none        Not navig. Ipmi          1        
================== =========== ========== ============= ========= ==============================

IpmiHsIpmiPowerSupply
~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== =============== ========= ================================
**Attribute Name** **Aggreg.** **Navig.** **Type**        **Mult.** **Description**
\_ipmipowersupply  composite   Navig.     IpmiPowerSupply 0..1      Array of ipmiPowerSupply objects
ipmi               none        Not navig. Ipmi            1        
================== =========== ========== =============== ========= ================================

IpmiProcessorHasProcessorDimmAggregateThermalMargin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

===================================== =========== ========== =================================== ========= =====================================================
**Attribute Name**                    **Aggreg.** **Navig.** **Type**                            **Mult.** **Description**
\_processordimmaggregatethermalmargin composite   Navig.     ProcessorDimmAggregateThermalMargin 0..1      Array of processorDimmAggregate ThermalMargin objects
ipmiprocessor                         none        Not navig. IpmiProcessor                       1        
===================================== =========== ========== =================================== ========= =====================================================

MobileFlowHasGtpPerFlowMetrics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

=================== =========== ========== ================= ========= ======================================
**Attribute Name**  **Aggreg.** **Navig.** **Type**          **Mult.** **Description**
\_gtpperflowmetrics composite   Navig.     GtpPerFlowMetrics 1         Mobility GTP Protocol per flow metrics
mobileflow          none        Not navig. MobileFlow        1        
=================== =========== ========== ================= ========= ======================================

VoiceQualityHasEndOfCallVqmSummaries
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

======================= =========== ========== ===================== ========= ==========================================
**Attribute Name**      **Aggreg.** **Navig.** **Type**              **Mult.** **Description**
\_endofcallvqmsummaries composite   Navig.     EndOfCallVqmSummaries 0..1      End of call voice quality metric summaries
voicequality            none        Not navig. VoiceQuality          1        
======================= =========== ========== ===================== ========= ==========================================

SipSignalingHasVendorNfNameFields
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

==================== =========== ========== ================== ========= =============================
**Attribute Name**   **Aggreg.** **Navig.** **Type**           **Mult.** **Description**
\_vendorNfnamefields composite   Navig.     VendorNfNameFields 1         Vendor, NF and nfModule names
sipsignaling         none        Not navig. SipSignaling       1        
==================== =========== ========== ================== ========= =============================

VoiceQualityHasVendorNfNameFields
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

==================== =========== ========== ================== ========= =============================
**Attribute Name**   **Aggreg.** **Navig.** **Type**           **Mult.** **Description**
\_vendornfnamefields composite   Navig.     VendorNfNameFields 1         Vendor, NF and nfModule names
voicequality         none        Not navig. VoiceQuality       1        
==================== =========== ========== ================== ========= =============================

Perf3gppContainsMeasDataCollection
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

==================== =========== ========== ================== ========= =====================================
**Attribute Name**   **Aggreg.** **Navig.** **Type**           **Mult.** **Description**
\_measDataCollection composite   Navig.     MeasDataCollection 1         3GPP measurement collection structure
perf3gpp             none        Not navig. Perf3gpp           1        
==================== =========== ========== ================== ========= =====================================

MeasDataCollectionContainsMeasInfo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ================== ========= =========================================================================
**Attribute Name** **Aggreg.** **Navig.** **Type**           **Mult.** **Description**
\_measinfo         composite   Navig.     MeasInfo           1..\*     Array of monitored object local distinguished name ids per 3GPP TS 32.300
measdatacollection none        Not navig. MeasDataCollection 1        
================== =========== ========== ================== ========= =========================================================================

MeasInfoContainsMeasInfoIdInteger
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

=================== =========== ========== ================= ========= ============================
**Attribute Name**  **Aggreg.** **Navig.** **Type**          **Mult.** **Description**
\_measinfoidinteger composite   Navig.     measInfoIdInteger 0..1      Measurement group Identifier
measinfo            none        Not navig. MeasInfo          1        
=================== =========== ========== ================= ========= ============================

MeasInfoContainsMeasInfoIdString
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ================ ========= ============================
**Attribute Name** **Aggreg.** **Navig.** **Type**         **Mult.** **Description**
\_measinfoidstring composite   Navig.     MeasInfoIdString 0..1      Measurement group Identifier
measinfo           none        Not navig. MeasInfo         1        
================== =========== ========== ================ ========= ============================

MeasInfoContainsMeasTypesInteger
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ================ ========= =================================================================================================================================
**Attribute Name** **Aggreg.** **Navig.** **Type**         **Mult.** **Description**
\_meastypesinteger none        Navig.     MeasTypesInteger 0..1      Array of measurement identifiers associated with the measurement results expressed as integers for efficiency rather than strings
measinfo           none        Not navig. MeasInfo         1        
================== =========== ========== ================ ========= =================================================================================================================================

MeasInfoContainsMeasTypesString
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== =============== ========= =================================================================================================================================
**Attribute Name** **Aggreg.** **Navig.** **Type**        **Mult.** **Description**
\_meastypesstring  composite   Navig.     MeasTypesString 0..1      Array of measurement identifiers associated with the measurement results expressed as integers for efficiency rather than strings
measinfo           none        Not navig. MeasInfo        1        
================== =========== ========== =============== ========= =================================================================================================================================

MeasInfoContainsMeasValues
~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ========== ========= ===================
**Attribute Name** **Aggreg.** **Navig.** **Type**   **Mult.** **Description**
\_measValuesList   composite   Navig.     MeasValues 1..\*     Array of measValues
measinfo           none        Not navig. MeasInfo   1        
================== =========== ========== ========== ========= ===================

MeasValuesContainsMeasResultInteger
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

=================== =========== ========== ================= ========= ================
**Attribute Name**  **Aggreg.** **Navig.** **Type**          **Mult.** **Description**
\_measresultinteger composite   Navig.     MeasResultInteger 0..\*     Array of results
measvalues          none        Not navig. MeasValues        1        
=================== =========== ========== ================= ========= ================

MeasValuesContainsMeasResultNull
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ============== ========= ================
**Attribute Name** **Aggreg.** **Navig.** **Type**       **Mult.** **Description**
\_measresultnull   none        Navig.     measResultNull 0..\*     Array of results
measvalues         none        Not navig. MeasValues     1        
================== =========== ========== ============== ========= ================

MeasValuesContainsMEasResultNumber
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== =============== ========= ================
**Attribute Name** **Aggreg.** **Navig.** **Type**        **Mult.** **Description**
\_mesresultnumber  none        Navig.     MesResultNumber 0..\*     Array of results
measvalues         none        Not navig. MeasValues      1        
================== =========== ========== =============== ========= ================

MeasValuesContainsMeasResultString
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ================ ========= ================
**Attribute Name** **Aggreg.** **Navig.** **Type**         **Mult.** **Description**
\_measresultstring none        Navig.     MeasResultString 0..\*     Array of results
measvalues         none        Not navig. MeasValues       1        
================== =========== ========== ================ ========= ================

CmNotifyHasCmNotif
~~~~~~~~~~~~~~~~~~

Applied stereotypes:

================== =========== ========== ======== ========= =============================
**Attribute Name** **Aggreg.** **Navig.** **Type** **Mult.** **Description**
\_cmnotif          composite   Navig.     cmNotif  1..\*     Array of cmNotif notificatons
cmnotify           none        Not navig. CmNotify 1        
================== =========== ========== ======== ========= =============================
