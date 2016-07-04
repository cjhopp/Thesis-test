#Methodology

##Match filter detection
 
\cite{Gibbons_2006}
\cite{Shelly_2007}

##NLLoc location of detections
Make sure to mention: Picks were adjusted by cross-correlation with detecting template. Allowed to shift no more than 0.1 seconds and thrown out if ccval < 0.3. Events with fewer than 6 picks were not located. \cite{Lomax_2014}

##HypoDD relocation of events
\cite{Waldhauser_2000}

##Computing
For this work we relied heavily on the seismic processing Python package Obspy \cite{Krischer_2015}. Matched filter detection was done using an open-source Python package called EQcorrscan \cite{Chamberlain_2014}, which allows for a scalable, multi-parallel approach to the matched filtering routine. The package's so-called "embarassingly parallel" approach allowed us to make use of the PAN computing cluster at the University of Auckland through the New Zealand eScience Infrastructure (NeSI), which cut the processing time from what may well have been measured in months to a matter of a few days.
