### Interval
* To change supported intervals in chart, modify the array https://github.com/yasincidem/chart/blob/cad09dcbd2d1039839e63edb92f33cb1917ed2f5/src/components/TVChartContainer/api/index.js#L5

### Timeframe
* To change timeframe in chart, modify the object
https://github.com/yasincidem/chart/blob/cad09dcbd2d1039839e63edb92f33cb1917ed2f5/src/components/TVChartContainer/index.jsx#L19

### Default Options
* To change widget default options like theme, interval, symbol etc. modify the defaultProps object 
https://github.com/yasincidem/chart/blob/cad09dcbd2d1039839e63edb92f33cb1917ed2f5/src/components/TVChartContainer/index.jsx#L33

### Disable Features
* To disable some features, modify the array
https://github.com/yasincidem/chart/blob/cad09dcbd2d1039839e63edb92f33cb1917ed2f5/src/components/TVChartContainer/index.jsx#L57

### Enable Features
* To enable some features, modify the array
https://github.com/yasincidem/chart/blob/cad09dcbd2d1039839e63edb92f33cb1917ed2f5/src/components/TVChartContainer/index.jsx#L58

### Configure Buttons
https://github.com/yasincidem/chart/blob/ebf40078bb6e20e4c054582e091ad318b27c0321/src/components/TVChartContainer/index.jsx#L76


### Add New Pairings
* To add new pairings, add symbol like "BTC/UTH" as key, exhange that supports the key(symbol) as value
https://github.com/yasincidem/chart/blob/cad09dcbd2d1039839e63edb92f33cb1917ed2f5/src/components/TVChartContainer/api/pairs.js#L1
* and add symbol, full_name, description, exchange, type to data array for searchable and selectable pairings
* Let's say you want to add "LTC/BTC" pairing.You should know which exchange supports the pairing.In this case "LTC/BTC" is supported by Binance.Then,

```

export default {
  "BTC/USD": "Coinbase",
  "ETH/USD": "Coinbase",
  "XLM/BTC": "Bitfinex",
  "XLM/ETH": "Bitfinex",
  "XLM/USD": "Bitfinex",
  "LTC/BTC": "Binance"
}

```
```

{
  symbol: 'LTC/BTC',
  full_name: 'LTC/BTC',
  description: 'description',
  exchange: 'Binance',
  type: 'type'
}

```

### How to build

**git clone https://github.com/yasincidem/chart.git**

**cd chart**

**npm install**

Make your changes on code

To test your changes do **npm start**.It will be displayed on localhost:3000

To get production build do **npm run build**.It will create build folder.

Get charting_library folder, static folder and index.html from build folder add these to public folder in your react app
