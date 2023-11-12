Postmortem

Issue Summary
Close to the end of the years operations and when the Christmas celebrations were about to begin, on December 10–2019 at 12:00 am GMT-5, a series of issues where starting to be reported by users and thus a full on investigation of this bug was set finding it was affecting 100% of traffic to the container who reported a (52) Empty reply from server. The fix was expected by that same day before 11:00 pm GMT-5.
Timeline
12–10–2019, 12:00 am GMT-5, first reports of issues started to arrive.
12–10–2019, 1:00 am GMT-5, Team is alerted of the situation and is called to find a solution.
12–10–2019, 9:00 am GMT-5, Devops team arrives on campus and start working on the issue.
12–10–2019, 9:09 am GMT-5, the devops team was sad because we weren't going on vacation yet.
9–12–2018, 1:00 pm GMT-5, After some reading and coffee, issue was identified. Apache was installed but never started.
9–12–2018, 2:00 pm GMT-5, possible solutions are drafted.
9–12–2018, 4:00 pm GMT-5, solution is found and code is uploaded to server.
9–12–2018, 5:00 pm GMT-5, the situation is being monitored in case of further issues.
9–12–2018, 6:00 pm GMT-5, Service is fully restored, no further issues reported (Finally people can use all the power of a container to type" Hello Holberton").

Root Cause
One of the Devops team members was so excited about his vacations he installed Apache on the server but forgot to initilize it. User of the container where getting errors as they were not getting any answer from port 8080.
Resolution and recovery
After discovering the root cause, the following script was created to start the apache server:
To test that the Apache was up and running curl 0:8080 was run and this time instead of the "curl: (52) Empty reply from server" error, Hello Holberton was returned as it was supposed to.
Corrective and Preventative Measures
This is a silly mistake as the only reason found for such an error is it was a human error. Before setting up a container it has to be tested and see if it is working, a check list could be of use from now on. Another recommendation would be to avoid giving any type of vacations to the devops team, it generates too many costly distractions.
