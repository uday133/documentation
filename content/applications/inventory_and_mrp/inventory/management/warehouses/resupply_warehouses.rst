===============================
Resupply from another Warehouse
===============================

A common use case for multiple warehouses is to have one central warehouse that resupplies shops,
each shop is considered as a local warehouse. When a shop want to replenish a product, this product
is ordered to the central stock. Odoo allows you to set easily which warehouse(s) can resupply a
warehouse.

Configuration
=============

In order to be able to resupply from another warehouse, you need to activate *multi-step routes*.

.. image:: resupply_warehouses/virtual-warehouses-settings.png
   :align: center
   :alt: Enable Multi-Step Routes in Odoo settings

You can then access your warehouses via :menuselection:`Inventory --> Configuration -->
Warehouses`.

Open the warehouse which should be resupplied by the another one. You will have the possibility to
directly indicate through which warehouse(s) it can be resupplied.

.. image:: resupply_warehouses/resupply-from-second-warehouse.png
   :align: center
   :alt: Supply one warehouse with another in Warehouse Configuration tab.

By activating this option, a new route will now be available on your products *Supply Product from
Second warehouse*. It can now be selected, along with either a *reordering rule* or a *make to
order*.

.. image:: resupply_warehouses/product-resupply-route-settings.png
   :align: center
   :alt: Route setting which enables a product to resupplied from a second warehouse.

In this example, a reordering rule is set with a minimum of 5 units in stock and a maximum of 10
units in stock, having currently 0 units on hand.

The system automatically creates two pickings, one *delivery order* from my Second Warehouse which
contains the necessary products, and a receipt in my main warehouse WH/Stock for the same products.
The source document is the *reordering rule* which triggered the route *Supply Product from Second
warehouse*. The location between the delivery and the receipt is a transit location.

.. image:: resupply_warehouses/resupply-receipts-from-reordering-rule.png
   :align: center
   :alt: A reordering rule automatically creates two receipts for stock between warehouses.

.. image:: resupply_warehouses/second-warehouse-delivery-order.png
   :align: center
   :alt: A warehouse order for resupplying one warehouse's stock with another.

.. image:: resupply_warehouses/second-warehouse-stock-receipt.png
   :align: center
   :alt: A receipt for stock received to one warehouse from another.
