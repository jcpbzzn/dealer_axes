# Dealer Axes

## Overview

This class of functions uses Bloomberg APIs to retrieve and elaborate dealers axes for a single bond or a collection of bonds. 

The goal of this project is to build a *momentum* indicator which, based on the estimate of dealer's end of day inventory, calculates whether the "street" is either long or short a particular name. 
This is particularly useful for understanding flows, street positioning and build a momentum indicator.

## Methodology

The main assumption is that the last RUN sent by a dealer on a given day is representative of their positioning on a particular security.

For example, at the end of the trading session, on bond ABCD 4 3/4 05/15/36 Bank XYZ is bid axed for 5,000,000 (5MM X) at B+217 (217/) and is offer axed for 300,000 (X 300M) at B+213 (/213).
The trader is net bid axed for 4,700,000 and the script considers Bank XYZ as net short ABCD 4 3/4 05/15/36 for 4,700,000.

