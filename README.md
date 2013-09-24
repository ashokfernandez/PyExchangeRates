# PyExchangeRates 
### An unoffcial interface to the Open Exchange Rates API


## Author
[Ashok Fernandez](https://github.com/ashokfernandez/)


## Description: 
Downloads the latest exchange rates from http://openexchangerates.org/ and saves them to a file. If the file can be
found the module will load the rates from the file if the file is less than one day old. Otherwise the file is updated
with the newest rates. There are money objects which can be manipulated with addition, substraction, multiplication
and division - with result is in USD but can be converted to any currency. See the example below for more details.

## Usage example: 
    import PyExchangeRates

    # Create an 'Exchange' object, this holds all the information about the currencies and exchange rates
    # Get a free API key from https://openexchangerates.org/signup/free
    exchange = PyExchangeRates.Exchange('YOUR API KEY HERE')         
    
    # Withdraw a few different currencies from the exchange
    a = exchange.withdraw(1000, 'USD')
    b = exchange.withdraw(1000, 'EUR')

    # Money can be added together, the result will be in USD
    print a + b
    2352.363797 USD

    # Money can be subtracted...
    print a - b
    -352.363797 USD

    # Multiplied...
    print a * b
    1352363.796680 USD

    # Scaled up...
    print a * 2
    2000.000000 USD

    # and divided by a constant
    print b / 2
    500.000000 USD

    # Money can also be converted to other currencies 
    print a.convert('AUD')
    1061.079000 AUD
