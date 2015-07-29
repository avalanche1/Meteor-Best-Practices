# Meteor Best Practices
Hey, fellow Meteor developer!  
Welcome to this humble place of Meteor knowledge :blush:

This Guide is intended to help Meteor developers share their best practices for building most efficient and robust Meteor applications.
Information provided here comes from Meteor experts and is proven by positive usage experience in Meteor community.

##Application Design
- [ ] *Describe Component Design*  

##Data Management
- [ ] *Describe Indexes*  
- [ ] **Retrieving data from a 3rd party API or other non-Mongo source**  
By default, data in publications come from MongoDB, but you can also publish data from other sources by using a `Client-only collection` and `this.added` call of the publication.  
This solution also makes your data static (as there is no Server collection), i.e. there are no reactive change on the Client when data in datasource changes. This can help you save server overhead (for maintaining reactive connection to [hopefully:wink:] thousands of clients) if you publish to your page static data that shouldn't change during single user-session.
Read: [Publishing anything](http://meteorcapture.com/publishing-anything/) by [@dburles](https://github.com/dburles)

##Performance
- [ ] *Describe FastRender*  
- [ ] *Describe SubsManager*
- [ ] *Describe static data retrieval*  
*One way is to use this.added described in Retrieving data from a 3rd party API*
*The other - through meteor methods*
 
## Security
- [ ] *Add [Josh Owen's](http://joshowens.me/) Security Checklist if he grants permission.*
 
##Miscellaneous
- [ ] *Add ref to https://github.com/oortcloud/unofficial-meteor-faq*

