#Methodology

##Obspy
\cite{Krischer_2015}

##Match filter detection

\cite{Gibbons_2006}
\cite{Shelly_2007}
###EQcorrscan
\cite{Chamberlain_2014}
##NLLoc location of detections
Make sure to mention: Picks were adjusted by cross-correlation with detecting template. Allowed to shift no more than 0.1 seconds and thrown out if ccval < 0.3. Events with fewer than 6 picks were not located. \cite{Lomax_2014}

##HypoDD relocation of events
\cite{Waldhauser_2000}
##Clustering
Match filter detection techniques are computationally expensive when applied across large datasets. The expense is multiplied as more earthquakes are added to the list of desired detectors (referred to by Barrett and Beroza as the design set) \cite{Barrett_2014}. At the same time, it is important that the design set effectively represent the variety of sources present in a given study area or risk missing what might be important seismicity. To address this, we use a hierarchical clustering technique to create groups of similar events. These groups are then represented by a series of subspace detectors.

The design set, representing the catalog for Ngatamariki/Rotokawa for 2015. To reduce that number to a manageable size, we cluster the events based upon event-event cross correlation coefficients.

##Subspace Detection

##Matched Field Processing
\cite{Templeton_2013}