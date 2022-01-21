# oss_bop_bzst_csv
Jupyter notebook to create the csv file to upload transactions into the BOP portal of the German Federal Central Tax Office (BZSt) in order to create the EU OSS declaration.

Please note that this is just a quick and dirty solution. There are some verifications included in the notebook. However, when using it, you should always double check the OSS declaration with the original source data, if the csv file is accepted by the BOP portal. Also, please note that there are no verification methods of the vat rates and VAT ids included. 

In order to upload the file with the raw in the notebook, use the excel template 'input_template.xlsx' which must have following columns and input:

- supply_of: 'goods' or 'services'

- fictitious_supply_by_marketplace: '0' default or '1' if marketplace is fictitiously involved in the supply chain 

- origin_country: alpha-2 code of the country where the transport/dispatch starts or where the services are supplied from, respectively

- origin_country_vat_id: vat id number of the country where the transport/dispatch starts or where the services are supplied from, respectively

- origin_country_tax_number: in alternative cases, if there is no VAT ID, the tax number assigned to the fixed establishment where the services are supplied from

- destination_country: alpha-2 code of the country where the transport/dispatch ends or where the services are supplied to (where the private customer resides), respectively

- vat_rate: applicable vat rate of the destination_country

- net_amount: net amount

Input may be included on a line-by-line basis (i.e.; one sales/refund one line) or already consolidated.

