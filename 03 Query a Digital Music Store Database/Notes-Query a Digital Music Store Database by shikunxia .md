## project intrduction
 For this project, you will be assisting the Chinook team with understanding the media in their store, their customers and employees, and their invoice information. 
 

 ![](https://s3.cn-north-1.amazonaws.com.cn/u-img/e122f4d8-91c7-4544-9d5b-622861a6ef23)
 
1. Question 1: Which countries have the most Invoices?
Use the Invoice table to determine the countries that have the most invoices. Provide a table of BillingCountry and Invoices ordered by the number of invoices for each country. The country with the most invoices should appear first.
![](https://s3.cn-north-1.amazonaws.com.cn/u-img/4ea96041-831f-456d-9faf-61ec1b0d16ce)
````
select BillingCountry, count(BillingCountry)  as Invoices
from Invoice 
group by BillingCountry
order by Invoices desc
````

2. question 2: Which city has the best customers?
We would like to throw a promotional Music Festival in the city we made the most money. Write a query that returns the 1 city that has the highest sum of invoice totals. Return both the city name and the sum of all invoice totals.
```
select BillingCity,sum(Invoice.Total)
from Invoice 
group by BillingCity
order by sum(Invoice.Total) des
```
The top city for Invoice dollars was Prague with an amount of 90.24.

3. Question 3: Who is the best customer?
The customer who has spent the most money will be declared the best customer. Build a query that returns the person who has spent the most money. I found the solution by linking the following three: Invoice, InvoiceLine, and Customer tables to retrieve this information, but you can probably do it with fewer!
```
select Invoice.CustomerId,sum(Invoice.Total)
from Invoice 
group by CustomerId
order by sum(Invoice.Total) desc
```
The customer who spent the most according to invoices was Customer 6 with 49.62 in purchases.
4. Question 4
Use your query to return the email, first name, last name, and Genre of all Rock Music listeners. Return your list ordered alphabetically by email address starting with A. Can you find a way to deal with duplicate email addresses so no one receives multiple emails?
I chose to link information from the Customer, Invoice, InvoiceLine, Track, and Genre tables, but you may be able to find another way to get at the information.
> 使用 distinct name 进行去重 
```
select  distinct Customer.Email,Customer.FirstName,Customer.LastName,Genre.Name
from Track
join Genre
on Genre.GenreId = Track.GenreId 
join  InvoiceLine
on InvoiceLine.TrackId = Track.TrackId
join Invoice
on Invoice.InvoiceId = InvoiceLine.InvoiceId
join Customer
on Customer.CustomerId = Invoice.CustomerId
where Genre.Name =  "Rock"
order by Customer.Email
```
5. Question 5
Who is writing the rock music?
Now that we know that our customers love rock music, we can decide which musicians to invite to play at the concert.
Let's invite the artists who have written the most rock music in our dataset. Write a query that returns the Artist name and total track count of the top 10 rock bands.
You will need to use the Genre, Track , Album, and Artist tables.
```
select  Artist.ArtistId,Artist.Name, count(Track.TrackId) Songs
from Track
join Genre
on Genre.GenreId = Track.GenreId 
join  Album
on Album.AlbumId=Track.AlbumId
join Artist
on Artist.ArtistId=Album.ArtistId
where  Genre.Name = "Rock"
group by Artist.Name
order by Songs desc limit 10
```
6. Question 6
First, find which artist has earned the most according to the InvoiceLines?
Now use this artist to find which customer spent the most on this artist.
For this query, you will need to use the Invoice, InvoiceLine, Track, Customer, Album, and Artist tables.
Notice, this one is tricky because the Total spent in the Invoice table might not be on a single product, so you need to use the InvoiceLine table to find out how many of each product was purchased, and then multiply this by the price for each artist.
```
select  *
from Track
join  Album
on Album.AlbumId=Track.AlbumId
join Artist
on Artist.ArtistId=Album.ArtistId
join InvoiceLine
on Track.TrackId=InvoiceLine.TrackId
join Invoice 
on Invoice.InvoiceId = InvoiceLine.InvoiceId
join Customer
on Customer.CustomerId=Invoice.CustomerId
```
7. Qustion 7
We want to find out **the most popular music Genre for each country. **We determine the most popular genre as the genre with the highest amount of purchases. Write a query that returns each country along with the top Genre. For countries where the maximum number of purchases is shared return all Genres.
For this query, you will need to use the Invoice, InvoiceLine, Customer, Track, and Genre tables.
8. Question 8
Return all the **track names that have a song length longer than the average song length** . Though you could perform this with two queries. Imagine you wanted your query to update based on when new data is put in the database. Therefore, you do not want to hard code the average into your query. You only need the Track table to complete this query.
Return the Name and Milliseconds for each track. Order by the song length with the longest songs listed first.
9. Question 9
Write a query **that determines the customer that has spent the most on music for each country**. Write a query that returns the country along with the top customer and how much they spent. For countries where the top amount spent is shared, provide all customers who spent this amount.
You should only need to use the Customer and Invoice tables.



## Requirement：

1. Four slides

2. One visualization per slide
3. A 1-2 sentence explanation of each slide
The SQL query used to create the data used in the visualization.
4. Note: you may choose to use queries that were motivated by the questions on the previous concepts, or you may choose four entirely new questions. However, if you use any of the previous queries, they must be those that had a **JOIN as stated in the Rubric**.
5. Each SQL query needs to include **one or more aggregation** . This could be a COUNT, AVG, SUM, or other aggregation.
6. http://www.sql-format.com/
> ![](https://s3.cn-north-1.amazonaws.com.cn/u-img/f28cb37a-0a89-4909-9900-4689568c21ec)
7. There shouldn’t be any additional data prep (sorting, filtering, renaming, etc.) between the query output and the visualization.

> /*Query 2 - the query uesd for insights*/
SQL转换为CSV

> Select Export to CSV, and then select the settings that match the ones below. Make sure your setting on New line characters is set to Unix: LF(\n)


