#Network
The seismic network used in this study is made up of seismometers operated by MRP (NS\*, RT\*), Contact Energy (THQ2, ARAZ), and GeoNet (WPRZ, PPRZ, HRRZ, ALRZ). Throughout 2015, an average of 25 stations were operational on a day-to-day basis. The network covers an area roughly 30km (NE-SW) by 15km (NW-SE) with the bulk of the stations occupying an area 15km (N-S) by 7km (W-E) around the Rotokawa and Ngatamariki geothermal areas. The MRP surface stations are 4.5Hz Geospace GS-11D instruments whereas the Contact Energy station ARAZ is a 1.0Hz Mark Products L-4C3D sensor.
#Dataset
Initial earthquake catalogs for this study are provided by a group at GNS, headed by Steve Sherburn, which is tasked with collecting, and preliminary analysis of, continuous seismic data from the MRP seismograph networks. The MRP data is collected roughly every three months directly from the data loggers. These data are supplemented by data from 
#Methodology
##Match filter detection
 
###EQcorrscan

##Clustering
Match filter detection techniques are computationally expensive when applied across large datasets. The expense is multiplied as more earthquakes are added to the list of desired detectors (referred to by Barrett and Beroza as the design set) \cite{Barrett_2014}. At the same time, it is important that the design set effectively represent the variety of sources present in a given study area or risk missing what might be important seismicity. To address this, we use a hierarchical clustering technique to create groups of similar events. These groups are then represented by a series of subspace detectors.

The design set  , representing the catalog for Ngatamariki/Rotokawa for 2015. To reduce that number to a manageable size, we cluster the events based upon event-event cross correlation coefficients.

##Subspace Detection

##Matched Field Processing

\cite{Templeton_2013}