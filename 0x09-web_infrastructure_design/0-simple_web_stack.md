
1.  A server:

        This is a piece of computer hardware or software that provides 
        functionality for other programs or devices.
2.  What is the role of the domain name:

        The Domain name enables users to access Websites, without having
        to know the associated IP addresses of the websites.
3.  What type of DNS record www is in www.foobar.com:

        www is a CNAME(Canonical Name) DNS record-type in www.foobar.com since 
        it also points to the same IP address as foobar.comand if the IP address changes
        we can only record changes in the DNS A record of foobar.com.
4.  The role of the webserver

        The role of the webserver is to accept requests made by the browser through HTTP,
        process the requests by responding with HTML content.
5.  The role of the application server:

        The role of the application server is to act as a host (or container) for
        the user’s business logic while facilitating access to and performance of the
        business application.
6.  What is the server using to communicate with the computer of the user requesting the website:
        the server communicates through HTTP protocol
7.  The role of the database:

        A database is a software used for storing data in our application.
        The role of the database is to allow the management, creation, updating,
        and retrieval of records. The Database also gives structure to business information.

Issiues with this infrustraction:
1. SPOF;

Single Point Of Failure (SPOF), is a part of the system that,
if it fails the whole entire system stops from working.

The above infrastructure has no redundancy that can help in avoiding SPOFs,
 hence, any single failure in any part of the system will cause all the system to stop.

2. Downtime when maintenance needed (like deploying new code web server needs to be restarted);

The Infrastructure above, downtime will occur because we only have one server and
one database, that is used to make the deployment and maintenance
hence no way users will access the website in that period.

3. Cannot scale if too much incoming traffic;

The above infrastructure cannot scale if there’s too much incoming traffic because
no second server in the system to share loads and the system will be overloaded.
