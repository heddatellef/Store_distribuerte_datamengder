# Store_distribuerte_datamengder

Assignment 2 - MySQL
Group: 22
Students: Simen Tvete Aabol, Hedda Sofie Tellefsen, and Marcus Klomsten Dragsten
Introduction
The tasks given are split into three, where Simen and Marcus mainly did task one, and Hedda did task two. The whole group worked together on writing the report in task three.
Task one addressed the insertion of data from the Geolife dataset into our MySQL database. The first problem we solved was which data we would want to pass into the database. After deliberating we landed on excluding data, we deemed invalid. Firstly, we only kept the data from users that labeled their activity that matched with the activities’ start- and end times. We did include, on the other hand, all the data from the users that had not labeled their activities. Another exclusion, that affected all the data, was the exclusion of activity-files that contained over 2500 lines of track points. More of this is in the results part of the report, but we managed to decrease the number of track points from 24 million to about 5,3 million.
Lastly, the method of inserting the data into the database was essential for completing task one. Our first implementation added the track points one by one using a for loop. This was very inefficient, so we changed the method to add the track points into a list of tuples, and then add multiple track points at a time. This was the only complication we phased in this task. Adding the users and activities was much simpler.
We used the client program “Beekeeper Studio” to connect to our database and use as a tool to write and test the queries before inserting them into our Python program. Using the setup from example.py we made the Python program QueryProgram.py to answer the questions in part 2. For most of the tasks, clean MySQL-queries were sufficient to get the result(s), but in some of them, we used python code to manipulate the data received from the queries. We used tabulate for all the tasks to present the results cleanly and clearly.
We did the programing together using GitHub, but the repository is private, as the passwords are not hashed. Therefore, all the relevant files are delivered in BlackBoard.
TDT4225
       1

 TDT4225
   Results Part 1:
The first 15 rows are from the User table. We can see that only user 010 has labeled its activities.
 The first 15 rows are from the Activity table. These activities are all from user 000, which has not labeled its activities.
   2

 Lastly, the first 15 rows are from the TrackPoint's table. All these track points are from the first activity.
TDT4225
        3

 TDT4225
   Lastly, we wanted to show how many track points we added to the database. As mentioned in the introduction, the count is now 5,355,358 track points.
 Part 2:
Task 1 results:
Task 2 results:
The average is rounded with one decimal.
    4

 Task 3 results:
TDT4225
     Task 4 results:
OverNightUsers ----------------
      000
      001
      002
      003
      004
   5

 005
006
007
011
013
014
015
016
017
018
019
020
021
022
024
025
026
027
028
029
030
032
035
036
037
038
039
041
042
043
044
050
051
057
058
061
062
070
071
074
083
TDT4225
      6

 TDT4225
         085
      094
      095
      099
      103
      113
      115
      126
      128
      132
      134
      140
      142
      146
      150
      155
      157
      163
      168
      172
Task 5 results:
The query retrieves duplicates in activities and returns no lines. This is considered good.
Task 6 results:
By only checking users: 003, 004, 006, and 007 (to save time) this is the result:
     7

 TDT4225
   We tried running the script for the whole dataset. The resulting array is a lot longer than shown in the screenshot. The total number of users matched was 1864, which means that there are 932 distinct matches in the dataset. (Distinct as in (000, 001) and (001, 000) is the same).
 Task 7 results:
NotTaxiUsers --------------
     000
     001
     002
     003
     004
     005
     006
     007
     008
     009
     011
     012
     013
     014
     015
     016
     017
     018
     019
     020
   8

 021
022
023
024
025
026
027
028
029
030
031
032
033
034
035
036
037
038
039
040
041
042
043
044
045
046
047
048
049
050
051
052
053
054
055
056
057
059
060
061
063
TDT4225
      9

 064
065
066
067
068
069
070
071
072
073
074
075
076
077
079
081
082
083
084
086
087
088
089
090
091
092
093
094
095
096
097
099
100
101
102
103
104
105
106
107
108
TDT4225
      10

 109
110
112
113
114
115
116
117
118
119
120
121
122
123
124
125
126
127
129
130
131
132
133
134
135
136
137
138
139
140
141
142
143
144
145
146
147
148
149
150
151
TDT4225
      11

      152
     153
     154
     155
     156
     157
     158
     159
     160
     161
     162
     164
     165
     166
     167
     168
     169
     170
     171
     172
     173
     174
     175
     176
     177
     178
     179
     180
     181
Task 8 results:
The results are ordered in descending order from the number of distinct users that have used the different transportation modes, because this seems more informative than doing it alphabetically
TDT4225
      12

 Task 9 results:
