# 28Kasim2022PostgreSql
** <h1>28 Kasım 2022 Postresql Ödevi</h1>
## INNER JOIN
```
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
### IN
```
select ct.name as "Kent",a.street from cities ct 
inner join adresses a
on ct.city_id=a.city_id
where a.street not in('cadde1')
```
<h2>Kod Çıktısı</h2>
<img src="https://github.com/HuseyinCanSimsek/28Kasim2022PostgreSql/blob/main/Outputs/in.png" width=40% height=40%>
  </p>


