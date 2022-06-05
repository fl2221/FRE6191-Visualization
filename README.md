# FRE6191-Visualization
Visualize user selected stock price, return, return bar plot and Monte Carlo price simulation plot. Also visualize user selected strategy performance on selected stock (Strategy includes two-period SMA, Hidden Markov model, Relative Strength Index). User can also choose the time window they want.

We design our website into 2 parts: 
The first part is to show some basic feature of each stock the user selects, 
and the second part is to show some common strategy performance.

For the FIRST part, the user can choose the time window and the stock they want, we have the default time window here, and after the user choose the ticker, the four graphs will be plotted, and also the number of traces and number of days will be displayed, which are Monte Carlo simulation parameters.
  Number of Traces can be set from 10 to 200 with step 10, and default value 50.
  Number of Days can be set from 10 to 100 with step 5, and default value 30.

Here we got four graphs, and we use flex to display them into 2 by 2 frame, and we also add some cube loading animation here to make it more beautiful. 

The first graph is simply the close price, second graph is stock daily return, for these two we have range slider and also can choose what time step we want. 
Third one is stock return bar plot, the fourth one is the stock price prediction by Monte Carlo method.

For the SOURCE CODE part, we encapsulate the code into 4 classes, it is like we make them into some modules, so that we can apply the formatting or calculation more convenient in our main py file:
-	Stock.py: mainly used to retrieve the history data for selected stock in specific time window, calculate return, and Monte Carlo simulation
-	Graph.py: mainly used to do different graph formatting, and add lines or bars
-	Getdash.py: mainly used to get some user input value
-	Strategy.py: mainly used to generate different strategies like Simple Moving Average, Hidden Markov Model, and Relative Strength Index

And we also use decorators like @staticmethod or @classmethod to make the member function call in each class more convenient.
