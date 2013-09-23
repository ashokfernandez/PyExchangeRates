# PyExchange : An unoffcial interface to the Open Exchange Rates API


## Author: Ashok Fernandez - https://github.com/ashokfernandez/
## Date  : 23 / 09 / 2013

## Description: 
Downloads the latest exchange rates from http://openexchangerates.org/ and saves them to a file. If the file can be
found the module will load the rates from the file if the file is less than one day old. Otherwise the file is updated
with the newest rates. There are money objects which can be manipulated with addition, substraction, multiplication
and division - with the results always being in USD. Money values can be converted to other currencies. See the example
below for more details

## Usage example: 
    import PyExchange
    exchange = PyExchange.Exchange('YOUR API KEY HERE')
    a = exchange.withdraw(1000, 'USD')
    b = exchange.withdraw(1000, 'EUR')
    print a + b
    2352.363797 USD

    print a - b
    -352.363797 USD

    print a * b
    1352363.796680 USD

    print a * 2
    2000.000000 USD

    print a + b
    2352.363797 USD

    print b / 2
    500.000000 USD

    print a.convert('AUD')
    1061.079000 AUD
