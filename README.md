# Course project mkulczewski-cvega
Please excuse us, we had a problem with the upload of the proyect to github due to the master branch being up to date with the changes,
this was beacause an error we had with the first commit of the proyect that results in a extrange folder that is uploades in the master branch (the proyect 1.2). We had to resort to upluad the proyect in a zip folder (the last file) that contais everything.


For the queries that we write we put a default id for each one of the queries to make them work, those can be found in the "find()" method or in the "where" section.
For the database we create a mini base in the seeds file to run the queries. Our assumptions with the model are these ones:
 - The admin of the organization will be the creator
 - When an invitation is recived the user must choose an option immediately and this is the vote

Questions 13, 14, 15

13) If an event in our model there would be a cascade that will delete all the invitations and the votes of the users or at least delete the foreing keys (depends on the dependent). From our point of view this default feature (cascade) makes sense beacause if the event is deleted the invitations will no longer be usefull as well as the votes. To improve this feature, there could be a trigger the notifies you if the event was deleted, but that is an idea for the future.

14) If an organization is deleted as well as the previous answer the default cascade feature will take action and all the connections like organization members and organization events will be deleted, but the event itself will not. This doesnt make sense, beacause in real life if an organization is disolved all the events will be canceled. So to improve our model there should be dependents to the event so when a organization is deleted all the events realted to that organization will be deleted aswell.  

15) In our model if a user is deleted the events and the organizations will not be deleted, but the comments will lose the foreing key of the user leaving them as comments without autor. This makes sense only refearing to the organizations and the comments, at least for us the comment shoudl stay but not its creator, but for the event is wrong it shoul be deleted as well as the user, this cuold be fixed if we aplied a dependent on the event table to be deleted with the user.
