# Uber Trip History Bookmarklet

A nifty little bookmarklet that scrapes your Uber trip history and spits out a CSV file, using [artoo.js](http://medialab.github.io/artoo/) - inspired by hours trying to wrangle with the appearingly intentionally handicapped Uber Developer API (would you believe this isn't possible using it?) + [this awesome gist.](https://gist.github.com/Yomguithereal/5d792d88ad6f1fe7c15d)

Once you have your CSV, the extacted data can be easily visualized using the [Uber Data Visualizer](#) project.

## How To Use

First up, install the bookmarklet from [insert link] by dragging and dropping it in your bookmarks bar.

Once installed, navigate to https://riders.uber.com/trips, login and then click the bookmarklet from your bookmark bar. Uber currently takes ~5 seconds per page of 20 rides, so depending on how big an Uber user you are things may take a while. You'll see a "Scraping in progress.." message and it will automatically download a CSV once it's done. 

If you'd like to monitor it's status more granularly, fire up your Developer Tools and monitor the network activity. 

The bookmarklet currently scrapes and outputs the following fields:

- trip_id
- date
- date_time
- driver
- car_type
- city
- price
- payment_method
- start_time
- start_address
- end_time
- end_address

## Building
If you'd like to build the bookmarklet yourself, navigate to the project directory and run the following:

```bash
# Assumes you have grunt installed ([sudo] npm install -g grunt grunt-cli)
npm install
gulp
```

This will output a `build/uber-trip-history.bookmark.js` file containing the bookmarklet. It also automatically copies the bookmarklet to your clipboard, so you can easily install it in your browser.