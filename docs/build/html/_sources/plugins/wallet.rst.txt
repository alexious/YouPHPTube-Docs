What is it
==========

It is a virtual wallet that you can store some credits, to use on the
YouPHPTube. you probably need some other plugins to be able to spend
those credits.

This is quite interesting to avoid third parties fees.

Manual Requests
===============

On every manual request the specified email on the configuration will be
notified about the request. ## Add Funds This option is in case the site
receives payment in other ways defined by the administrator.

In this case when the user makes the payment he must notify by the site
that the payment was made. so the administrator can approve or cancel
the request.

If the payment is approved, the credit is automatically added to the
user's wallet.

Withdraw Funds
--------------

When a user request a withdraw, the requested balance is automatic
removed from the user wallet and the transaction will be pending on the
user history.

If the Admin set this history log to Cancel the credit will be refund to
the user, otherwise the credit goes to the admin wallet.

Configuration Options
=====================

-  decimalPrecision = The decimal precision of the currency you will use
   in your site
-  wallet\_button\_title = The top button title;
-  add\_funds\_text = The text that appear on the automatic add page
   (PayPal);
-  add\_funds\_success\_success = Text used in case of automatic add
   funds success;
-  add\_funds\_success\_cancel = Text used in case of automatic add
   funds cancel;
-  add\_funds\_success\_fail = Text used in case of automatic add funds
   fail;
-  transfer\_funds\_text = Text used on the transfer page;
-  transfer\_funds\_success\_success = Text used in case of transfer
   funds success;
-  transfer\_funds\_success\_fail =Text used in case of transfer funds
   fail;
-  withdraw\_funds\_text = Text used on withdraw page;
-  withdraw\_funds\_success\_success = Text used in case of withdraw
   funds success;
-  withdraw\_funds\_success\_fail = Text used in case of withdraw funds
   success;
-  currency = Currency abbreviation (USD);
-  currency\_symbol = "$";
-  addFundsOptions = an JSON array with the values options to add funds;
-  showWalletOnlyToAdmin = check this in case you want only admin to see
   the wallet on the top;
-  CryptoWalletName = Each user can add an Crypto currency wallet
   address, and that is the name we will label it;
-  enableAutomaticAddFundsPage = Enable this in case you want to use
   PayPal;
-  enableManualAddFundsPage = Enable this in case you want a manual add
   funds option (useful to use your own currency);
-  manualAddFundsMenuTitle = The menu label;
-  manualAddFundsPageButton = The confirm button label;
-  manualAddFundsNotifyEmail = The email where we will notify the add
   funds request;
-  manualAddFundsTransferFromUserId = The user ID that we will use to
   transfer funds in case a add funds request is approved;
-  enableManualWithdrawFundsPage = Enable this in case you want a manual
   add withdraw option (useful to use your own currency);
-  withdrawFundsOptions = an JSON array with the values options to
   withdraw funds;
-  manualWithdrawFundsMenuTitle = The menu label;
-  manualWithdrawFundsPageButton = The confirm button label;
-  manualWithdrawFundsNotifyEmail = The email where we will notify the
   withdraw funds request;
-  manualWithdrawFundsTransferToUserId = The user ID that we will use to
   transfer funds in case a withdraw funds request is approved;
