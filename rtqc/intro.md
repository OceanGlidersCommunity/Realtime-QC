# Realtime Quality Control for Underwater Gliders

## Credits

(List of contributors including brief description of the contribution(s))

[List of contributors](section-contributors)

## Statement of Purpose

## Inbox - Content to be processed

Here I'll add texts from our discussions that should be processed and organized
in this new document. Mostly copy-n-paste so we don't loose anything.

Topics that reached a consensus

### What defines real-time QC?

## Main Document

<!-- Underwater gliders only -->
This document is focused on underwater gliders, which use changes in buoyancy as the main propulsion, thus characterized by relatively slow propagation velocities.
Other types of platforms with different natures of operation, such as wave gliders and propelled underwater autonomous vehicles, might take advantage of this document but there is no intention on covering specific aspects of those other platforms.

<!-- Why should we do RTQC? -->
There are a wide range of applications that cannot afford waitting for the delayed mode product due to time constraints, such as data assimilation for weather and sea state forecasts, thus requiring a real-time quality control with low latency. Given the diverse environments where gliders are operated and differences among glider models, the operators themselves are the best suited to evaluate their own measurements. Despite that, different users might have different priorities as well as tolerance for what they consider as useful data. While for data assimilation one might unforgive bad measurements and rather use less data with higher quality, a monitoring or alerting system cannot afford wrongfully flaggin and miss a single extreme event. Although there is no one unique optimal flagging for everyone, communication with the final users and understanding of the expectations can help fine tunning the QC criteria and desired informative flags. It should be expected that some users will apply their own QC procedure in addition to the QC from the operators, but all it takes is one obviously bad data point to damage the credibility of the whole dataset. Even before the final users, the glider operation itlsef benefits from a continuous real-time QC. A prompt detection of sensor degradation might trigger an early recovery and swap sensors or the full platform when possible. Catastrophic failures are sometimes preceded by anomalous behaviour, thus high rate of errors should raise the alertness of the pilots. Some spurious measurements are inevitable for any ocean observing system. Despite the constraints imposed by telemetry and pressure for low latency, real-time QC has clear benefits and should be part of all glider operation.

<!-- Do not modify the original data -->
The methods described here augment the original data to guide the user on the decision of what to trust and hence what to use. The raw data must not be modified, but instead  classification quality flags should be aggregated, therefore, allowing users to apply alternative quality control methods without limitations. For instance, advanced methods might be developed in the future, requiring the original data to avoid error propagation. Quality control in this document does not consider calibration but is limited to a classification. Whenever it is considered important to provide the best data possible ready to use, the recommendation is to aggregate such corrected data while preserving the original values directly available.

<!-- Do not limit to automatic procedures -->
Real-time QC is commonly associated with automatic checks, which indeed better suit the fast response requirements for a real-time data stream, but it should not be limited to automatic procedures. One of the distinct characteristics of underwater gliders is the close monitoring from pilots and scientists as frequently as hourly to at most every couple of days. 
Complex cases, otherwise missed by the automatic procedures, but identified by the operators should be flagged and updated in the data stream. With the assumption of a low rate of mistakes by the automatic procedure, it is best to do not hold the automatic procedure for manual confirmation, but employ a fast automatic assessment and stream a posterior correction when necessary.

include::tests.adoc[leveloffset=+1]

## Procedures

#### Argo BGC

9. Spike test (median)

Red Sea and Mediterranean Sea, flag 4 if test value > 1 micromole/kg

Other places, flag 4 if test value > 5 micromole/kg

## History

Virtual synchronous meeting on XXX.
(add participants/contributors on each step.

### Virtual workshop

Between May 11 - 15 2021

(I think we had one single sync meeting. Find the correct date/time, participants, and notes taken)

### Async discussions from Apr 10 2021 to July 19 2021
Title Best Practices on Realtime QC

### Called: Main document

Contacted people by email.

Asynchronous discussions through a Google Docs initiated on Feb 2021 and contributions extended up to Oct 2021.

A Google Doc was choosen at that time to reduce the technical barrier and expand
the participation and contributions.

Participants:

* Guilherme Castelao (Gui), castelao@ucsd.edu, Scripps Institution of Oceanography
* Soeren Thomsen, soeren.thomsen@locean.ipsl.fr,	LOCEAN, OceanGliders.org Best Practice coordinator
* Mark Bushnell, mark.bushnell@noaa.gov
* Pierre Testor, pierre.testor@locean.ipsl.fr
* Emma Slater, emmer@bodc.ac.uk
* Justin Buck, juck@bodc.ac.uk
* Mun Woo, mun.woo@uwa.edu.au,	IMOS Ocean Gliders
* Thierry Carval, thierry.carval@ifremer.fr, IFREMER
* Corentin Guyot, corentin.guyot@ifremer.fr, IFREMER
* Sylvie Pouliquen, Sylvie.Pouliquen@ifremer.fr, IFREMER and Euro*Argo ERIC
* Victor Turpin, vturpin@oceanops.org, OceanOPS
* Nikolaos Zarokanellos, nzarokanellos@socib.es, SOCIB
* Christoph Waldmann, waldmann@marum.de, MARUM
* John Kerfoot, kerfoot@marine.rutgers.edu
* Claire Gourcuff, claire.gourcuff@euro-argo.eu

(section-contributors)=
## Contributors

List of all contributors an their contributions.

*  Schmechtig (@catsch), CNRS
   PR-1: Details on Argo's Nitrate test
