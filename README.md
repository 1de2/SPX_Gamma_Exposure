
# SPX Gamma Exposure Table

Upload a CSV containing options data (from CBOE free with a 15-minute delay) to produce a GEX Table

![gexexample](https://github.com/user-attachments/assets/95a8db3c-1a7e-4bcc-927e-aa6e46282cca)


## Installation

Install this project with GitHub

In your terminal run 

```bash
  git clone git@github.com:Nicholas-Battista/SPX_Gamma_Exposure.git
  pip install pandas
  pip install pyqt6
```
Then simply run the code!
## Tutorial

Before running the program head on over to [CBOE's Website](https://www.cboe.com/delayed_quotes/spx) to grab your options data (this link takes you to $SPX)

    1. Click on "Options" below the search bar
    2. Select the "Options Range" drop-down and choose "All"
    3. Click the green view chain to see all strikes for every day of the current month
    4. Scroll all the way down and click "Download CSV"

Upon gathering your data you can now run the program and will be met with this

![blankgex](https://github.com/user-attachments/assets/eb2728ac-4af3-4fff-b9cb-75b1cfef041f)


Enter the spot price in the empty area (spot is the current price)

Click "Load CSV" and upload the CSV you downloaded from CBOE

From here just choose the strikes you want the table to aggregate across, and click submit!

You now have an accurate GEX representation!!
## Legend



### Net GEX - Net of positive vs negative gamma
- Cell Highlights
    - Dark green: Strike with the highest positive gamma
    - Light Green: Strike with second highest positive gamma
    - Dark Red: Strike with the highest negative gamma
    - Light Red: Strike with second highest negative gamma
    
    

### Absolute GEX (abs) - Absolute value of pos and neg gamma
 - Cell Highlights
    - Dark Blue: Strike with most Abs gamma
    - Light Blue: Strie with second most Abs gamma



### OI - Open Intrest
- Cell Highlights
    - Green Text (symbol): Highest call OI
    - Red Text (symbol): Highest put OI
    - Blue Text (symbol): Highest combined OI
    - Grey Shade: relatively higher OI vs all strikes

### Additional Data
- Put/Call Ratio: Ratio of puts to calls
- Net Positive/Negative Gamma: Total of each side gamma exposure
- Max Pain: Strike Price where the most Calls/Puts expire worthless


