java c
DAT 560G: Database Design and SQL
Spring 2025, Mini A
Assignment #3: SQL Part 2
Instructions
1. This is an individual assignment. You may not discuss your approach to solving these questions with anyone, other than the instructor or TA.
2. Please include only your Student ID on the submission.
3. The only allowed material is:
            a. Class notes
            b. Content posted on Canvas
            c. Textbook
4. You are not permitted to use other online resources
5. Questions 1 – 6 are auto-graded on Canvas due by 6 am the day of the next lab
6. The other questions are due on Canvas, by the next lab
7. There will be TA office hours. See the schedule on Canvas.
Background
Renting an apartment with roommates is guaranteed to be a new experience. You’ll make memories with your roommates, learn about their culture and hobbies, and learn how you cope with others in different times.
The database here is focused on renting out apartments to people with roommates. The people renting the apartments are one part of the database, but not the important part of it. We are mostly interested in the apartment buildings, and the owners of apartment buildings.
An apartment building has information about the date built and the year built. We also maintain information on address, city, and number of apartments in the building. Each apartment may be rented to one, or more, people. Other information we have is the total monthly rent for all tenants and the value of the apartment building, if it were sold. A property manager runs the individual apartment buildings. We also have the gender of the property manager.
Buildings (Building, DateBuilt, YearBuilt, Address, City, Apartments, TotalRent, Value, PropertyManager, Gender)
The apartment building is owned by a single company, or be several companies. Each company may own one, or more, apartment buildings. They may also only partial ownership of an apartment building. In that case, they would be partners with other companies. The Property attribute in the Ownership relation is identical to the Building attribute in the Buildings relation. (It’s a foreign key.)
For each owner we maintain information about what percent of the building that company owns. To give an example, if a building is owned by 3 companies, each with a different share, the ownership fraction for each company could be 33%, or one company may own a larger share. In another case, only 1 company owns the building. In this case, their ownership share would be 100%.
Information about the owners includes the city they are in, the number of partners, date the company was founded, and the number of times the partners meet each year. We also have information about the total assets owned by this company (in $M). The company has a manager. The manager’s gender is also kept.
Owners (Company, City, Partners, Meetings, DateFounded, Assets, Manager, Gender)
For each owner, in each building, we also know the date they purchased their share of the building. (To clarify, each company may have bought their share at a different time.) We also know what percent of their ownership stake has a mortgage on it. In the same building it could be that one owner has a mortgage of 80%, while another does not have a mortgage.
Ownership (Property, Company, Percent, PurchaseDate, PurchaseYear, Mortgage)
Tenant information in the database includes information about the people renting apartments. Each apartment may have one, or more, tenants. Frequently, roommates rent an apartment together. In addition to the tenants name, gender, and age, we have information about the apartment. This information includes the building name, the apartment number within the building, and the size of the apartment.代 写DAT 560G: Database Design and SQL Spring 2025 Assignment #3: SQL Part 2
代做程序编程语言 Information about the lease includes the date this person started to rent the apartment, their monthly rent, and the duration of the lease in months.
Since many of the apartments have sublets, renters in the same apartment may have started their lease at different dates.
Tenants (Building, Tenant, Gender, Age, Apartment, Size, Rent, LeaseStart, Duration)
Database
The E/R Diagram for the database is below.

Relations:
Buildings (Building, DateBuilt, YearBuilt, Address, City, Apartments, TotalRent, Value, PropertyManager, Gender)
Owners (Company, City, Partners, Meetings, DateFounded, Assets, Manager, Gender)
Ownership (Property, Company, Percent, PurchaseDate, PurchaseYear, Mortgage)
Tenants (Building, Tenant, Gender, Age, Apartment, Size, Rent, LeaseStart, Duration)
Each of these questions is 10 points. Submit answers to these online on Canvas, by 11.59 pm the day before the lab. They are automatically graded.
1) Select companies that purchased new properties in the year 2010. Let's consider a building new if it is built in the same year that purchased. List properties, and companies in your results. Sort results in increasing the order of property names.
2) Find the buildings with more than 5 tenants. List the name of the building, number of tenants, and average age of tenants.
3) In total, how many buildings were built in St. Louis? What were their total number of tenants, the average duration of the lease, and the average size rented?
4) List the companies that have at least 3 different buildings in the city of St. Louis.
5) For each company with assets more than 3 find all properties that they owned 100%. Include information about the company name, assets, mortgage, city of the property, and the value of the property. Sort result in increasing order of company name and increase in property value. Do not report rows with null values.
6) List companies that own at least 20% of the buildings they have ownership in with a mortgage (do not consider 0 mortgages).
Each of these questions is worth 5 points. Submit answers to these on Canvas before the due. They will be graded by TAs.
For each question, submit your SQL code and a screenshot of the results. If the results are too long, partial results are fine. Include relevant attributes for each result, to explain that the result is correct. Do NOT include many unnecessary attributes. Do NOT use SELECT *.
7) List pairs of tenants who live in the same building and have the same age. List the tenants and the building name. Order by the building.
8) Find the number of tenants per building where the gender of the tenant is the same as the property manager’s gender. List the building, and number of tenants (with the same age as the manager). Order by the building.
9) List the building name, address, city, Manager of the owner, and mortgage of the building by the owner. Exclude the rows where the mortgage is null. Order by the mortgage.
10) Find companies that have managers and property owners of a different gender. Do not report buildings with less than 6 apartments. List company name, manager name, manager gender, property manager’s name, property manager’s gender, and property’s name. Sort the result by company.
11) List the average size and average rent cost of the cities. List cities with at least 5 different buildings. Do not report null cities. Sort the results by average rent cost in decreasing order
12) List buildings with at least 5 tenants. Name the building, city, and number of apartments.
13) Find the average duration stays of tenants per building and apartment size. Exclude Null sizes.
14) How much time did you spend on this assignment?







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
