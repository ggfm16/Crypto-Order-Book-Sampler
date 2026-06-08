# Crypto Order Book Sampler

An automated data sampling notebook built and designed to run in Google Colab. Pulls live order book data from the Coinbase public API and logs key market microstructure metrics to a dated CSV file on a configurable schedule.

## What It Does
- Connects to the Coinbase Advanced Trade public API — no API key required
- Calculates bid/ask volume and capital within a configurable price threshold around the best bid and ask
- Automates recurring data collection using a scheduler, sampling at a set interval for a set number of samples
- Exports all collected samples to a dated CSV file for downstream analysis

## Notes
Originally written against the Binance API. Binance returns HTTP 451 from US-based servers including Google Colab due to geo-restrictions. Coinbase was used as a drop-in replacement with a minor adjustment to the response parsing to account for the different order book entry format.

## Running the Notebook
Open in Google Colab and run cells in order. Configure your trading pair, price threshold, sample interval, and sample count in the configuration cell before running the scheduler. All libraries used are available in Colab by default — no additional installation required.
