Add Pipeline Step to Apply Mappings
===========================================================

The second *pipeline step* applies the *value mapping set* you 
configured in :doc:`add-value-mapping-set`.

1. Navigate to the *pipeline* **City Info from File to City Info Item Sync Pipeline**.
2. Add the following item:

    +-------------------+---------------------------------------------------------------------+
    | Template          | **Apply Mapping Pipeline Step**                                     |
    +-------------------+---------------------------------------------------------------------+
    | Name              | **Apply Mapping**                                                   |
    +-------------------+---------------------------------------------------------------------+

3. Set the following field values:

    +---------------------------------+---------------------------------------------------------------------+
    | Field                           | Value                                                               |
    +=================================+=====================================================================+
    | Mapping set                     | **Value Mapping Sets > File Row City to Sitecore City Item**        |
    +---------------------------------+---------------------------------------------------------------------+

4. Save the item.
