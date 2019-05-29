# FXCM-LiveConnect
FXCM API to use live ticker data

A working file in progress that will continue to be updated - see remarks.
This will be combined with a ML prediction BUY/SELL trading agent to execute trades.
Final version will either grab historical ticker data or from when the connection is made, wait until there is enough data for the ML predictor to calculate and start trading.
Possibibly the ticker data will be saved to a CSV file and newer ticker data will be added to this file.
Auto timer and manual stop will be added.

## Update ##
Within the week I will probably update this that will include a working example - I found a YouTube from FXCM that has been extremely useful.

The code I have written by myself, but someone could be just as effiencent and copy something from the FXCM GitHub.

I still have to work out a solution to take in live trades, pass this through my ML Algo, then use this new data to execute a new trade.
As there is a bit of computing time behind grabbing the data and predicting, I think 30 minute intetervals will work.
There is an OCO script that I mentioned previously to close any open trades and then open a new one.
The timer / auto stop will be reviewed, not sure I will just close after each day of trading or maybe base this from the ROI% gained. E.g. once the trading has made 500% ROI from the inital account value, it will close the trade and connection.

Mainly I will concentrate on creating this in Juptyer Notebooks and then 'convert' to a py script to run from Digital Ocean.
Addtional features will include a start-up function to provide an overview of the account and give the use options to choose what instrument they want to trade
