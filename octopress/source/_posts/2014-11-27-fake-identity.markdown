---
layout: post
title: "fake-identity"
date: 2014-11-27 17:31:17 +0530
comments: true
categories: util 
---

# [fake-identity](https://www.npmjs.org/package/fake-identity)

> Generate random identity objects including name, address, etc. This may be useful if you are trying to fill your application with random personal data.

__What else?__

- Generates a single random identity or multiple identities in an array.
- Includes first and last names, email address, phone number, street, city, state, zip code, date of birth, sex, company, and department.
- Email address is based off of name.
- First name matches sex.
- All names, streets, and cities are commonly found in the US.
- States are weighted on population, so more populous states appear more often.
- Zip codes are loosely based on state. Zip codes are weird so it's not perfect, though.
- Date of birth will be between 18 and 60.
- Usable in the browser or Node.js.
- No dependencies.

__Install it:__ `npm install fake-identity`

__Sample usage:__

```javascript
identity = require('fake-identity')
identity.generate();
/* 
Would result in a random object like:
{ sex: 'male',
  firstName: 'Jonathan',
  lastName: 'Murphy',
  emailAddress: 'jmurphy@example.com',
  phoneNumber: '(555) 555-2739',
  street: '4473 Highland Avenue',
  city: 'Glendale',
  state: 'KS',
  zipCode: '67069',
  dateOfBirth: Mon Jan 24 1955 00:00:00 GMT+0530 (IST),
  company: 'Woodgrove Bank',
  department: 'Engineering' }
*/

identity.generate(2); // Int val for the number of records.

/*[ { sex: 'male',
    firstName: 'Nathan',
    lastName: 'Morgan',
    emailAddress: 'nmorgan@example.com',
    phoneNumber: '(555) 555-5027',
    street: '2897 Meadow Lane',
    city: 'Ashland',
    state: 'CA',
    zipCode: '94347',
    dateOfBirth: Fri Jan 14 1966 00:00:00 GMT+0530 (IST),
    company: 'Northwind Traders',
    department: 'Product Management' },
  { sex: 'male',
    firstName: 'Jackson',
    lastName: 'Wilson',
    emailAddress: 'jwilson@example.com',
    phoneNumber: '(555) 555-7407',
    street: '514 Court Street',
    city: 'Shiloh',
    state: 'MO',
    zipCode: '64416',
    dateOfBirth: Sun Apr 02 1995 00:00:00 GMT+0530 (IST),
    company: 'Fourth Coffee',
    department: 'Information Systems' } ]
*/
```

__GIF FTW!__

![fake-identity](/images/fake-identity/fake-identity.gif)


This is pretty modular and sweet util, that needs some more configurability, thanks to [Travis Horn](http://travishorn.com/) for fake-identity.

