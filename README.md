# LabVIEW Currency Monitor (REST API Integration)

A specialized engineering tool developed in **LabVIEW** to fetch, process, and visualize exchange rate data for **EUR, USD, and CHF** relative to the Polish Zloty (PLN). This project demonstrates the integration of graphical programming with modern web services.

## Features
* **On-Demand Data Fetching**: Updates charts and values only when triggered by the user (Event-Driven UI).
* **Multi-Currency Support**: Compares EUR, USD, and CHF exchange rates in a single interface.
* **REST API Integration**: Connects to the **National Bank of Poland (NBP)** web services.
* **JSON Parsing**: Automated extraction of financial data from JSON responses.
* **Data Visualization**: Clear, interactive charts showing currency trends.

## Tech Stack
* **Environment**: LabVIEW
* **Communication**: HTTP Client (REST API)
* **Data Format**: JSON

### User Interface (Front Panel)
<img width="1106" height="607" alt="image" src="https://github.com/user-attachments/assets/589cba2d-b508-435b-8fd6-a4495354f131" />

### Logic (Block Diagram)
<img width="1352" height="640" alt="image" src="https://github.com/user-attachments/assets/fea9f8f4-39b1-441e-bb52-f672642e1141" />

## How it works
1. The user selects the desired date range or specific currency.
2. Upon clicking the **"Fetch Data"** button, the application sends an asynchronous **HTTP GET** request to the NBP API endpoint.
3. The received **JSON** string is parsed using LabVIEW's native JSON functions.
4. The extracted numeric data is mapped onto a **Waveform Chart/Graph** for visual comparison.

## API Reference
This project uses the [NBP Web Services](http://api.nbp.pl/):
* **Endpoint**: `https://api.nbp.pl/api/exchangerates/rates/{table}/{code}/{startDate}/{endDate}/`
* **Format**: JSON

---
