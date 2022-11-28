# 28Kasim2022PostgreSql
** 28 Kasım 2022 Postresql Ödevi
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

