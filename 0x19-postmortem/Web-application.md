# Postmortem

![Developer meeting](developer-meeting.jpeg)


Date: [10-11-2023]

## Issue Summary:
On 8-11-2023, our web application experienced a critical incident that resulted in downtime. The incident occurred at 9:05 am GMT and lasted for about 2 hours. This postmortem aims to document the incident, identify its root causes, and propose preventive measures.

## Timeline:

+ 8-11-2023 9:05 AM GMT+1 - A user complained that they couldn't access the site, that it was displaying Error 404.
+ 8-11-2023 9:09 AM GMT+1 - one of our developers, tried to access the site experienced the same issues reported our users.
+ 8-11-2023 9:13 AM GMT+1 - Getting a 404 error has given us clue that it wasn't a server issue.
+ 8-11-2023 9:25 AM GMT+1 - We assumed the problem was from the route of the homepage.
+ 8-11-2023 9:50 AM GMT+1 - We checked that the views might not be binding the route file to the right model file, which later turned out to be false.
+ 8-11-2023 10:10 AM GMT+1 - One of our frontend developer thought the issue might have been that the page was mistakenly replaced or deleted.
+ 8-11-2023 10:20 AM GMT+1 - The incident was escalated to the front end team.
+ 8-11-2023 10:55 AM GMT+1 - The incident was resolved by rerouting the index page of the web application (Homepage).
 
 ### Root Cause And Resolution

 The index file was renamed as homepage, It was raising an error 404 Page not found, because it couldn't find the root file which is by default name as "index" and also the home page of the website. One of our frontend developer fixed the issue by dupicating and renaming the home page into index.html page and the site came up immediately.

### Corrective And Preventative Measures

+ Communication
Clear communication channels during incidents are crucial.
Regular updates should be provided to stakeholders.

+ Monitoring:
Enhance monitoring tools to detect issues early.
Implement automated alerts for critical system metrics.

+ Documentation:
Maintain up-to-date documentation on configurations and dependencies.
Document incident response procedures for quick reference.

+ Testing:
 Strengthen the testing process to identify potential issues before deployment.
+ Implement automated testing for critical paths.
