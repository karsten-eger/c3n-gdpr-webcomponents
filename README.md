# c3n-gdpr-webcomponents
(partly) web component based wrapper in polymer3 regarding the General Data Protection Regulation (GDPR)

## Update
Due to some time constraints I had to create a short term solution without web components :( For anyone interested, it can be seen here: https://cdn.c3-net.de/js/gdpr.js
It uses https://github.com/js-cookie/js-cookie for easy cookie handling.

The basic functionality is identical to the web component idea I'd like to make, though.

### How it works? What does it do?
A lot of elements are able to load external content - images, iframes,... - and those are blocked until the user accepts it (for the one element or all elements of this type).

When the user accepts it for all elements of this type, the cookie - which contains a json object - is updated to remember this decision.

### How to use it?
- Just change all elements with a ```src``` attribute to ```data-src``` instead and add a ```data-gdpr``` attribute with a unique identifier for the content type - i.e. ```data-gdpr="youtube"```
- Modify the text to be shown as you desire
- (optional) Modify the name of the cookie
