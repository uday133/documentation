====================================================================
When Should you Use Packages, Units of Measure or Special Packaging?
====================================================================

Units of Measure
================

Units of measure specify the unit used to handle a product. In Odoo, you have the possibility to
specify the unit of measure in which you manage your stock and the one which is used when
purchasing the product to your supplier.

.. image:: usage/uom-handling-vs-purchase.png
   :align: center
   :alt: Specify unit of measure for handling a product vs. when it's purchased

The *conversion* between the different units of measure is done automatically. The only condition
is that all the units have to be in the *same category* (Unit, Weight, Volume, Length,...)

For example, if I have the following reordering rule for the egg and I run the scheduler, the
quantity added in the automatically generated purchase order will be in dozens but what will enter
the stock will be units.

.. image:: usage/units-of-measure-conversion.png
   :align: center
   :alt: Units of Measure conversion happens automatically with quantity multiplier field

.. image:: usage/uom-conversion-on-purchase-order.png
   :align: center
   :alt: Units of Measure converts to appropriate quantity on generated purchase orders

.. image:: usage/uom-conversion-by-category.png
   :align: center
   :alt: Units of Measure conversions happen automatically as long as units are in the same category.

Packages
========

The package is the physical container in which you put one or several products from a picking. For
example, when you deliver a product, you can decide to separate the quantity into two different
packages. It then allows you to have a report with the quantity of products for each package.

To separate a delivery into different packages you will have to set the done quantity to the
desired package quantity then click on "PUT IN PACK", do this for each package.

.. image:: usage/separate-delivery-into-different-packages.png
   :align: center
   :alt: Separate delivery into different packages

.. image:: usage/delivery-package-details.png
   :align: center
   :alt: Separate delivery package details

Packagings
==========

The packaging is a standard container containing several units of your  product. If you are selling
cans of soda, the packagings would be a 6-Pack, a 15-Pack or even a pallet.

In Odoo, packagings are used for indicative purposes on sales/purchase orders and transfers. The
main difference between packagings and units of measure is that packagings are defined at product
level while UoMs are generic.

.. image:: usage/product-packaging-examples.png
   :align: center
   :alt: Different product packaging examples

.. image:: usage/package-field-on-po.png
   :align: center
   :alt: Package field on purchase order

.. note::
   Another useful use of the packaging is for product reception. By scanning the barcode of the
   packaging, Odoo adds the number of units contained in the packing on the picking.
