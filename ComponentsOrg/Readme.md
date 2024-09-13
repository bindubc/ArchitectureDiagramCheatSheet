

### Client:
1. Identify the Actor/Client = > Browser, mobile app(ios/andriod), external and internal service

### Server Side:
 1. Identify the Frontend System and differentiate
 3. identify the backend system
    * stateless
    * statefull
 4. (Minimize the latency)identify DNS/GeoDNSComponent: We configure our DNS to direct all requests from our browser app to our frontend host and from our frontend host and two mobile apps to our backend host.
  5. Identify the Data store
      * Sql
      * no sql

        
![This is an alt text.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781633439108/files/OEBPS/Images/CH01_F01_Tan.png "This is a sample image.")
![image](https://github.com/user-attachments/assets/4735f360-d50d-456c-be1c-feab592b54f5)


### Notes:
 
 * Geodns : If our service serves users from a specific country or geographical region in general, we will typically host our service in a nearby data center to minimize latency. If your service serves a large geographically distributed userbase, we can host it on multiple data centers and use GeoDNS to return to a user the IP address of our service hosted in the closest data center. This is done by assigning multiple A records to our domain for various locations and a default IP address for other locations. (An A record is a DNS configuration that maps a domain to an IP address.)

When a client makes a request to the server, the GeoDNS obtains the client’s location from their IP address and assigns the client the corresponding host IP address. In the unlikely but possible event that the data center is inaccessible, GeoDNS can return an IP address of the service on another data center. This IP address can be cached at various levels, including the user’s Internet Service Provider (ISP), OS, and browser.
