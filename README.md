# What factor(s) determine the price of a car?

Data Preparation

Originally, the data containied 426880 records with the following columns:

id, region, price, year, manufacturer, model, condition, cylinders, fuel, odometer, title_status, transmission, VIN, drive, size, type, paint_color, size

On initial inspection, using 'VIN', 'price' & 'odometer', the data contained 215109 duplicate rows which were removed (keeping one copy). The following column were dropped as they did not contain useful information: 'id', 'VIN', 'size', 'cylinders','condition','drive','paint_color','type'. After type conversion, the categorical data was encoded ('region', 'transmission','fuel','odometer','model','title_status','manufacturer','state') using OrdinalEncoder. Rows with a price <= 1,000 and > 25,000 were also removed (the decision for this, and the following, modification came after a histogram of the remaining columns to identify outliers). Rows with 'year' < 1925 were also removed. Finally, rows with 'odometer' < 1,000 and > 400,000 were also dropped. This resulted in a data set of 135395 rows.

Histogram of the data:

[TODO: insert 1]
