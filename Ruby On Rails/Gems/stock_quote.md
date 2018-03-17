install stock quote in gems

gem 'stock_quote', '~> 1.5', '>= 1.5.4'

then you can use rails console to access stock quotes with

```StockQuote::Stock.quote('GOOG')```

to see close price

```StockQuote::Stock.quote('GOOG').l```

to see open price

```StockQuote::Stock.quote('GOOG').op```
