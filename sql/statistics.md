Create a simple table with an ID and a number value (float8 means "floating point, 8 bytes (= 8 * 8 = 64 bits)" precision).
See https://float.exposed to see more about how floating point numbers are constructed.

```
create table stats (id bigserial primary key, value float8);
```

This table will be empty at first, so let's put some numbers in it.

```
insert into stats (value) select random_normal(0.5, 0.1) from generate_series(1,100);
```

This should show something like:

```
INSERT 0 100
```

and you can run this to see what's in the table now:

```
select * from stats;
```
You can get the average using the `avg` function:

```
select avg(value) from stats;
```

which should show something like:

```
        avg         
--------------------
 0.5102796738426547
(1 row)
```


You can also find the mean (average) by adding everything up and dividing by the count:

```
postgres=# select sum(value) from stats;
        sum        
-------------------
 51.02796738426547
(1 row)

postgres=# select sum(value)/count(value) from stats;
      ?column?      
--------------------
 0.5102796738426547
(1 row)
```


Smallest and largest:

```
select min(value), max(value) from stats;
```

With a normal distribution, you'll probably see about 0.25 and 0.75 as the smallest and largest, respectively:

```
         min         
---------------------
 0.27882517761616954
(1 row)
        max         
--------------------
 0.7954177917840675
(1 row)
```

For median, that's the 50th percentile:

```
postgres=# select percentile_cont(0.5) within group (order by value) from stats;
   percentile_cont   
---------------------
 0.49549565148808017
(1 row)
```

This is collecting the items, sorting them by the numerical value, then looking for the number 0.5/1.0 (half-way) down the list.
You can reverse it - `(order by value desc)` will swap the meaning, so the result for `0.25` would look like the one for `0.75` going in the other directoin.

Other percentiles (and quartiles) can be useful - 25th (25% of the numbers are smaller than this) and 75th (75% of the numbers are smaller than this), for example:

```
postgres=# select percentile_cont(0.25) within group (order by value) from stats;
  percentile_cont   
--------------------
 0.4260711003051616
(1 row)

postgres=# select percentile_cont(0.75) within group (order by value) from stats;
  percentile_cont   
--------------------
 0.5819326686558256
(1 row)
```

95th and 99th percentile are a good way of finding out what the highest _reasonable_ number is, if you ignore anything that's unusually big.

```
select percentile_cont(0.95) within group (order by value) from stats;
```
