# mongodb-amazon-price-scraper
This is a python data pipeline notebookto extract Amazon's product and seller data and upload it to a MongoDB database using Pymongo.

Keepa data's entry point is through either a product ASIN, or a seller ID. This pipeline is focussed on product-first approach. We extract 1000 products for each product category first. This product data also loads in the IDs for the sellers who sold that product. Then the code gets the data for each individual seller and loads that in.


The keepauploader_products_us.ipynb is the first file to be run in the process. This file extracts the data for the individual products. Once we extract the products data, the keepauploader_sellers_us.ipynb file is then run to get the seller IDs from the product data and extract seller data and load into the seller data tables.
