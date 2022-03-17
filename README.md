# Database-Application
This is a repo with database application developed using SQL. It is group project of one of course at my Bachelor's study
BUSINESS PROBLEM FOR DATABASE APPLICATION
The database application is designed for a medical company. The company
takes ingredients from suppliers and uses those ingredients to manufacture
products and these products are supplied to various branches. Each branch
has its own employees. The database design is quite complex. Because the
company doesn’t simply buy the products, but it manufactures them instead,
this complicates things as then there have to be some ingredients which the
company possesses to manufacture products. To add to it the ingredients
have to be supplied by some supplier. Furthermore, we also assume that a
company has more than one branch, so this adds to the complexity of the
database as then the supplier has to supply to each branch and moreover,
each branch has different employees.
Thus, the database created has 7 entities and 6 relations to store an
integrated and complete system. From this database, you can retrieve the
product, employee, supplier information. Also, users could trace the product
that could cure a certain disease.
We have set two view models for the users of this database. Both views are
implemented with a GUI, which could help users better use this system. One
is designed for common users, which provides users the right to check
product name and what disease the product could cure. And it will record the
user orders into our database for retrieval in later time. Another one is
designed for managers in this company, which has a branch manager view.
In this model users could retrieve internal information of the company, such
as the ingredient of a product and its supplier, also could retrieve which
branch company these suppliers supply for. The main goals of our database is
efficiency, safety and stability. Make the company who uses our database
won't miss any useful information.

Employees
The database consists of a total of 7 entities and 6 relations to store an
integrated and complete system. The medicine company buys ingredients
from suppliers to make products and sell them to customers at all branches.
The company has employees, and each employee has his/her details. The
“Employee” table stores all information about employees. Each employee has
a unique ID which is set as the primary key, defined as “E_ID”. Since this is a
centrally stored database, we have to make sure that each branch has
data.”work_for_relationship" is used to relate employees to their specific
branches and vice versa. Since employees work on manufacturing products,
there are special employees who do research on products, and they are
defined as “Researchers”. The relationship “Research_relationship” is used to
retrieve and know about such researchers. This relation relates them to the
products on which they are doing research.
6
Products
Products are an integral part of this database design. Products are
manufactured using ingredients. The product information is stored in the
table named “Product”. Product name “P_name” is defined as the primary
key because the name of every product is unique. The “Uses_relationship” is
used to retrieve ingredients used in manufacturing a specific product or vice
versa. Furthermore, “Cure” relationship specifies the disease(s) a product can
cure. Product table has a relation with “buy” as well, which specifies products
to be bought by customers.
Suppliers
Supplier supplies ingredients which are to be used in manufacturing
products. The entity defined as “Supplier” is used to store all supplier related
information. Each supplier has a unique ID which is defined as “S_ID”. This is
also the primary key for this entity. Each supplier supplies to one or multiple
branches and every supplier may supply one or more than one ingredient.
The relation “Supplies_relatioship” is used to store the above information,
where “B_ID” is the ID of the branch to which ingredient is supplied and
“I_Name” is the name of ingredient supplied
Customers
Customer entity is one of the fundamentals in any sales business’s database
design. In our database the table “Customer” stores all customer related data.
Every customer has a unique phone number hence the attribute
“phone_number” is set as the primary key. Customers make purchases of
product(s), the relationship “buy” specifies the product(s) name(s), quantity,
ID of transaction named “T_ID” and other transaction related details.
Others
Other smaller entities include “Ingredient” and “Disease”. Disease name is
specified as “D_Name” which is used to retrieve the products which can cure
this disease as shown in “Cure” relation. Ingredient(s) are supplied by a
supplier and are used in manufacturing product(s), specified in
“Uses_realtionship” and “Supplies_relationship” respectively.
7
IMPLEMENTATION AND TESTING OF DATABASE APPLICATION
Database was successfully deployed into oracle accounts of each of the group
members (refer to appendix). Toy data is used to perform simple queries and
to enable client side operations. The deployment of the database is done
using SQL, while two client side applications are implemented using JAVA.
There are two client-side applications developed. One is for more common
users (i-e customers) and the other for slightly more privileged users. The
basic/common user interface allows only simple retrieval of information such
as transaction details or information about products
Interface for a common user/ customer 
➔ When a user runs the application, the welcome screen appears where users can see the privileges they have.
➔ Search by Disease: This button allows users to look up for products that
cure a specific disease. On click on any
disease, names product(s) which are cure of that disease appear
➔ View Orders: This function is to allow customers to view their orders.
 It takes a phone number as input.
Exception is displayed if there are no orders of that customer or wrong
Phone number is entered. In case when the correct phone number is
entered, the products and quantity of them ordered by that customer
are displayed.
➔ Search by Product: This interface allows users to look up for product
details to add it to order. A window listing names of products appears,
on clicking the button, and by selecting a product, a new interface
appears as shown in listing the details of that particular product.
By selecting the proceed button, the user is taken to a new window,
which asks for user details and amount of product to be ordered.
➔ General features: After selecting any of the above options, the user can
go back to the home window by using the “Back” button. In general, to
confirm the order or user wants to end any query, there is a confirm
button at the bottom.
8
Interface for branch managers 
➔ Branch managers log into the application using their names and the
corresponding branch ID. This limits access to other users in the
database.
➔ After successful login, the manager chooses to view employees or
suppliers which are related to the branch that they manage.
➔ In the view employee page, the managers are able to view details of
any selected employee with the “profile” button.  They may
remove any employee or add a new one to their branch.
➔ Information about suppliers and the supply records can be retrieved
from the view supplier page.

