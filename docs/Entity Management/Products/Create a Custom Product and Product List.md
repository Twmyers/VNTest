



# Create a Custom Product and Product List

In addition to the default products in
Value
Navigator, you can create your own products. You can decide
whether to allow declines for your products or whether to include them
in your reserves.



When you create a custom product, you must assign it to a Product List
in order to add the custom product to an entity. See the procedure
below.



When you create a custom product, the product is displayed on the Import
Codes tab of the Products dialog box. If you are able to import
production or injection data for your custom product (from a data vendor
such as IHS or geoScout), you need to assign it an import code. See
[Assign an Import Code to a Product](Assign%20an%20Import%20Code%20to%20a%20Product.md) .

To create a custom product

1.  In the **Tools** menu, point to **Global Project Data** and click
    **Products**.
2.  Click **Add**.
3.  Complete the following fields:
    | Field | Description |
    |----|----|
    | Name | Enter a name for the product. |
    | Product Class | Select **Production** or **Injection** |
    | Unit Type | The unit type determines the units you can select. |
    | Imperial Unit | Default Imperial unit for the product. |
    | Metric Unit | Default Metric unit for the product. |
    | Imperial prices/costs | Default Imperial prices and costs for the product. |
    | Metric prices/costs | Default Imperial prices and costs for the product. |
    | Colour | Determines the colour of the decline (if you select **Allow Decline**). |
    | Include in volume equivalence calculation | Includes the product volumes in the calculated BOE. This option is not editable for default products. It is editable for custom products with Gas Volume or Liquid Volume selected for the Unit Type. |
    | Allow decline | Enables you to add a decline for the product on **Predictions \| Declines**. |
4.  Click the **Product Lists** tab.
5.  Do one of the following: 
    | To                                           | Do this       |
    |----------------------------------------------|---------------|
    | Create a Product List,                       | Go to step 6. |
    | Add the product to an existing product list, | Go to step 8. |
6.  Click **Add**.
7.  Complete the following fields:
    | Field           | Description                     |
    |-----------------|---------------------------------|
    | Name            | Enter a name for the list.      |
    | Description     | Enter a description (optional). |
    | Primary Product | Select the primary product.     |
8.  Move your new product (and any other products you want included in
    the new product list) from the Available
    column to the Selected column.
9.  Click **OK**.

You can also edit product ratios on the **Ratio** tab or add import
codes to the product on the **Import Codes** tab.
