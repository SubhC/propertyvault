# Project Name: Property Vault (propV)
Descriptions: This application provides a maaintainable safekeeping machanism to manage application related properties. Mostly                 all applications today keeps the properties/config files to externalize the links, startup parameter, general                   cofiguration information & resources. Now, any change to these cause halt/recycle of the the environment like                   webserver restarts. Moreove keeping sensative information on the flat files also exposes threats. Plenty of                     casses it is need that for avoiding security complications developers kept password information on these types                  of properties files, And that goes without saying "a major risk".
          
               This application is an attempt to
               1> To make the property or external information management easy and more governed as life cycle
               2> To hide sensative information
               3> To avoid JVM/web server recycle for making any property change
               4> To avoid hard copy flat file drop to manage properties
               5> To provide a mechanism to run as
                  a) Server Only Mode
                     Where the consumer pulls the information from active PropV server always and does keep any local cache.
                     Any changes to any property/ies and corresponding puss and pull is managed by the PropV server. In case the                      PropV server is down the Consumer may fail to get the properties and hence fail to load. 
                     
                  b) Cache Mode
                     Where the consumer pulls the information from active PropV server and keeps in a local cache.
                     Any changes to any property/ies and corresponding puss and pull is managed by the PropV server and updates                      the local cache. In case the PropV server is down the Consumer may load properties from the ;lastly updated                      cache. This cache is encrypted.
