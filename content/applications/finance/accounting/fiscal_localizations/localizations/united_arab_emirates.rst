====================
United Arab Emirates
====================

.. _uae/installation:

Installation
============

:ref:`Install <general/install>` the following modules to get all the features of the United Arab
Emirates localization:

.. list-table::
   :header-rows: 1

   * - Name
     - Technical name
     - Description
   * - :guilabel:`U.A.E. - Accounting`
     - ``l10n_ae``
     - Default :doc:`fiscal localization package <../overview/fiscal_localization_packages>`. Has all the accounts, taxes, and reports. [Install if you have Accounting]
   * - :guilabel:`U.A.E. - Payroll`
     - ``l10n_ae_hr_payroll``
     - Has all the rules, calculations, and salary structures. [Install if you don’t have Accounting module, but you have payroll]
   * - :guilabel:`U.A.E. - Payroll with Accounting`
     - ``l10n_ae_hr_payroll_account``
     - Has all the  rules, calculations, salary structures, and accounts linked to the rules. [Install if you have Accounting + Payroll]
   * - :guilabel:`U.A.E. - Point of Sale`
     - ``l10n_ae_pos``
     - Has the UAE compliant POS receipt. [Install if you have POS]

Next, go to :menuselection:`Accounting --> Configuration --> Settings`, and double check if the
package is set up in place.

An updated set of accounts is installed within the package. A mix of services-retail applicable
accounts, as well as legal/regulatory [VAT] accounts.

Configure your company
Go to the :menuselection:`Accounting --> Configuration --> Chart of Accounts` and have a look at the
installed chart of accounts. Delete or check the deprecated checkbox in that account’s setup as you
see fit. Finally, feel free to add, edit, or keep any of the accounts as per your needs.

Chart of accounts
U.A.E. - Accounting: Has all the accounts, taxes, and reports. [Install if you have Accounting]

Remember to always keep at least one Receivable account and one Payable account.
Finally, I would advise you to keep the accounts below, since they’re either used as intermediary accounts by Odoo or somewhere in the localization.



Currency Exchange Rates
Currency exchange rates are updated automatically from the UAE Central Bank. The update interval is up to you. To configure this, go to settings and find it under the accounting section.



Journals
To set up your journals, go to Accounting → Configurations → Journals. You can edit/adjust the existing journals to be tailored for your needs. Also feel free to create new journals with the appropriate type (Sales, Purchase, Bank, Cash, miscellaneous) if needed.










Taxes and Tax reports

The tax report is up to date.
Tax closing entries and adjustments are now ready to use.
RCM (Reverse Charge Mechanism) is now supported more than ever.
Taxes
To view the taxes applicable to your localization, go to Accounting → Configurations → Taxes. Then, deactivate, archive, or delete the ones that are not applicable or out of your company’s scope.



Go through the accounts set on your taxes, make sure the types of these accounts represent the nature of the tax type accordingly:


Assign the correct fiscal position to your contacts, so taxes show up properly when you invoice/bill them:


Make sure you are in developer mode and check your tax groups to see the tax closing entries:

Remember to only set accounts on the 5% tax group, other groups do not need closing, then create some Invoices, Journal Entries, and Bills to test.

Tax report
Go to your tax report and try closing the period. The period you set on the settings page is the period used for closing.

.. _uae/payroll:

Payroll
=======

Make sure to :ref:`install the modules you need <uae/installation>`. The guilabel:`U.A.E. - Payroll`
module includes all the rules configured under the UAE Employee Payroll Structure in the Salary
rules section as per the U.A.E rules and regulations.

.. image needed here, but I removed the : in the paragraph before as this image only illustrates.


These rules are linked to the corresponding accounts that are on the Chart of accounts.

To activate these rules to an employee, choose the correct salary structure type UAE Employee (which under it falls the salary structure UAE Employee Payroll Structure with all the salary rules ) on the employee’s contract:

Leave deduction is calculated using a salary rule linked to the unpaid leave time off type, however, any other deduction or reimbursement is done manually using other inputs.

Additionally, overtime is added manually through work entries and finally, Generated from the Salary Attachments Model are the Attachment of Salary, Assignment of Salary, and Child Support.

Note:
Uncheck the appear on payslip checkbox if you do not want the rule to show up in the printed payslip.

Also if you go to any contract, under the Salary Information tab, you can find some fields that appear after installing the localization package such as Wage, Housing allowance, Transportation allowance, and Other allowances as well as the Number of days field which is how the end of service provision is calculated:

:

End of Service Provision and End of Service
The provision is defined as the total monthly allowance / 30 multiplied by the number of days set in the field Number of days shown above.

This provision is then calculated via a salary rule that is associated with two accounts. These accounts are: the End Of Service Indemnity (Expense account) and the End of Service Provision (Non-current Liabilities account). The latter is then used to pay off the End of service amount by settling it with a Payables account.

Note:
The End of service calculations are based on the Basic Salary only as to the United Arab Emirates HR laws. The start and end dates of the employee’s contracts trigger the calculations.
Invoices
Invoices generated while the U.A.E localization is installed can be in English, Arabic, or both. It also includes a line to display the VAT amount per line.