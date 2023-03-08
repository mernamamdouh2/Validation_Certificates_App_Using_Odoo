# Validation_Certificates_App_Using_Odoo
Validation_Certificates_App_Using_Odoo

A Client needs to implement Odoo as a system for his company that is working in the field of vehicles validation certificates.
The client company is licensed by the Ministry of interior to check vehicles and issue validation certificates to them.

The system should be able to record and print the validity certificates with the following screens:

![3](https://user-images.githubusercontent.com/74082044/223754737-1b86a091-cfda-4c1e-a796-d619098dbaa6.png)
![2](https://user-images.githubusercontent.com/74082044/223754761-d4c5a8a1-c80b-45b5-b553-2856e27cfb5f.png)

Notes for certificates form view:
1 – Vehicle types are predefined list of (Car, Bus, Minibus, Microbus)
2 – Certificate type should be a dropdown list that contains all certificate types that our client has a license to issue, keeping in mind that these certificate types should be extendable by the client if he/she was able to get any new license in the future.
Examples of certificate types: Motor Change, Chassis Fix, … etc
3 – Traffic departments should be a dropdown list with all departments that our client has a license to deal with, keeping in mind that these departments should be extendable by the client if any new department added in the future.
Examples of traffic departments: 6th October, Nasrcity, Aboud … etc
4 – The customer field should be related with “res.partner” model of odoo.
5 – Car model field should be a dynamic list that is generated automatically and lists all years between current year and 20 years before.
For example, if we are in 2024, then the list should contain all years between 2004 and 2024
6 – Brand field should be a dropdown list that contains vehicle brands added by the client.
Examples of brands: Mercedes, BMW, Toyota, … etc.
7 – Each certificate should have an automatic serial number that is using odoo sequences and has the following format: TD00001, TD00002, ...etc.

8 – The print button should be able to generate the pdf report of the certificate like the following template:
![1](https://user-images.githubusercontent.com/74082044/223754649-4d1d0127-5e9e-4bb0-ba24-902fdf40e256.png)


Notes about user types:
1 – There are two types of users:
  A. Normal Users
  B. Supervisors
2 – Each normal user can create and read only the certificates he/she has issued.
3 – Supervisors can create/read/update/delete any certificate.
4 – For security reasons we need to restrict each normal user to be able to print the issued certificate only once and we need to keep track with 
the timing he/she has printed the certificate
5 – The Supervisors will be able to allow reprinting for any certificate by clicking a button called “Allow Reprint” in the certificate form view.
Once the supervisor clicked this button on any certificate, the normal user should be able to print it again.
6 – Normal users should have read-only access on all certificate types, customers, traffic departments and vehicle brands
7 – Supervisors should have read/create/update/delete access on all certificate types, customers, traffic departments and vehicle brands
