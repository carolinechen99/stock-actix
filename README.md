# Stock Market Quotes

## Overview
This is a simple tool that fetches stock market quotes from the Yahoo! Finance API. It allows you to fetch the latest price of a stock, as well as the price at a specific time in the past. It also includes a simple search feature that allows you to search for a stock by keyword.

## Usage
- First run `cargo run` to start the server.
- To search for a ticker by keyword, 
    type in `localhost:8080/search/<KEYWORD>` in your browser.
    Here is an example for searching for keyword "rust":
    ```
    localhost:8080/search/rust
    ```

    And the output will be:
    ```
    Keystone Realtors Limited: RUSTOMJEE.NS
    Keystone Realtors Limited: RUSTOMJEE.BO
    U.S. Strategic Equity Fund Clas: RUSTX
    ```

- To fetch the latest price of a stock, 
    type in `localhost:8080/latest/<TICKER>/<TIMEFRAME>` in your browser.
    Here is an example for fetching the latest price of Tesla stock:
    ```
    localhost:8080/latest/TSLA/1d
    ```
    And the output will be:
    ```
    The latest price of TSLA is $173.22000122070313 at 2023-01-31 21:00:04 UTC
    ```
- To get the history quotes of a stock, type in `localhost:8080/history/<TICKER>/<STARTTIME>/<ENDTIME>` in your browser.
    Here is an example for fetching the price of Tesla stock between 2020-01-01 and 2020-01-03:
    ````
    localhost:8080/history/TSLA/20200101/20200103
    ```

    And the output will be:
    ```
    [Quote { timestamp: 1577975400, open: 28.299999237060547, high: 28.713333129882813, low: 28.11400032043457, volume: 142981500, close: 28.68400001525879, adjclose: 28.68400001525879 }, Quote { timestamp: 1578061800, open: 29.36666679382324, high: 30.266666412353516, low: 29.128000259399418, volume: 266677500, close: 29.534000396728516, adjclose: 29.534000396728516 }]
    ```

### References

* [rust-cli-template](https://github.com/kbknapp/rust-cli-template)
* [yahoo! finance API](https://crates.io/crates/yahoo_finance_api)
* [tokio-test](https://crates.io/crates/tokio-test)