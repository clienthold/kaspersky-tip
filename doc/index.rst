Kaspersky TIP API documentation
===============================

`Kaspersky Threat Intelligence Portal <https://opentip.kaspersky.com/>`_ unofficial **API** for Python

✨ Features
************

- **Unlimited** searches and uploads
- Search by **hash** (md5, sha1, sha256)
- Search by **IP address**
- Search by **domain**
- Search by **URL**
- Upload **samples**

📥 Installation
*****************

.. code:: python

   pip install kasperskytip

▶️ Getting Started
******************

.. code:: python

   import kasperskytip

   ks = kasperskytip.kaspersky_tip()
   site = ks.search("google.com")

   print(site.is_safe)
   >>> True

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   pages/search-by.rst
   pages/upload-file.rst
   pages/exceptions.rst