=================
Internal Transfer
=================

In Odoo, a company with at least two bank accounts or cash registers can handle internal money
transfers in a few clicks.

Configuration
=============

An internal transfer account is automatically created on your database based on your company
localization and depending on your country’s legislation. If needed, the default :guilabel:`Internal
transfer account` can be modified going to :menuselection:`Configuration ‣ Settings` and then under
the :guilabel:`Default Accounts` section.

.. note::
   At least two bank accounts are needed to make internal transfers. Please refer to :ref:`this
   documentation <interbank/import-and-reconcile>` to see how to add an additional bank account to
   your database.

Register an internal transfer from one bank to another - use case
=================================================================

Let's make an internal transfer for a company that has two bank accounts registered on its database.
We want to make a transfer of 1.000 USD from Bank A to Bank B account.

Log an internal transfer
------------------------

From the accounting dashboard, click on ⋮ on one of your banks.  In the :guilabel:`New` column click
on :guilabel:`Internal Transfer` and enter the information related to the transfer.

.. image:: interbank/internal_transfer.png
   :align: center
   :alt: Fill in the information related to your internal transfer

.. note::
   Fill in the :guilabel:`Memo` field for automatic reconciliation.

:guilabel:`Save` and :guilabel:`Confirm` to register your internal transfer. The money is now booked
in the transfer account and another payment is **automatically** created in the destination journal
(Bank B).

Bank journal (Bank A)
~~~~~~~~~~~~~~~~~~~~~

.. list-table::
   :header-rows: 1
   :stub-columns: 1

   * - **Account**
     - **Debit**
     - **Credit**
   * - Outstanding Payments account
     -
     - $1.000
   * - **Internal transfer account**
     - **$1.000**
     -

Automated booking - Bank journal (BANK B)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. list-table::
   :header-rows: 1
   :stub-columns: 1

   * - **Account**
     - **Debit**
     - **Credit**
   * - Outstanding Receipts account
     - $1.000
     -
   * - **Internal transfer account**
     -
     - **$1.000**

.. note::
   There are one outstanding payment and one outstanding receipt pending in your two bank account
   journals, because we did not book yet the bank statement confirming the sending and receiving of
   the money.

.. image:: interbank/outstanding-payments-receipts.png
   :align: center
   :alt: Outstanding Payments/Receipts pending bank statement booking

.. _interbank/import-and-reconcile:

Import bank statements and reconcile
------------------------------------

The next step is to book the bank statements to finalize the transaction. Fill in your
:guilabel:`Transactions line`. Once done, Odoo displays a :guilabel:`Computed Balance` which is the
theoretical end balance of your bank account. If it’s corresponding to the bank statement, it means
that no errors were made. Fill in the :guilabel:`Ending balance` and click on the
:guilabel:`Reconcile` button.

.. image:: interbank/transactions-line.png
   :align: center
   :alt: Transaction lines to be filled in prior to reconciliation

The following window opens and you need to choose counterparts for the payment. In our case, the
outstanding payment account. Then :guilabel:`Validate`.

.. image:: interbank/bank-reconciliation.png
   :align: center
   :alt: Reconcile your payment

Bank journal entry
~~~~~~~~~~~~~~~~~~

.. list-table::
   :header-rows: 1
   :stub-columns: 1

   * - **Account**
     - **Debit**
     - **Credit**
   * - Outstanding Payment
     - $1.000
     -
   * - Bank Account (BANK A)
     -
     - **$1.000**

The same steps must be repeated once you receive the bank statement related to bank B. Book and
reconcile your bank statement lines.

Bank journal entry
~~~~~~~~~~~~~~~~~~

.. list-table::
   :header-rows: 1
   :stub-columns: 1

   * - **Account**
     - **Debit**
     - **Credit**
   * - Outstanding Receipt
     -
     - $1.000
   * - Bank Account (BANK B)
     - **$1.000**
     -