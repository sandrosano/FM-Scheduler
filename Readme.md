Here is a Tiny Data Engine i wrote, which generates automatically Lists for each aspect of Folk Marathon Logistics organization: Band (listening vs dancing concert) Schedule, Volunteer Schedule and Workshop-Dance and Workshop-Music Schedules.
Theoretically, this could be useful for any Event management scheduling, where artists, teachers and volunteers have similar availability options.

Place a correctly named .csv table with all the users, their Scheduling-Days availabilies and their type of contribution ( WS / Concert / Volunteer ) , correctly formatted.
( i offer to change input format or interface a different input format, if you have a clear idea and interest about it, just write me)

Run this script with python.

Examine the resulted lists and maybe integrate or change some minor aspects. Voila.


The current column- format of the input .csv is the following:
"id","firstName","[SOME COLUMNS WITH ORGANIZATIONAL DATA]","interest","interestDetail","teachWorkshop","workshopTitle","workshopDescription","workchosendays","workshopNeeds","playConcert","bandName","audienceType","playDuration","performanceDays","responsiblePerson","volunteerShift","jobType","availableDays","song1","song2","song3","song4","song5","song6","song7","song8","song9","song10","accommodation"