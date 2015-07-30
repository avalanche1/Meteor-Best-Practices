# Meteor Best Practices
Hey, fellow Meteor developer!  
Welcome to this humble place of Meteor knowledge :blush:

This Guide is intended to help Meteor developers share their best practices for building most efficient and robust Meteor applications.
Information provided here comes from Meteor experts and is proven by positive usage experience in the Meteor community.  
*Please note that some of the techniques may prove hard to grasp for Meteor beginners and moderate experience with Meteor is advised.*

*This Guide is in its infancy :baby: - PRs are very welcome*

##Application Design
- [ ] *Describe Component Design*  

##Data Management
- [ ] *Describe Indexes*  
- [x] **Retrieving data from a 3rd party API or other non-Mongo source**  
By default, data in publications come from MongoDB, but you can also publish data from other sources by using a `Client-only collection` and `this.added` call of the publication.  
This solution also makes your data static (as there is no Server collection present), i.e. there are no reactive changes on the Client when data change in the datasource. ~~This can help you save server overhead; see: *Performance - Using Static Data*~~  
Read: [Publishing anything](http://meteorcapture.com/publishing-anything/) by [@dburles](https://github.com/dburles)

##Performance
- [ ] *Describe FastRender*  
- [ ] *Describe SubsManager*
- [ ] *Describe Using Static Data*  
*This can help you save server overhead (for maintaining reactive connection to [hopefully:wink:] thousands of clients) if you publish to your page static data that shouldn't change during single user-session.*  
~~*One way is to use this.added described in Retrieving data from a 3rd party API*~~  
*The other - through meteor methods*
*The other - through FastRender injection*
 
## Security
- [ ] *Add [Josh Owen's](http://joshowens.me/) Security Checklist if he grants permission.*

## Scaling
- [ ] *Describe capacity scaling*
- [ ] *Describe geographical scaling*
 
##Miscellaneous
- [ ] *Add ref to https://github.com/oortcloud/unofficial-meteor-faq*

##Hacks 
:warning: *naturally* ***not*** *best practices, but may prove useful*:wink:
- [ ] *Describe Meteor._sleepForMs(time)*  
- [ ] *Describe Blaze._globalHelpers['helper']()*  
- [ ] *Describe T.__helpers.get('helper').call()*  
- [ ] *Describe Meteor.defer()*
*Since those features are undocumented, their syntax may be modified or dropped altogether in the next update without any notice.* ***Use at your own discretion***
