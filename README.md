# SQL-Testing-Task
   --First Query--
select S.Std_Name,b.Book_Name,r.Rent_Date
from students S , books b,[renting history] r
where b.Book_ID=r.Book_ID and s.Student_ID=r.Student_ID 
/*******************/
      --second query---
select s.Std_Name,COUNT(r.book_id) as Count
from students s join [renting history] r on 
s.Student_ID=r.Student_ID 
group by s.Std_Name
Having COUNT(r.Student_ID)>1;
