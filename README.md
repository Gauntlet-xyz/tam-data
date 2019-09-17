# tam-data

Data gathered on the market size for crypto infrastructure. Data sourced from:
* [CoinGecko](https://www.coingecko.com/en)
* [State of the dApps](https://www.stateofthedapps.com/)

With additional information from:
* [ICOBench](https://icobench.com/)
* [ICODrops](https://icodrops.com/)
* [ICOMarks](https://icomarks.com/)
* [ICORating](https://icorating.com/)
 
You can read more on [the blog post here]().

***
## Adding data

Review the schema below to add or update data. [Here's an example commit](https://github.com/GauntletNetworks/tam-data/pull/1) - it's great to include a source with each update. You can test the CSV by forking it along with the visualization below, and updating the path as described to the forked file. 

## Zoomable Icicles


**Visualization** [here](https://observablehq.com/@lelandlee/protocol-sizing-landscape-l1-l2-dapps-fixed-height)

Here we show the comparative differences between `Market Cap`, `Money Raised`, `Users / Transactions`, `Category Count` of different blockchain protocols and tokens organized by different categories. Note that some categories have data points entirely missing. For example, it is difficult acquire transaction and user data for the long tail of layer 1s. However, given this limitation we've constructed a lower and upper bound for all the metrics.

If you want to update the visualization with your own data, follow the `data.csv` file format and update the ```base = d3.csv(<url>)``` with your own url. Feel free to fork the code and make your own changes. This is the main reason why we chose to put the visualization into [Observable](https://observablehq.com/), as it makes real time editing and forking straightforward.

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
