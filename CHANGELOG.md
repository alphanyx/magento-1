# Changelog

## 4.1.4
**Features**

* RatePay B2B Invoice added
* In case of guaratee rejection, Payone Safe Invoice is not displayed again to the customer
* Enforce Amazon Pay redirect mode for in-app browsers (#161, thanks @gndk)
* Sending the overcapture flag for PayDirekt now possible
* RatePay backend orders are now possible
* Automatically recognize credit card type after 6 digits of PAN

**Bugfixes**
* Fixed wrong license identifier in composer.json
* Fixed missing modman directive (#176, thanks @tim-bezhashvyly)
* Fixed "undefined index" problems (#152, thanks @norgeindian; #168, thanks @Schrank)
* Headers are now set correctly when using FastCGI
* Fixed some bugs introduced with Mage 1.9.3.x (#165)
* Re-activated the conversion of reference parameters for PayDirekt to honor disallowed chars
* Removed HTML from backend labels for 1.9.3.8 compat

## 4.1.2
**Features**

* Handle Ratepay unauthorized payment response by disabling the payment method for the customer
* Allow to send registration number instead of birthdate for B2B cases

## 4.1.1
**Feature**

* Completed Amazon Pay background processes
* RatePay orders can now be properly reversed


## 4.1.0
**Feature**

* New payment methods
    * Invoice with payment gurantee
    * Amazon Pay
* Allow quote as parameter in Payone_Core_Model_Payment_Method_Abstract
* Add functionality for recurring payment
* Improve the handling of external payment providers

**Bug**
* Set correct model for default mapping
* Correctly handle payment fee calculation
* Fixed default payment titles for giropay & idl
* Payone_Core_Model_Mapper_ApiRequest_Payment_Authorize_Abstract getCustomerIp() will no return the last ip like described in the comment
* Fixed php notice because array key does not exist
* Payone_Core_Model_Observer_Sales_Order paymentPlaceEnd() will now validate if the user exists
* Fixed url-encoding
