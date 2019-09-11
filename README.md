# tam-data

Analysis to understand what is the market opportunity for both DApp and Layer 1 simulations along with everything in between.

***
## Zoomable Icicles
Here we show the comparative differences between `Market Capitulation`, `Money Raised`, `Users / Transactions`, `Category Count` of different blockchain protocols and tokens organized by different categories. Note that some categories have data points entirely missing. Example, it is difficult acquire transaction and user data for the long tail of layer 1s. However given this limitation we've constructed a lower and upper bound for all the metrics.

**Blog Post** [here]()

**Visualization** [here](https://observablehq.com/@lelandlee/protocol-sizing-landscape-l1-l2-dapps) If you want to update the visualization with your own data, follow the `data.csv` file format and update the ```base = d3.csv(<url>)``` with your own url. Feel free to fork the code and make your own changes. This is the main reason why we chose to put the visualization into [observablehq](https://observablehq.com/), as it makes real time editing and forking straight forward.

## data.csv format
| Column Name | Description                                    |
|-------------|------------------------------------------------|
| name        | name of the protocol                           |
| g1          | 1st grouping - Layer                           |
| g2          | 2nd grouping (opt.)  - Sector/Consensus Mech.  |
| g3          | 3rd grouping (opt.) - Subsector (dApps only)   |
| market_cap  | market cap of protocol if applicable           |
| mau         | monthly active users of protocol if applicable |
| funding     | funding received by protocol if applicable     |

Caveats on the Data
* All MAU data is on dApps rather than L1
* MAU should not be seen as an additive metric
* MAU is for dapp usage not ERC20 transfers
* Market cap data is recent but not up to date
* All the groupings of protocols is arbitrary
* Gaming dApps were not included due to difficulties in acquiring meaningful data
