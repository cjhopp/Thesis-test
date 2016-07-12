#Methodology

##Match filter detection
Matched filter earthquake detection relies on waveform cross corelation of a known earthquake signal or signals with continuously recorded seismic data. It has been shown to be especially useful in noisy areas where more traditional, amplitude-based techniques fail \cite{Gibbons_2006} \cite{Shelly_2007}. This makes it particularly useful in areas of geothermal power generation where large numbers of highly similar, low-magnitude earthquakes can occur and which are usually subject to high levels of anthropogenic noise associated with the power generation process.

The 637 events taken from the filtered GNS catalog were used as 'template events' for this study. Each template waveform was one second long, starting 0.1 seconds before the P-pick at each station for which a pick was made. Waveforms were filtered from 1.0 to 20.0 Hz after confirming that most events in the dataset contained significant amounts of energy within that pass band. Continuous seismic data were processed in an identical manner to the templates prior to matched filtering.

To generate detections, event templates were cross correlated with continuous data at a rate of 50 samples per second. At each sample, the cross correlation coefficients for each channel of data were summed to create the network detection statistic. Whenever the detection statistic exceeded a threshold value, in this case the mean absolute deviation (MAD) of the detection statistic multiplied by 8 (as suggested by \cite{Shelly_2007}), a detection was recorded.

##NLLoc location of detections
Picks for each of the newly detected events were made based upon cross correlation of the detecting template with the continuous data at the time of the detection. Template waveforms were correlated with network data over a 0.2 second window centered on the detection time. If a cross correlation coefficient of greater than 0.3 was found within that window, the pick was made at the time corresponding to the highest correlation value. Channels for which a correlation coefficient of greater than 0.3 did not exist were ignored. We kept all events with more than 5 picks and discarded those with fewer. These events were then located using the nonlinear location program NonLinLoc \cite{Lomax_2014} using the OctTree search algorithm.

##HypoDD relocation of events
As a final step, the entire catalog was relocated using the double-difference relocation program HypoDD \cite{Waldhauser_2000}. Due to the size of the catalog, events were split into separate Rotokawa and Ngatamariki catalogs before being relocated with HypoDD.

##Computing
For this work we relied heavily on the seismic processing Python package Obspy \cite{Krischer_2015}. Matched filter detection was done using an open-source Python package called EQcorrscan \cite{Chamberlain_2014}, which allowed for a scalable, multi-parallel approach to the matched filtering routine. The package's so-called "embarassingly parallel" approach allowed us to make use of the PAN computing cluster at the University of Auckland through the New Zealand eScience Infrastructure (NeSI), which cut the processing time from months to a matter of a few days.
