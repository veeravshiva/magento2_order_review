OAG - Magento 2 Order Review module

This module is developed by oriolauge, Plugin is sending the Email with Admin URL and we have updated files to send order review email with baseURL without admin URL.

This module adds the next feature: A customer, X days after creating a sales' order in Magento 2's ecommerce, will recieve an email with a link to add a review of his experience. The values that we evaluate are:

Shipping
Product
Customer Support
Comment (optional)
All reviews are saved in a database table that the Magento admin user needs to moderate in order to decide if the review is verified to show or not in https://your_website_name/reviews. This moderation should be done in the magento backoffice.

Technologies
This module was created with:

Magento 2.3.2+ CE
PHP 7.1+
Install
To install this module, we used the next method:

cd MAGENTO_ROOT_PATH
cd app
cd code (maybe you need to create the code folder with mkdir code command)
mkdir OAG
mkdir OAG/OrderReview
cd OAG/OrderReview
drop this repository in your current path (app/code/OAG/OrderReview)
After this commands, you will need to install the module with the following command: php bin/magento setup:upgrade.

Cronjob
This module has a cronjob that sends the emails to the customers. Even so, if you want to execute the cronjobs manually, you can use the next command:

cd MAGENTO_ROOT_PATH
php bin/magento cron:run --group oag_order_review