## eNETS_QR_Demo_Android
This repository will get you a copy of the project up and running on your local machine for development and testing purposes.
**Does not** show interaction with merchant portal.

See [development portal](https://api-developer.nets.com.sg/) for a complete guide on how to deploy the project on a live system.

## Main implementation
**1. AndroidManifest.xml**

Take note of the additional permissions added.
```
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="com.nets.netspay.QR_TRANSACTION"/>
```
        
**2. build.gradle(Module: app)**

A few additional dependencies, namely:

```
implementation 'com.squareup.retrofit2:retrofit:2.4.0'
implementation 'com.squareup.retrofit2:converter-gson:2.4.0'
```         
**3. MainActivity.java**

HTTP POST to NETS endpoint for a basic "order request".

**4. SignatureGenerator.java**

Used for generating your signature. In actually production environment, the signature should be generated on the merchant portal. However, for this sample application, the implementation is shown in the application.

## Basic Functionalities
1. Sends a HTTP POST (async) message to eNETS endpoint.

2. Receives and parses the response into POJO.

3. Allows alteration and editing of the payload.

4. Generate the corresponding signature.

5. Calls NETSPay application, passing in QR-code with the added Bundle.

6. Implements corresponding actions.

## Built With

* [Android Studio 3.0.1](https://developer.android.com/studio/)

## Contact
Do contact me via my email if you have any question.
