==========
Using Kits
==========

A *kit* is a set of unassembled components. Kits may be sold as products, but are also useful tools
for managing more complex bills of materials (BoMs). To use kits, the :guilabel:`Manufacturing` and
:guilabel:`Inventory` applications need to be installed.

Creating the kit as a product
=============================

To use a kit as a sellable product or simply as a component organization tool, the kit should first
be created as a product. To create a kit product, go to :menuselection:`Manufacturing or Inventory
--> Products --> Products`, then click :guilabel:`Create`.

Next, set the :guilabel:`Product Type` to :guilabel:`Storable Product`: this allows for management
of kit inventory. The :guilabel:`Route` designation under the :guilabel:`Inventory` tab for the kit
product does not matter, since Odoo uses the routes of the kit’s components for replenishment
purposes. All other parameters for the kit product may be modified according to preference.
Finally, click :guilabel:`Save`.

The kit’s components require no specific configuration. 

Setting up the kit BoM
======================

After fully configuring the kit product and its components, create a BoM for the kit product. Go to
:menuselection:`Manufacturing --> Products --> Bills of Materials`, then click :guilabel:`Create`.
Next, set the :guilabel:`BoM Type` to :guilabel:`Kit`. Finally, add each component and specify its
quantity. Make sure to :guilabel:`Save` the changes.

.. image:: kit_shipping/bom-kit-selection.png
   :align: center
   :alt: Kit selection on the bill of materials. 

If the kit is solely being used as a sellable product, then only components need to be added, and
configuring manufacturing operations is not necessary.

.. note:: When a kit is sold as a product, it appears as a single line item on the quotation and
    sales order. However, on delivery orders, each component of the kit is listed. 

Using kits to manage complex BoMs 
=================================

Kits are also used to manage *multilevel BoMs*. These are products that contain other products as
components and therefore require nested BoMs. Incorporating pre-configured kits into multilevel BoMs
allows for cleaner organization. List a kit as a component in a higher-level product’s BoM to
eliminate the need to add the kit’s parts individually, as illustrated below by the Custom Computer
Kit in the Custom Server BoM.

.. image:: kit_shipping/multilevel-bom-kit.png
   :align: center
   :alt: Kit as a component in a multilevel bill of materials. 

To access a comprehensive overview of the multilevel BoM's components, click on the
:guilabel:`Structure & Cost` smart button. Sublevel BoMs can be expanded and viewed from this
report. 

.. image:: kit_shipping/structure-and-cost-kit.png
   :align: center
   :alt: Expanded kit in the Structure and Cost report. 

When creating a manufacturing order for a product with a multilevel BoM, the kit product
automatically expands to show all components. Any operations in the kit’s BoM are also added to the
list of work orders on the manufacturing order. 
