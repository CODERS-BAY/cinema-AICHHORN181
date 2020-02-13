# Cinema
## Choose useful attributes and relations


The STAR-MOVIES company operates a cinema chain with several cinemas (Name,
Address... ). Each cinema can have several halls where the films are shown. The seating plan of each hall should be recorded; a row and a seat must be indicated for each seat. A box should be managed like a row.
It must be possible to create a seating plan. Of course, several films can be shown per room on one day. In order to be able to determine which seats are available for a performance, each ticket purchase must be noted. Each ticket should show: cinema, hall, film title, date, starting time, serial number within the screening, row, seat, price.
Provision must be made for pricing: Each row of a hall has a standard price, but for certain performances the row prices can be set individually. For information purposes, the actors should be recorded with their personal data (surname, first name, nationality, date of birth, date of death, comments, ... ) and it should be possible to tell which actors have acted in which films.
The analogous statements should also be possible for directors, whereby it can be assumed that there is only one director for a film. However, it is possible that the director also plays a part in a film.
The other data of a film include: Title, type (thriller, western, youth film, ... ), year of production, country, language, duration, distribution, etc.

Create a ERD and a Relation Model for this example

Cinema( **CNR: int**, name: varchar(30), address: varchar(30));</p>
halls( **CNR: int, HNR: int** );</p>
films( **FNR: int**, nam: varchar(30), *ftnr: int*, dnr: int );</p>
filmtype( **FTNR: int**, name: varchar(30));</p>

filmactor(***fnr:int,anr:int***) </p>
actors( **ANR: int**, name: varchar(30), ...);

director( **DNR: int**, name: varchar, ...);

seatingplan ( ***CNR: int, HNR: int, row: int, seatnr: int*** );

timetable( ***cnr:int, hnr:int***, **sernr: int**, fnr:int, date:date, startingtime: time)

timetableprice( ***cnr_int, hnr:int, sernr: int***, **row:int, seat:int**, price: double) </p>

tickets( ***cnr:int, hnr:int, sernr:int***, *row:int, seat:int*)

pricestandard( **cnr:int, hnr:int, row:int, seat:int**, price double;
