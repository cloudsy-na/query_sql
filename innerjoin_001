with ditem as (
  select
  image.sku,
  image.image_file
  from `mid-internal-systems.pim.pm_image` as image
  )
select item.sku,
item.product_group_code,
item.product_name,
item.model_number,
item.box_no,
brand.brand_name
from `mid-internal-systems.pim.pm_item` as item
left join ditem
on ditem.sku = item.sku
inner join `mid-internal-systems.pim.pm_brand` as brand
ON item.brand_code = brand.brand_code
Where ditem.image_file is NUll AND item.disable=0 AND box_no = 'I0300'

#LIMIT 20
