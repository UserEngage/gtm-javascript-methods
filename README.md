# Official User.com UE Methods Tag for Google Tag Manager

https://user.com/en/integrations/javascript/

##### Update User data using UE methods

Custom javascript methods let you achieve desired goals using only frontend actions. Methods listed below are available though a global window object UE. Depending on your use case, you can pass data inside User.com app in many ways. Using widget methods, you will be able to interact with user much closer updating his data within page hit, initializing widget with a new user or destroying the whole widget instance.



##### User.com | Implementation must be loaded to use UE methods


#### Methods available

- UE.pageHit()
- UE.resetAuth()
- UE.destroy()


**UE.pageHit()**

Within UE.pageHit() methods you can update the user with the same attributes as in window.civchat object (including custom attributes).

UE.pageHit() sends a request to our server and updates a URL (generates new page view) and passed user attributes with certain data. It’s an equivalent of navigating to new page in "standard" HTTP installations.


**UE.resetAuth()**

This function resets __ca__chat cookie, then creates a new one, which results in creating a new user. Parameter data is an object with the api key. Remember, it also resets a global cookie. You can use it to keep users privicy on the higher level. After user log out from your application, you can run this function and without loggin in, this user won’t be able to check conversations history on chat.
You can also provide more information about the new user (ie. email address).


**UE.destroy()**

Destroy current widget instance and remove window from DOM. After the current widget instance has been destroyed, you cannot refer to the UE methods.


#### Configuration

##### Required configuration data

- **API Key**
    - You can find it in your **Application -> Settings -> Setup & Integrations**

##### Optional configuration data

- **User Attributes**
    - Pass data to update standard and custom User attributes
    - Provide standardized attribute names without blank characters, i.e. Do not use First Name, use first_name instead
    - Undefined values will not be passed

- **Console Logs**
    - Select to enable debug console logs.
    - Selection will enable logs in both Preview and Published containers