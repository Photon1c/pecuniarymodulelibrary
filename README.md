# Pecuniary Scripts Library

![Logo](/inputs/logo.png)

A collection of financial scripts to speed up the process of batch processing input lists through screeners and visualizer output generators.

The sequence of steps that these scripts adhere to is as follows:

-Retrieve a list of stock tickers.  
-Iterate them through screening functions.  
-Update list with output from screening functions to generate charts.  

Check back later as material for this project is released.

```mermaid
stateDiagram-v2
Inputs --> Screeners
Screeners --> Charts
Charts --> Inputs
```
# Advanced Screening Added 2.9.2025 ⚗️🔎  

A hypothetical portfolio that contains a given list of tickers may be sorted in the following manner so as to decide which positions to close and which to keep. This is for educational purposes only and is not financial advice, the concepts here are meant to build upon existing ones and branch on to new ones. Check back later for new scripts.  

```mermaid
flowchart TD
    A[Start] --> B{Evaluate Stock Performance}
    B -- Gain > 10% --> C{Consider for Gainers}
    B -- Loss > 5% --> D{Consider for Losers}
    
    C -- Short-Term Strategy --> G("Gainers_close: Sell and take profits")
    C -- Long-Term Strategy --> H("Gainers_keep: Hold for potential growth")
    
    D -- Loss Potential Recoverable --> I("Losers_keep: Hold and wait for improvement")
    D -- Loss Unlikely to Recover --> J("Losers_close: Sell and cut losses")
    
    B -- No Significant Change --> K["Monitor and Re-evaluate Later"]
```


