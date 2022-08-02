==============================
Use Different Units of Measure
==============================

In some cases, handling products in different units of measure is necessary. For example, if you
buy products in a country where the metric system is of application and sell in a country where
the imperial system is used, you will need to convert the units. Another common use case is buying
products in bigger packs to your supplier and selling them in units to your customers.

You can set up Odoo to work with different units of measure for one product.

Configuration
=============

In the *Inventory* application, go to :menuselection:`Configuration --> Settings`. In the
*Products* section, activate *Units of Measure*, then *Save*.

.. image:: uom/uom-enable-setting.png
   :align: center
   :alt: Enable Units of Measure in Inventory settings.

Create New Units of Measure
===========================

In the *Inventory* application go to :menuselection:`Configuration --> UoM Categories`.
The category is important for unit conversion, you will be able to
convert products from one unit to another only if those units belong to
the same category.

.. image:: uom/uom-categories.png
   :align: center
   :alt: Set Units of Measure categories in Configuration settings

As an example, we will create a Box of 6 units that we will use for the Egg product.

Hit on the *Unit* category.

Hit *Add a line*. As an example, we will create a Box of 6 units that we will use for the Egg
product. The box of 6 is 6 times bigger than the reference unit of measure for the category which
is “Units” here.

.. image:: uom/convert-products-by-unit.png
   :align: center
   :alt: Convert products from one unit to another as long as they belong to the same category.

Specify Units of Measure on your Products
=========================================

In the :menuselection:`Inventory application --> Master Data --> Products`, open the product which
you would like to change the purchase/sale unit of measure, and click on *Edit*.

In the *General Information* tab, you can select the *Unit of Measure* in which the product will
be sold, which is also the unit in which internal transfers will take place. You can also select
the *Purchase Unit of Measure*, which is the unit in which you purchase the product.

.. image:: uom/internal-uom-vs-purchase-uom.png
   :align: center
   :alt: Specify Units of Measure by use: internal transfer or when the product is purchased.

Transfer from One Unit to Another
=================================

Buy in the Purchase UoM
-----------------------

In the *Purchase* application, *Create* a new request for quotation in which you include the
product with the different *Units of Measure* and *Confirm* it.

.. image:: uom/rfq-with-diff-uom.png
   :align: center
   :alt: A request for quotation illustrating different Units of Measure.

On the automatically generated purchase orders, the UoM used is the Box of 6, meaning the Purchase
UoM. You have of course the possibility to manually modify the UoM if necessary. When you enter the
*Receipt* which is linked to the purchase order, you can observe that the 10 boxes of 6 units have
been converted in 60 units. Indeed, the stock is managed in units.

.. image:: uom/uom-conversion-on-receipt.png
   :align: center
   :alt: Units are converted on purchase order receipts.

Replenishment
-------------

When doing a replenishment via the *Replenish* button on the product form, you have the possibility
to use a different unit of measure.

.. image:: uom/replenish-button-on-product.png
   :align: center
   :alt: The Replenish button on the product allows for different units of measure.

.. image:: uom/replenish-product-uom-settings.png
   :align: center
   :alt: Product replenishment UoM settings.

Sell in bigger UoM
------------------

You can choose the unit of measure on the sale order document and decide to sell the eggs by the
dozen. When doing so, the price is automatically computed from Units UoM to adapt to the selected
*UoM*.

.. image:: uom/sales-order-uom.png
   :align: center
   :alt: Specify Units of Measure on sales orders.

In the delivery order, the *UoM* used in the sale order is converted to the *UoM* used for stock
management, in our use case, the Units.

.. image:: uom/delivery-order-uom-conversion.png
   :align: center
   :alt: Units of Measure conversion on a warehouse order.
