# Build-your-movie-database
Using public API (here is IMDb) to request data and build the pipeline in Python to store the data into local MySQL sever.

### Why do we need API when we could use requests and <code>bs4</code> to retrieve data?
There is always sometime we need to fetch data from the website, and parsing web data by iterative requests and then parsing by <code>bs4</code> would be painful. First of all, the html data might be hard to parse or even some of the data are generated dynamically, making parsing one level harder. Secondly, you always have to wait the whole data to be rendered by web server and then catch the data to do further parsing and digesting. It's a more general way to scrape data, though. However, **when there is a more convinent tool to request data, why bother yourself to pretend as a user to scrape data from the original web page?** If a website provides its own API(Not many do, thou), we should always leverage it and get the data more efficiently. Therefore, below is how do we use API?

1. Finding whether there is a API you could leverage, and I recommend [API list](https://apilist.fun/)


### After we get the data using API, how to store into your local database?
Here I use Python to requests the data and use <code>json</code> package to parse the requested data.