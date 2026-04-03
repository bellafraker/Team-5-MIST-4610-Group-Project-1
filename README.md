# Team 5 MIST 4610 Group Project 1
## Team Name
61608 Group 5


## Team Members
1. Bella Fraker @https://github.com/bellafraker
2. Tim Adewoye @https://github.com/timiadewoye
3. Yachana Shah @https://github.com/tree-tee-tea
4. Lauren Cushings @https://github.com/laurencushing 
5. Brandon Sevel @https://github.com/BrandonSevel
6. Benjamin Saunders @https://github.com/BensOnPluto

## Problem Description
The task is to model and build a relational database for Athens Pulse Fitness operations, focusing on coordinating members, trainers, classes, and studio rooms. The database manages memberships, trainer assignments, class scheduling, and attendance while maintaining clear relationships between all entities. It enforces key business rules, including room capacity limits and membership tier restrictions, such as limiting Basic members to four classes a month while Unlimited members have unrestricted access. Attendance tracking must also ensure members are marked as “No-Show” if they fail to check in at least five minutes before class begins. The finished system supports meaningful business insights, member attendance trends, and facility usage efficiency.
## Data Model
Our model represents a fitness studio management system. The Members entity is our core entity and represents each individual who uses the studio. It includes information such as their name and contact information. Members and Memberships have a many-to-many relationship. To resolve this, we created the membershipLogs table as an associative entity to track these connections.

Another major part of the model is the relationship between Members and Trainers. Because of the many-to-many relationship between them, we created the associative entity trainingLogs. This table allows the studio to keep track of personal training sessions and the connections between clients and staff.

The model also includes a Classes entity, which represents the different classes offered by the fitness studio, such as yoga, cycling, or strength training. Because classes occur multiple times and can have many attending members, we used the classLogs entity as a central associative table to connect Classes, Members, Trainers, and studioRooms. This allows the system to record each class instance, who attended it, who taught it, and where it took place. Each of these entities has a one-to-many relationship with classLogs, as one class, member, trainer, or room can appear in many class instances.

Lastly, the model includes the studioRooms and Equipment entities to represent the physical resources of the studio. A studio room may contain many pieces of equipment, and the same type of equipment may appear in multiple rooms, so we created the equipmentInventory table as the associative entity between them.

Overall, this model captures both the customer-facing side of the fitness studio, such as memberships and classes, and the operational side, such as trainers, rooms, and equipment.
<img width="620" height="459" alt="Screenshot 2026-04-01 at 4 38 13 PM" src="https://github.com/user-attachments/assets/f5711b9b-ab73-486f-b52b-610f7167bedd" />
## Data Dictionary
<img width="662" height="293" alt="Screenshot 2026-04-01 at 8 30 37 PM" src="https://github.com/user-attachments/assets/35ea8bf7-5fd2-43b4-9fe2-7e63e0a86345" />

<img width="684" height="238" alt="Screenshot 2026-04-01 at 8 31 16 PM" src="https://github.com/user-attachments/assets/1a1e388d-a6b2-4f47-9da4-04c54c68ada6" />

<img width="669" height="456" alt="Screenshot 2026-04-01 at 8 32 47 PM" src="https://github.com/user-attachments/assets/d98a9e95-f57c-42da-80f7-10cfb7b0c5f3" />

<img width="661" height="194" alt="Screenshot 2026-04-01 at 8 34 08 PM" src="https://github.com/user-attachments/assets/b030c66d-b48c-4a0d-96d6-b54352511b35" />

<img width="653" height="305" alt="Screenshot 2026-04-01 at 8 52 13 PM" src="https://github.com/user-attachments/assets/9079c607-818d-4388-8127-eb12002a3aef" />

<img width="693" height="389" alt="Screenshot 2026-04-01 at 8 53 34 PM" src="https://github.com/user-attachments/assets/086fcc63-d0cf-479f-b39b-5b6d3f9bfc41" />

<img width="696" height="215" alt="Screenshot 2026-04-01 at 8 52 42 PM" src="https://github.com/user-attachments/assets/1d0a6f5e-83d8-43d5-86a8-4bcbcf75b788" />

<img width="705" height="299" alt="Screenshot 2026-04-01 at 9 10 12 PM" src="https://github.com/user-attachments/assets/2e2be027-78fb-458a-8e91-64e6decd4dc3" />

<img width="708" height="336" alt="Screenshot 2026-04-01 at 9 10 25 PM" src="https://github.com/user-attachments/assets/c30e5ca6-6307-45b6-b35f-2a4bcc2dacc7" />

<img width="713" height="276" alt="Screenshot 2026-04-01 at 9 10 44 PM" src="https://github.com/user-attachments/assets/7ad1a074-f380-4a5e-bf12-ffec97036dcb" />


## Queries

1. This query identifies the boutique gym’s highest‑demand classes by measuring total attendance across all logged sessions.
<img width="1250" height="692" alt="Screenshot 2026-04-03 at 6 37 59 PM" src="https://github.com/user-attachments/assets/c556c484-66d5-46ed-b8c3-e975ec4db740" />
By aggregating participation counts for each class and seeing them from most to least attended, the gym can quickly see which offerings attract the most members. These insights support strategic decisions such as reallocating studio space, adjusting instructor schedules, increasing class frequency, or investing more resources into the formats that consistently drive engagement.

## Database Information
Database Name: ns_Sp26_61608_Group 5

Additional Information: Each query listed above is marked in the database using stored procedures which can be called using the following format:???????
