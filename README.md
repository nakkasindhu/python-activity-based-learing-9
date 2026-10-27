# python-activity-based-learing-9
Algorithm
1.Start.
2.Store course schedules using tuples.
3.Check whether two courses have the same day and overlapping times.
4.Check room availability.
5.Display conflicts or a valid timetable.
6.Stop.
flowchart
Start
Enter course schedules
Check time and room conflicts
Conflict found?
Display result
Stop
courses = [
    ("Python", "Mon", 9, 10, "R1"),
    ("Maths", "Mon", 9, 11, "R1"),
    ("English", "Tue", 10, 11, "R2")
]

for i in range(len(courses)):
    for j in range(i + 1, len(courses)):
        a = courses[i]
        b = courses[j]

        if a[1] == b[1] and a[2] < b[3] and b[2] < a[3]:
            print(a[0], "and", b[0], "time conflict")

        if a[1] == b[1] and a[4] == b[4] and a[2] < b[3] and b[2] < a[3]:
            print("Room conflict:", a[4])
Python and Maths time conflict
Room conflict: R1
            
