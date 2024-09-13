
List of Use case to think though in term of scalability by systemComponent:


### SystemLevel Component 
  Actor : user, app, request 
    1. may only have a small number of users and thus a low request rate -->  A single host may be sufficient to handle the low request rate. 

### High Peak Impact:
 * backend service receives thousands/more of requests per second than expected->
     * status code 504 responses due to timeouts ==> We must scale up our system.
     * one of component could crash
     * database could overloaded due execution of higher query by backend service
     * Hotspot in lower/dependent service or 3rd service


   workaround :
     * if  Our service is stateless as per standard best practices,so we can provision multiple identical backend hosts and place each host in a different data center in a different part of the world.
     * GeoDNS to direct the client to the data center closest to it.
    
