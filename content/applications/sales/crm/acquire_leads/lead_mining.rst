===========
Lead mining
===========

Lead mining is a feature that allows CRM users to generate new leads directly into their Odoo
database. To ensure lead qualification, lead mining output is determined by variety of filtering
criteria, such as the country, the company size, and the industry.

Configuration
=============

To get started, go to :menuselection:`CRM --> Configuration --> Settings` and activate
:guilabel:`Lead Mining`.

.. image:: lead_mining/activate-lead-mining.png
   :align: center
   :alt: Activate lead mining in Odoo CRM settings

Start generating leads
======================

After the lead mining setting is activiated, a new button :guilabel:`Generate Leads`, is available
to use in the pipeline. Lead mining requests are also available from :menuselection:`Configuration
--> Lead Mining Requests` or through :menuselection:`Leads --> Leads` where the :guilabel:`Generate
Leads` button is also available.

.. image:: lead_mining/generate-leads-button.png
   :align: center
   :alt: Generate Leads button to use lead mining feature

From either dashboard, click on the :guilabel:`Generate Leads` button, and a window will appear
offering a variety of criteria to choose from.

.. image:: lead_mining/generate-leads-popup.png
   :align: center
   :alt: Pop-up window with selection criteria in order to generate leads in Odoo

When choosing to target Companies and their contacts, there is an option to filter leads based on
:guilabel:`Role` or :guilabel:`Seniority`.

.. note::
   Make sure to be aware of the latest EU regulation when receiving contact information. Get more
   information about General Data Protection Regulation on `Odoo GDPR <http://odoo.com/gdpr>`__,

Additional filtering options include:

- :guilabel:`Size`: define the range of employees for the companies criteria
- :guilabel:`Countries`: define leads by the country (or countries) they are located in
- :guilabel:`States`: further define leads geolocation criteria by state, if applicable
- :guilabel:`Industries`: define specific scope(s) of industry where leads work in
- :guilabel:`Sales Team`: choose which Sales Team the leads will be assigned to
- :guilabel:`Salesperson`: choose which person(s) on the Sales Team the leads will be assigned to
- :guilabel:`Default Tags`: choose what tags are added directly to the leads once found

Pricing
=======

Lead mining is an In-App Purchase feature and each generated lead costs one credit.

Choosing to receive contact information from each lead will also cost one additional credit.

.. note::
   See here for full pricing information `feature Lead Generation by Odoo IAP
   <https://iap.odoo.com/iap/in-app-services/167?>`__.

To buy credits, navigate to :menuselection:`CRM --> Configuration --> Settings --> Buy
Credits`.

.. image:: lead_mining/buy-lead-mining-credits-setting.png
   :align: center
   :alt: Buy credits from lead mining settings

Alternatively, credits may also be purchased by navigating to :menuselection:`Settings -->
In-App Purchases --> View my Services`.

.. image:: lead_mining/buy-lead-mining-credits-iap.png
   :align: center
   :alt: Buy credits via In-app Purchase settings

.. tip::

   - Consumed credits dynamically display in real-time how many credits the current settings need.
   - If you are on Odoo Online (SaaS) and have the Enterprise version, you benefit from free trial
     credits to test the feature.

.. seealso::
   * :doc:`../../../general/in_app_purchase`
