# TRUNC Date Function<a name="r_TRUNC_date"></a>

Truncates a time stamp and returns a date\.

## Syntax<a name="r_TRUNC_date-synopsis"></a>

```
TRUNC(timestamp)
```

## Arguments<a name="r_TRUNC_date-arguments"></a>

 *timestamp*   
A timestamp column or an expression that implicitly converts to a time stamp\.  
To return a time stamp value with `00:00:00` as the time, cast the function result to a TIMESTAMP\.

## Return Type<a name="r_TRUNC_date-return-type"></a>

DATE

## Examples<a name="r_TRUNC_date-examples"></a>

Return the date portion from the result of the SYSDATE function \(which returns a time stamp\): 

```
select sysdate;

timestamp
----------------------------
2011-07-21 10:32:38.248109
(1 row)

select trunc(sysdate);

trunc
------------
2011-07-21
(1 row)
```

Apply the TRUNC function to a TIMESTAMP column\. The return type is a date\. 

```
select trunc(starttime) from event
order by eventid limit 1;

trunc
------------
2008-01-25
(1 row)
```