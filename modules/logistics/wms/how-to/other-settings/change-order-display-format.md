# Change order display format

You have the ability to specify exactly what kind of information is displayed on the first line of each of your **orders** in the WMS Worker.

This can be achieved using a **configuration key** specified in an appropriate **[string interpolation](https://docs.erp.net/tech/advanced/string-interpolation/index.html?q=string)** format.

![picture](pictures/Order_information_09_02.png)

Having access to order data before you even take it allows you to instantly learn what it's about even if a few basic details are provided.

## How to do it

To change the information displayed on the first line of your orders, you need to edit the **OrderDisplayFormat** config key.

You can learn more about it in the **[Config options reference](https://docs.erp.net/tech/reference/config-options-reference.html#55-wmswms-workerorderdisplayformat)**.

![picture](pictures/Core_config_11_02.png)

Once you open the key, change its **Key Value** using appropriate **[string interpolation](https://docs.erp.net/tech/advanced/string-interpolation/index.html?q=string)** notation. 

![picture](pictures/Config_key_value_13_02.png)

Based on what you provide for **Key Value**, different information will be displayed on the first line of all of your orders in the **WMS Worker**.

![picture](pictures/Order_Warehouse_13_02.png)

### Behavior in particular cases 

Here is the expected behavior of changing the order display format in certain cases:

•	If there is **no** config key set, the information displayed will be retrieved from the **To Party** field. This is the default behavior.

•	If there is a key set, but the **Key Value** field is left blank, the displayed information will also be retrieved from **To Party** field.

•	If there is a config key set, but the assigned parameters are **not** returning any value, the displayed information is going to be “-“.
