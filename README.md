# E-hub
Abstract:
E-hub is a software company that provides various types of software solutions to clients across India. It has recruited various programmers
for software development. Each programmer is identified by the id, date of joining, experience, qualification, specialization,
programming_languages_known. Specialization signifies the programming language for which he is most specialized in. The company
may develop more than one software for one client. Each client is identified by his id, name, address, phone numbers. The details of
software developed for the client such as date_of_commencement, date_of_release, status_of_software, etc. are also maintained. Each
software may be developed by more than one programmer with one project leader. The software's working by a programmer will have
schedule_id, start_date, end_date.
<h1>Er Diagram:<h1> 
  
![alttext](https://github.com/tanguduraviteja/E-hub/blob/main/Erdiagram.png)
 
<h1> schema diagram: <h1>
 
![alttext](https://github.com/tanguduraviteja/E-hub/blob/main/Schema%20diagram.png)

<h2> Relational Schema : <h2>
<p> We have 6 entities namely - Client,Programmer,Software,Project leader,Schedule,Specialization
Composite attributes – name,address(client entity)
Multivalued attributes -phone_numbers,languages_known(programmer entity),phone_numbers(client entity)
Derived attributes – duration(schedule entity)
The strong entity set reduces to schema with the same attributes. The composite attributes get simplified by
creating separate attributes.
Programmer(programmer_id,name,phone_numbers,qualification,date_of_joining)
Languages_known(programmer_id,language)
Programmer_phoneno(programmer_id,phone_no)
Client(client_id,fname,lname,street,city,state)
Client_phonenumbers(client_id,phonenumber)
Software(software_id,date_of_starting,date_of_release,status_of_software,client_id)
Project_leader(projectleader_id,name)
Manages(projectleader_id,software_id,schedule_id,programmer_id)
Works_on(software_id,programmer_id,schedule_id)
Schedule(schedule_id,start_date,end_date)
Specialization(programmer_id,language) <p>
