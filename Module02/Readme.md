# Примеры запросов к БД super_sales


__Sales count, Total sales, Total profit__

select count(sales) sales_count , sum(sales) total_sale , sum(profit) total_profit  
from orders o 

<p align="center">	
    <img src="https://github.com/gyllub/DE-101/blob/main/Module02/pic/1.png">
</p>

__Наиболее профитные покупатели__

select
	customer_name ,
	sum(profit) as profit,
	round(sum(profit)/(select sum(profit) from orders\*100,2) profit_percent  
from orders o  
group by customer_name  
order by profit desc  
limit 5

<p align="center">
    <img src="https://github.com/gyllub/DE-101/blob/main/Module02/pic/2.png">
</p>

__Наибольшие суммы возвратов__

select o.customer_name, round(sum (o.sales)) as returned_sale  
from orders o
	inner join "returns" r on o.order_id=r.order_id  
group by o.customer_name  
order by 2 desc  
limit 7  

<p align="center">
    <img src="https://github.com/gyllub/DE-101/blob/main/Module02/pic/3.png">
</p>

__Месяцы с максимальными суммами возвратов__

select to_char(order_date::date, 'month, yyyy') as month, round(sum(sales)) as returned_sale  
from orders o inner join "returns" r on o.order_id =r.order_id  
group by month  
order by returned_sale desc  
limit 7  

<p align="center">
    <img src="https://github.com/gyllub/DE-101/blob/main/Module02/pic/4.png">
</p>

__Максимальные продажи по сегменту и месяцу__

select to_char(order_date::date, 'month, yyyy') as month, segment, round(sum(sales),2) sum_sales  
from orders o  
group by month, segment  
order by 3 desc  
limit 5  

<p align="center">
    <img src="https://github.com/gyllub/DE-101/blob/main/Module02/pic/5.png">
</p>





