# parsebars.js

# 1.0 Back4App Registration

In order to host your own version of Parsebars.js, you will most likely want to create an account at www.back4app.com. Given that Parsebars.js was originally developed with Parse, this means that Back4App is currently one of the few viable free hosting options out-of-box. Back4App is a Cloud BaaS (Back-End as a Service) solution that will host your database initially free of charge (that is, until your query requests reach a specified limit threshold per second). See https://www.back4app.com/pricing for additional pricing information at scale. I've found Back4App to be highly reliable so far, but if you are interested in hosting your own Parse Server elsewhere, there are tons of useful instructions and tutorials online. This article is a good place to start: https://medium.com/@timothy_whiting/setting-up-your-own-parse-server-568ee921333a

# 1.1 Application Configuration

Simply open **blog.js** and change the configuration values to our own Application Id and Javascript Key, provided to you by Back4App (https://dashboard.back4app.com/ > Core Settings). This is where we connect to Parse. The configuration code will looks like this. The Application Id is the first string and the Javascript Key is the second:

```javascript
    // Connect to Parse API
    Parse.initialize(
        'x0rtG9s535J8ExWWJUXi8WO19C5xHcfDDef68Epm',
        'qX2sBdcEztbNQ9l8D0EZKdq1Suuopdrww310ti5x');
    Parse.serverURL = 'https://parseapi.back4app.com
 ```

<a name="schema"/>
## 2.0 Database Schema

The complete database schema is documented below. Without configuring the following classes and attributes in your own Parse dashboard, downloading the source code probably won't be much help!

<a name="classes"/>
### 2.1 Classes

For each Class, I've excluded the auto-generated default Parse columns, i.e. objectId, createdAt, updatedAt, ACL, etc. due to redundancy. Also, I've provided examples of object data for demonstration purposes only. If you are relatively unfamiliar with software development or have little experience with NoSQL databases in particular, you should be aware that you only need to create the columns with their provided titles, and should not by any means include a sample object like I have below. Doing so could mess up your application; this data will be generated on its own when users start interacting with your application.

* User

<hr>

<a name="user"/>
#### 3.1.3 User

| username (String) | name (String) | bio (String) | websiteLink (String) | profilePicture (File) | phoneNumber (String)
|--------------------------|-----------------|-------------------|--------------|----------------------|---------------|----------------|-------------------------------------|-----------------|-----------------------|----------------------|-------------------|----------------|
| lumberg | Lumberg | Just make sure you go ahead and put that new cover letter on all your TPS reports next time, mmkay? | https://www.youtube.com/watch?v=kVmC0ktznNo | https://memecrunch.com/image/51621675afa96f32ef000013.jpg?w=400 | 1-800-SLAVE-LABOR |
