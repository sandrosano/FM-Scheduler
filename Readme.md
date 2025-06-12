Here is a Tiny Data Engine i wrote, which generates automatically Lists for each aspect of Folk Marathon Logistics organization: Band (listening vs dancing concert) Schedule, Volunteer Schedule and Workshop-Dance and Workshop-Music Schedules.
Theoretically, this could be useful for any Event management scheduling, where artists, teachers and volunteers have similar availability options.

Place a correctly named .csv table with all the users, their Scheduling-Days availabilies and their type of contribution ( WS / Concert / Volunteer ) , correctly formatted.
( i offer to change input format or interface a different input format, if you have a clear idea and interest about it, just write me)

Run this script with python.

Examine the resulted lists and maybe integrate or change some minor aspects. Voila.

The algorithm is based on the concept of availability-options, and sorts redundandly starting from the least available person ( so first deals with the most picky ones and the more flexible ones fill up the gaps)

The current column-format of the input .csv is the following:

"id","firstName","lastName","interest","interestDetail","teachWorkshop","workshopTitle","workshopDescription","workchosendays","workshopNeeds","playConcert","bandName","audienceType","playDuration","performanceDays","responsiblePerson","volunteerShift","jobType","availableDays","song1","song2","song3","song4","song5","song6","song7","song8","song9","song10"

Expected Content for each column:
- ID: THe unique user ID. Each Band has one primary contact, so in the output its ID is referenced.
- First, last name: intuitive
- interest: Yes / No: if user wants to declare a special interst.
- interestDetail: Free Text Input: The special interest, can be anything, can be analyzed with the same script like (see below) the most voted songs (not tested).
- teach WOrkshop: Yes / No
- Workshop Title: Free Text
- Workshop Description: Free Text
- workshop chosen Days: Can be any or a subset of: [Friday 29/12,Saturday 30/12,Sunday 31/12,Monday 01/01,Tuesday 02/01] and defines on which days of the Event the teacher gives availability to conduct the workshop
- WS needs: Free Text, Teacher tells Organizer if he needs something ( whiteboard, silent room, speaker, matress)
- "playConcert", Yes / No, Tells if user wants to perform
- "bandName", Free Text 
- "audienceType", Listening / Dancing , Tell if the concert is for dancing or more calm, to sit down and listen.
- "playDuration", Number, Minutes of performance (not implemented, i check manually if it works and tune the output accordinly)
- "performanceDays", Can be any or a subset of [Friday 29/12,Saturday 30/12,Sunday 31/12,Monday 01/01], and defines on which days the band is available to play the gig.
- "responsiblePerson", Free Text (name) (although should be ID), Band Leader or Reference
- "volunteerShift", Xes / No, tells if person wants to make a volunteer shift
- "jobType", can be any or a subset of [Whatever is needed!,Serve beers at the bar,Sell drink tickets / Entrance, Badge & Welcome,Prepare food,Pepare and clean the venue,I am from Palermo, I want to help visitors in city-related questions] and determines which kind of activity the given person wants to / is able / offers to perform. Note that "Whatever is needed" is evaluated at last, to fill up the gaps.
- "availableDays", can be any or a subset of [28/12,29/12,30/12,31/12,01/01,02/01] and determines, on which day a given person is available to do the volunteering shift.
- The SongX columns are for the second juptyer code cell, where the most voted songs to play are determined out of the user input in those fields. The users have 10 Free Text input fields, each for a distinct song they want to play.