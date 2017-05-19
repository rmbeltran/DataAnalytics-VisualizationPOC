## Data Analytics and Visualization Proof of Concept
The following is a demostration of some Data Analytics I performed on sales data. The goal was to identify ways to help Account Managers boost their ability to bring in recurring revenue.

### The Analysis
The analysis was done primarily using SQL on a teradata data source. First I performed some data exploration on the product sales data. During the exploration phase it is important to clearly understand the underlying business concept in order to be able to gain some context of how the data fields in our source are utilized. I also like to use data vizualization in order to understand how all of the data fields interact and what they represent when describing the sales lifecycle. For example: If a particular end customer has 50K rows of data, I would attempt to condense all of that data into something I can vizualize on a timeline or by a few other characteristics, in order to understand how the customer behaves.

#### Here is an example below of compressing 50k lines of data into a single vizualization looks like:
<img src="https://github.com/rmbeltran/Images/blob/master/TimelineViz.PNG" width="800" height="450" />

You can immediately start to get a feel for how this particular customer does business. You can see the full lifecycle of a post sale, from shipment to contract, to contract end date and other key information about the customer and products.

### Documentation
Its important to document your observations and ideas about the analysis you have performed to date to as to not lose on those moments of enlightenment that you can use in your Analytics. For example in this particular case I started to notice certain trends in how the products were sold and renewed.

### Investigation
The more and more I looked at the data and my visual aides, I noticed that some products showed certain desirable charcteristics from a recurring revenue perspective while others didn't. I decided to perform some statistical analysis at the product id level to test my thesis. 

### Data Wrangling
Using SQL I collected data on all product id's (over 50K!) and manipulated the data to horizontally organize all of the contract timelines for a paricular distinct serial number instance and computed a contract coverage score (ratio). I then took those coverage scores (ratios) at the distict product id level and computed an average coverage ratio, standard deviation and skew. The end result was a lookup table with the entire list of product id's and their summary stats. 

### Actionable Analytics
Being able to show the seller which of their opportunities was highly likely to close made it actionable. This was extremely exciting as we could now give the seller the ability to prioritize opportunities so they could determine where to invest their time and efforts wisely.

### Building an interactive Demo
In order to demonstrate how the analytics could be leveraged, I built a webapp that contained visualizations and explanations of the analysis so the stakeholders could interact with the solution and dream of the posibilities.

