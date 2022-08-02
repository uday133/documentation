=======================================================
Integrating additional costs to products (landed costs)
=======================================================

The landed cost feature in Odoo allows to include additional costs (shipment, insurance, customs
duties, etc.) into the cost of the product.

Configuration
=============

First, you need to go in :menuselection:`Inventory --> Configuration --> Settings` and activate the
landed costs feature. You can also determine the default journal in which the landed cost
accounting entries will be recorded.

.. image:: integrating_landed_costs/landed-costs-setting.png
   :align: center
   :alt: Activate the landed cost feature in Inventory Settings

Add costs to products
=====================

Receive the vendor bill
-----------------------

Let's imagine I receive a bill from custom duties for a shipment. I'll tick the box *Landed Costs*
on the vendor bill line.

.. image:: integrating_landed_costs/landed-costs-field-vendor-bill.png
   :align: center
   :alt: Enable Landed Costs field on vendor bill line.

.. note::
   The landed cost product must be of type service.

If this product is always a landed cost, you can also define it on the product and avoid having to
tick the box on each vendor bill.

.. image:: integrating_landed_costs/define-landed-cost-on-product.png
   :align: center
   :alt: Option to define a product as always a landed cost

At the top of my vendor bill, I'll see a button *create landed costs*. I click on this button and a
landed cost is automatically created. I can now decide on which picking those additional costs
should apply.

.. image:: integrating_landed_costs/warehouse-transfer-landed-costs.png
   :align: center
   :alt: Using a warehouse transfer to cover a landed cost in the accounting journal.

I can now click on *Compute* and go in the tab *Valuation Adjustments* to see the impact on my
products costs. The last step is to validate the landed cost.

I can access the journal entry that has been created by the landed cost by clicking on the journal
entry.

.. image:: integrating_landed_costs/landed-cost-journal-entry.png
   :align: center
   :alt: Landed cost journal entry

.. note::
   You are not forced to start from the vendor bill, you can also go in :menuselection:`Inventory
   --> Operations --> Landed Costs` and directly create the landed cost from there.