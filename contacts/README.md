# Contacts

Contacts is intended as part of a re-design of Audience.


#### The problem with Audience

> There's an enormous opportunity for Emma to deliver the best **contact management** toolset in our market by making it indispensable to marketers' experience of the application.  
>  
> The current Audience section has not received any serious attention in over seven years. While its fundamental components (Contacts, Fields, Groups) are functional for most basic marketing needs, they are painfully dated, with slow load times, unintuitive interface, and buried features. The audience section does not currently reflect the value of a user's audience.  
>   
> Several levels of work will be required to bring this section up to date, ranging from **a substantial refactor of the Contacts database** to a redesign of the core interactions of the application. 
>  
> A redesign of the Audience application will enable us to support a dramatically expanded amount of audience data, ranging from location (based on IP address) to purchase history to event registration activity and more. Our access to this data will enable us to deliver a more powerful view of a marketer's email audience than any other email service provider currently offers. We'll be able to tell users who their contacts are, what they're interested in, when they're most likely to engage, where they're located, and why their email strategy matters.

See [Audience 2.0](https://myemma.atlassian.net/wiki/display/AUDIENCE/Audience+2.0).


#### Design objectives

* increase the size (deep and wide) of the single lists the Emma platform can import, manage, export, and merge for sending
* reduce cost of counting groups
* increase the performance and usability of segments
* separate read/write locations between contacts and response data
* create a 'drop-in' replacement of the contacts system so other services do not require changes

See esp. the discussion regarding [distributed storage options](https://myemma.atlassian.net/wiki/display/ARCH/Distributed+Storage+for+Contacts) for Contacts.


