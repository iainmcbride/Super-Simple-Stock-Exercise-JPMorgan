# Super-Simple-Stock-Exercise-JPMorgan

The files in this repository contain the code for the exercise demonstrating simple calculations involving stocks and trades for JP Morgan recruitment.

Assumptions:

The specification is unclear whether a user should be able to add stocks to the system. ("No database or GUI is required, all data need only be held in memory.") Thus, I have not created any structure for user input. However, in the file starterClass I have added the list of stocks shown in the specification to the collection class Stocks. 

Since, the specification does not make clear whether the user should be able to add transactions to the system, I have also created 10 random transactions in the class starterClass involving the stocks in the specification each with a timestamp between 30 minutes ago and now. (Only those transactions within the last 15 minutes are used to calculate the stock price as per the specification.) These stocks and trades allow the user to see the results when using example stocks and trades and demonstrate that the code in the Stock and Stocks class performs as required.

I've created an inner class in the Stock class called Trade to hold the data associated with trades involving the Stock object in question. The specification seems to suggest that a trade is a property of a stock object. However, it would be a simple matter to create a completely separate class Trade and a collection class Trades to achieve the same result. 

In the definition of P/E ratio, the denominator of the formula for calculating P/E ratio is described as 'Dividend'. I have assumed in the implemented calculation that this was intended to mean the 'Last Dividend' for the stock in question. This means that the P/E ratio of the 'TEA' stock is ill-defined, I have assumed that in this case the P/E ratio should be zero.

Throughout the implementation I have made the assumption that 'Ticker Price' = 'Stock Price'.

I have set up the program to create a file called 'Stock and Trade Details.txt" in the same folder as the program is run. The details of the stocks and trades involved and the results of the calculations are output to this file. 

