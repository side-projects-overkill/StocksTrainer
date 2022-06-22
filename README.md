# Stock Trainer
This repo contains some information about stock trainer

<h3>WIP: Architecture Diagram </h3>
https://www.figma.com/file/hYHqMQO2HRvDLysBOAXN5H/Stuff?node-id=0%3A1

<h3>Work Pipeline:</h3>
<ul>
  <li>Kite API Bridge - Makes API Calls to Broker (Kite)</li>
  <li><strong>Historical Data DB (Design Pending)</strong> - DB to store historical data, OHLC with timestamp, volume, OI</li>
  <li><strong>Data Manager</strong> - Provides historical stock data from Broker</li>
  <li>Data Request MQ</li>
  <li>Data Notify MQ</li>
  <li><strong>Backtester</strong> - The meat of the machine, parses, executes strategies on historical data and generates results
    <ul>
      <li>Can we use ready-made backtester? https://pypi.org/project/Backtesting/</li>
      <li>Whats the feasibility?</li>
    </ul>
  </li>
  <li><strong>Strategy Code</strong> - Code executed by the backtester on the historical data to generate trades
    <ul>
      <li>Use Python scripts for backtesting?</li>
      <li>Use Java .class with Serialization/Reflection?</li>
      <li>Write Custom parser / interpreter?</li>
    </ul>
  </li>
  <li>Strategy code persistence - How to store strategy code?</li>  
  <li><strong>Backtester results</strong> (format pending) - Data generated from executing strategy</li>
  <li><strong>Strategy DB (Design Pending)</strong> - Stores data like strategies and execution results.</li>
  <li>Backtester MQ</li>
  <li>Stuff API - API to add strategy, launch backtest, fetch results etc.</li>
</ul>
