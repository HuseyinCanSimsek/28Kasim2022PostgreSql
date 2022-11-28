# 28Kasim2022PostgreSql
** <h1>28 Kasım 2022 Postresql Ödevi</h1>
## INNER JOIN
```sh
select p.name as "Ürün adı",c.name as "Kategori adı",s.name as "Tedarikçi adı" from suppliers s
inner join products p
on s.supplierid=p.supplierid
inner join products_categories pc
on p.product_id=pc.product_id
inner join categories c
on pc.category_id=c.category_id
where p.name = 'Cola'
```
<h2>Kod Çıktısı</h2>
<img src="https://github.com/HuseyinCanSimsek/28Kasim2022PostgreSql/blob/main/Outputs/inner%20join.png" width=40% height=40%>
  </p>
  
  ## IN

``select ct.name as "Kent",a.street from cities ct 
inner join adresses a
on ct.city_id=a.city_id
where a.street not in('cadde1')
``
<h2>Kod Çıktısı</h2>
<img src="https://github.com/HuseyinCanSimsek/28Kasim2022PostgreSql/blob/main/Outputs/in.png" width=30% height=30%>
  </p>

## GROUP BY AND HAVING
``
select p.stock as "Ürün Stoğu",c.name as "Kategori adı" 
from products p
inner join products_categories pc
on p.product_id=pc.product_id
inner join categories c
on pc.category_id=c.category_id
group by p.stock,c.name
having p.stock > 30
``

<h2>Kod Çıktısı</h2>
<img src="https://github.com/HuseyinCanSimsek/28Kasim2022PostgreSql/blob/main/Having.png" width=30% height=30%>
  </p>
 
## BETWEEN
`select p.stock as "Ürün Stoğu",s.name as "Tedarikçi adı" 
from products p
inner join suppliers s
on p.supplierid=s.supplierid
group by p.stock,s.name
having p.stock between 30 and 100
`

<h2>Kod Çıktısı</h2>
<img src="https://github.com/HuseyinCanSimsek/28Kasim2022PostgreSql/blob/main/Outputs/between.png" width=30% height=30%>
  </p>
