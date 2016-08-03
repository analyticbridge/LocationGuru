# LocationGuru
Retail Analytics Prediction test case 
Big  Retailer  is looking for your help in maximizing sales and minimizing returns for their delectable inventory of baked goods. With over 1 million stores across Mexico, the transactional dataset for the Group Inventory Demand competition is huge. 

Accurately predicting each store's demand will make sure customers aren’t staring at empty shelves, while also reducing the amount spent on refunds to store owners with surplus product unfit for sale.

you will forecast the demand of a product for a given week, at a particular store. The dataset you are given consists of 9 weeks of sales transactions in Mexico. Every week, there are delivery trucks that deliver products to the vendors. Each transaction consists of sales and returns. Returns are the products that are unsold and expired. The demand for a product in a certain week is defined as the sales this week subtracted by the return next week.

The train and test dataset are split based on time.

Things to note:
•	There may be products in the test set that don't exist in the train set. This is the expected behavior of inventory data, since there are new products being sold all the time. Your model should be able to accommodate this.
•	There are duplicate Cliente_ID's in cliente_tabla, which means one Cliente_ID may have multiple NombreCliente that are very similar. This is due to the NombreCliente being noisy and not standardized in the raw data, so it is up to you to decide how to clean up and use this information. 
•	The adjusted demand (Demanda_uni_equil) is always >= 0 since demand should be either 0 or a positive value. The reason that Venta_uni_hoy - Dev_uni_proxima sometimes has negative values is that the returns records sometimes carry over a few weeks.
File descriptions
•	train.csv — the training set
•	test.csv — the test set
•	sample_submission.csv — a sample submission file in the correct format
•	cliente_tabla.csv — client names (can be joined with train/test on Cliente_ID)
•	producto_tabla.csv — product names (can be joined with train/test on Producto_ID)
•	town_state.csv — town and state (can be joined with train/test on Agencia_ID)

Data fields
•	Semana — Week number (From Thursday to Wednesday)
•	Agencia_ID — Sales Depot ID
•	Canal_ID — Sales Channel ID
•	Ruta_SAK — Route ID (Several routes = Sales Depot)
•	Cliente_ID — Client ID
•	NombreCliente — Client name
•	Producto_ID — Product ID
•	NombreProducto — Product Name
•	Venta_uni_hoy — Sales unit this week (integer)
•	Venta_hoy — Sales this week (unit: pesos)
•	Dev_uni_proxima — Returns unit next week (integer)
•	Dev_proxima — Returns next week (unit: pesos)
•	Demanda_uni_equil — Adjusted Demand (integer) (This is the target you will predict)