In the first part of query 9b, we have included both the most active the second most active user (measured by the number of activities).
Hence, the user with the most activities is the one with user_id: 062.
In the second part, we have included the reported hours (rounded with two decimals), for the users from the first part.
From this, we can conclude that user 062 has fewer recorded hours than the user with the second most activities.
TDT4225
         13

 Task 10 results:
The answer is rounded to the closest integer.
TDT4225
        14

 Task 11 results:
Task 12 results:
There are a lot of invalid activities, which is may imply that some activities are wrongly recorded.
user_id invalid_activities --------- --------------------
000 101 001 45 002 98 003 179 004 219 005 44 006 17 007 30
TDT4225
       15

 008 16 009 31 011 32 012 43 013 29 014 118 015 46 016 20 017 129 018 27 019 31 020 11 021 1 022 55 023 11 024 27 025 263 026 18 027 2 028 36 029 25 030 112 031 3 032 12 033 2 034 88 035 23 036 34 037 100 038 58 039 147 040 17 041 201 042 54 043 21 044 31 045 7 046 13 047 6 048 1 050 8
TDT4225
      16

 051 36
054 2
055 15
056 1
057 16
058 2
060 1
061 12
062 133
063 8
065 5
066 6
067 1
069 1
070 5
071 27
072 2
073 6
074 19
075 1
076 2
077 3
078 5
079 2
080 1
081 2
083 15
084 4
085 11
086 2
087 1
089 4
090 3
092 1
093 4
094 16
095 4
097 2 099 11 103 24 108 2
TDT4225
      17

 109 3 111 1 112 10 113 1 115 26 119 22 121 4 122 6 123 3 126 3 127 4 128 138 130 8 131 10 132 3 133 4 134 31 135 5 139 2 140 86 142 52 144 1 145 5 146 7 150 16 151 1 152 2 153 2 155 30 157 9 158 9 159 5 162 9 163 4 164 6 165 2 166 2 167 4 168 19 169 9 171 3
TDT4225
      18

 172 9
173 5
175 1
176 8
180 2
181 14
TDT4225
      19

 TDT4225
   Discussion
The first task was the most time-consuming, because of the requirement of deeply understanding the assignment and planning before coding the implementation. We learned a lot from this task though, ranging from implementing the most efficient method of inserting data, as well as cleaning the data before inserting. This turned out to be the most challenging part of the task. As for deviations from the assignment sheet, we decided to not use the column date_days, because we saw no use for it in the assignment. The rest of the structure of the database is the same as described in the assignment sheet. Furthermore, we made some assumptions about what data we decided to insert into the database. As explained in the introduction, we included all activities from users without labels (except the ones with more than 2500 lines of track points). We are happy with the results of decreasing the number of track points drastically. Also, as described in the introduction, the biggest pain point of this task was finding an efficient way of inserting data into the database.
For the second part of the task, we found a lot of the tips at the bottom of the assignment sheet very helpful. We thought we would use MySQL Variables, which was linked to as one of the tips, to solve task 11 and 12, but we decided to use LAG instead of variables, as this seemed to be a nice way of calculating distance in altitude or time between two consecutive points.
After running the python program several times, we had some struggles with query 11 as the following error suddenly occurred:
“ERROR: Failed to use database: 1114 (HY000): The table '/tmp/#sql93bad_235_4' is full mysql”
After doing some research we found this MySQL site describing some MySQL bugs that seemed relevant: https://bugs.mysql.com/bug.php?id=99100&fbclid=IwAR0O9mj7kQKbxQ46lcPRaIg TFiSMV3raNl03nnzde_Tneu8mxVbgdufvKjo
Here is a screenshot from this site:
     20

 TDT4225
    It seems like there is a bug which causes the error that we received in our program, that is corrected for the 8.0.27 version. But since we are using version 8.0.26, this bug is present, and probably the reason why we got the error.
Further down at the same site, we found a temporary solution to the problem. When entering the virtual machine and the MySQL server, one can write
set session internal_tmp_mem_storage_engine=Memory;
This makes you able to run the 11th query in the Python program with receiving results instead of the error.
    21

 Feedback
The group enjoyed completing this task. The tasks felt relevant and 'up-to-date'.
If the assignment is to be used for next year, it could be opened up for the students to have some freedom of choice on how to filter/clean the data set. Had the group had freedom of choice on this, we would probably have filtered out activities that stretched over two days.
We also wanted to explore the possibility of looking at latitude, longitude, and altitude to find out if these changed dramatically during an activity. You could then remove these, and get even more accurate data.
Another thing that is quite suspicious is that some users have identical activities. The first Trajectory file for users 057, 094, and 150 was completely identical.
TDT4225
      22
