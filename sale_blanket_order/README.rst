===================
Sale Blanket Orders
===================

.. !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-AGPL--3-blue.png
    :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fsale--workflow-lightgray.png?logo=github
    :target: https://github.com/OCA/sale-workflow/tree/14.0/sale_blanket_order
    :alt: OCA/sale-workflow
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/sale-workflow-14-0/sale-workflow-14-0-sale_blanket_order
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runbot-Try%20me-875A7B.png
    :target: https://runbot.odoo-community.org/runbot/167/14.0
    :alt: Try me on Runbot

|badge1| |badge2| |badge3| |badge4| |badge5| 

A blanket order is a pre-agreement to sell a certain number of quantities of
products at a specific price. From a confirmed blanket order, the users can
create new sale orders at such price, until the blanket order expires, either
due to reaching the validity date or exhausting all the quantities of products.

**Table of contents**

.. contents::
   :local:

Usage
=====

A new menu in the Sales area is created, allowing users to create new blanket orders.

To create a new Sale Blanket Order go to the sale menu in the Sales section:

.. figure:: https://raw.githubusercontent.com/OCA/sale-workflow/14.0/sale_blanket_order/static/description/BO_menu.png
    :alt: Blanket Orders menu

Hitting the button create will open the form view in which we can introduce the following
information:

* Vendor
* Salesperson
* Payment Terms
* Validity date
* Order lines:
    * Product
    * Accorded price
    * Original, Ordered, Invoiced, Received and Remaining quantities
* Terms and Conditions of the Blanket Order

.. figure:: https://raw.githubusercontent.com/OCA/sale-workflow/14.0/sale_blanket_order/static/description/BO_form.png
    :alt: Blanket Orders form

From the form, once the Blanket Order has been confirmed and its state is open, the user can
create a Sale Order, check the Sale Orders associated to the Blanket Order and/or
see the Blanket Order lines associated to the BO.

.. figure:: https://raw.githubusercontent.com/OCA/sale-workflow/14.0/sale_blanket_order/static/description/BO_actions.png
    :alt: Actions that can be done from Blanket Order

Hitting the button Create Sale Order will open a wizard that will ask for the amount of each
product in the BO lines for which the Sale Order will be created.

.. figure:: https://raw.githubusercontent.com/OCA/sale-workflow/14.0/sale_blanket_order/static/description/PO_from_BO.png
    :alt: Create Sale Order from Blanket Order

Installing this module will add an additional menu which will show all the blanket order lines
currently defined in the system. From this list the user can create customized Sale Orders
selecting the lines for which the PO (or POs if the customers are different) is (are) created.

.. figure:: https://raw.githubusercontent.com/OCA/sale-workflow/14.0/sale_blanket_order/static/description/BO_lines.png
    :alt: Blanket Order lines and actions

In the Sale Order form one field is added in the PO lines, the Blanket Order line field. This
field keeps track to which Blanket Order line the PO line is associated. Upon adding a new product
in a newly created Sale Order a blanket order line will be suggested depending on the following
factors:

* Closer Validity date
* Remaining quantity > Quantity introduced in the Sale Order line

.. figure:: https://raw.githubusercontent.com/OCA/sale-workflow/14.0/sale_blanket_order/static/description/PO_BOLine.png
    :alt: New field added in Sale Order Line

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/sale-workflow/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us smashing it by providing a detailed and welcomed
`feedback <https://github.com/OCA/sale-workflow/issues/new?body=module:%20sale_blanket_order%0Aversion:%2014.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Acsone SA/NV

Contributors
~~~~~~~~~~~~

* André Pereira <github@andreparames.com> (https://www.acsone.eu/)
* Adrià Gil Sorribes <adria.gil@forgeflow.com> (https://www.forgeflow.com/)
* Jordi Ballester Alomar <jordi.ballester@forgeflow.com>
* Alex Comba <alex.comba@agilebg.com> (https://www.agilebg.com/)

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

This module is part of the `OCA/sale-workflow <https://github.com/OCA/sale-workflow/tree/14.0/sale_blanket_order>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
