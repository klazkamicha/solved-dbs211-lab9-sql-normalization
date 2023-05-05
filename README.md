Download Link: https://assignmentchef.com/product/solved-dbs211-lab9-sql-normalization
<br>
<strong>Objective:</strong>

<ul>

 <li>Students create the <strong>Un-normalized Form</strong> (UNF) relation from a user view.</li>

 <li>Students identify a <strong>Multi-valued Dependency </strong>(a.k.a. Repeating Group )</li>

 <li>Students create the <strong>First Normal Form</strong> (1NF) relation from the UNF.</li>

</ul>

<strong>Definitions:</strong>

<u>Definition</u>: <strong>Normalization</strong> is the process of assigning attributes to relations in such a way that data redundancies are reduced or eliminated.

<u>Definition</u><strong>: User Views</strong> can be individual descriptions, reports, forms, or lists of data that are required to support the operations of a particular database user.

<u>Definition</u>:<strong>  Unnormalized form (UNF) </strong>is a relation that contains one or more <strong>Multi-valued Dependencies</strong><em>. </em>

<strong><u> </u></strong>

<u>Definition</u>:<strong>  </strong>A <strong>Multi-valued Dependency </strong>is an attribute or collection of attributes within a relation that has multiple values for a single value of the primary key for that relation.

<u>Definition</u>:  A relation is in<strong> 1NF </strong>if it does not contain any multi-valued dependencies.

<strong>Instructions:</strong>

Step 1:  Create UNF Relation from a User View. The goal here is to create a single relation for the data found in the user view. The method used is:

<ul>

 <li><strong>Examine the user view</strong></li>

 <li><strong>Identify all attributes</strong></li>

 <li><strong>Describe the user view using DBDL</strong></li>

</ul>

Here is an example of a user view. This reports lists the customers of the Premiere Corporation.

<strong>Premiere Corporation Customer List</strong>

<table width="678">

 <tbody>

  <tr>

   <td width="63"><strong>CustNo</strong></td>

   <td width="107"><strong>Name</strong></td>

   <td width="144"><strong>Street</strong></td>

   <td width="72"><strong>City</strong></td>

   <td width="95"><strong>State</strong></td>

   <td width="85"><strong>ZipCode</strong></td>

   <td width="112"><strong>SalesRepNo</strong></td>

  </tr>

  <tr>

   <td width="63">124</td>

   <td width="107">Sally Adams</td>

   <td width="144">482 Oak</td>

   <td width="72">Lansing</td>

   <td width="95">MI</td>

   <td width="85">49224</td>

   <td width="112">03</td>

  </tr>

  <tr>

   <td width="63">256</td>

   <td width="107">Ann Samuels</td>

   <td width="144">215 Pete</td>

   <td width="72">Grant</td>

   <td width="95">MI</td>

   <td width="85">49219</td>

   <td width="112">06</td>

  </tr>

  <tr>

   <td width="63">311</td>

   <td width="107">Don Charles</td>

   <td width="144">48 College</td>

   <td width="72">Ira</td>

   <td width="95">MI</td>

   <td width="85">49034</td>

   <td width="112">12</td>

  </tr>

  <tr>

   <td width="63">315</td>

   <td width="107">Tom Daniels</td>

   <td width="144">914 Cherry</td>

   <td width="72">Kent</td>

   <td width="95">MI</td>

   <td width="85">48391</td>

   <td width="112">06</td>

  </tr>

  <tr>

   <td width="63">405</td>

   <td width="107">Al Williams</td>

   <td width="144">519 Watson</td>

   <td width="72">Grant</td>

   <td width="95">MI</td>

   <td width="85">49219</td>

   <td width="112">12</td>

  </tr>

  <tr>

   <td width="63">412</td>

   <td width="107">Sally Adams</td>

   <td width="144">16 Elm</td>

   <td width="72">Lansin</td>

   <td width="95">MI</td>

   <td width="85">49224</td>

   <td width="112">03</td>

  </tr>

  <tr>

   <td width="63">522</td>

   <td width="107">Mary Nelson</td>

   <td width="144">108 Pine</td>

   <td width="72">Ada</td>

   <td width="95">MI</td>

   <td width="85">49441</td>

   <td width="112">12</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<ol start="124">

 <li><strong>Examine the user view: </strong>As you examine this report, you can see that it contains a title, a line of column headings and the body of the report. Each line in the body of the report contains data about a particular customer. For example we can see that in the first line of the body of the report, there is data about Customer 124.  This customer’s name is Sally Adams and she lives at 482 Oak in Lansing, Michigan (MI).  The Sales Representative who calls on Sally Adams is Sales Rep Number 03.</li>

 <li><strong>Identify all attributes: </strong>The attributes (or characteristics) of a User View can often be found by simply looking at the column headings. In our Customer Report we see that we have the following attributes: Customer Number, Customer Name, Street, City, State, Zip Code and Sales Representative Number.</li>

 <li><strong>Describe the relation using DBDL: </strong>Database Design Language (DBDL) is a standardized way of describing relations of a relational database. You describe a relation by:</li>

 <li>Choose an appropriate name for the relation. We chose to name our relation <strong>CUSTOMER</strong> because each line in the report describes customer data.</li>

 <li>List the attributes you found in the user view inside square brackets, giving each attribute a suitable attribute name. Note: <em>calculated fields or derived fields</em> should not be included in the DBDL</li>

 <li>Determine which attribute would be suitable as a primary key and underline that attribute.</li>

</ol>

The DBDL for the relation resulting from our Customer user view would look as follows:

CUSTOMER [ <u>CustNo</u>, CustName, CustStreet, CustCity, CustSt, CustZip, CustRep ]




Now you try it.  Examine the following report:




<strong>Premiere Corporation Parts List</strong>

<strong> </strong>

<table>

 <tbody>

  <tr>

   <td width="104"><strong>Part Number</strong></td>

   <td width="104"><strong>Part Description</strong></td>

   <td width="104"><strong>Qnty On Hand</strong></td>

   <td width="104"><strong>Class</strong></td>

   <td width="104"><strong>Warehouse</strong><strong>On Hand</strong></td>

   <td width="104"><strong>Price</strong></td>

  </tr>

  <tr>

   <td width="104">AX12</td>

   <td width="104">Iron</td>

   <td width="104">104</td>

   <td width="104">HW</td>

   <td width="104">3</td>

   <td width="104">24.95</td>

  </tr>

  <tr>

   <td width="104">AZ52</td>

   <td width="104">Dartboard</td>

   <td width="104">20</td>

   <td width="104">SG</td>

   <td width="104">2</td>

   <td width="104">12.95</td>

  </tr>

  <tr>

   <td width="104">BA74</td>

   <td width="104">Basketball</td>

   <td width="104">40</td>

   <td width="104">SG</td>

   <td width="104">1</td>

   <td width="104">29.95</td>

  </tr>

  <tr>

   <td width="104">BH22</td>

   <td width="104">Cornpopper</td>

   <td width="104">95</td>

   <td width="104">HW</td>

   <td width="104">3</td>

   <td width="104">24.95</td>

  </tr>

  <tr>

   <td width="104">BT04</td>

   <td width="104">GasGrill</td>

   <td width="104">11</td>

   <td width="104">AP</td>

   <td width="104">2</td>

   <td width="104">149.99</td>

  </tr>

  <tr>

   <td width="104">BZ66</td>

   <td width="104">Washer</td>

   <td width="104">52</td>

   <td width="104">AP</td>

   <td width="104">3</td>

   <td width="104">399.99</td>

  </tr>

  <tr>

   <td width="104">CA14</td>

   <td width="104">Griddle</td>

   <td width="104">78</td>

   <td width="104">HW</td>

   <td width="104">3</td>

   <td width="104">39.99</td>

  </tr>

  <tr>

   <td width="104">CB03</td>

   <td width="104">Bike</td>

   <td width="104">44</td>

   <td width="104">SG</td>

   <td width="104">1</td>

   <td width="104">299.99</td>

  </tr>

  <tr>

   <td width="104">CX11</td>

   <td width="104">Blender</td>

   <td width="104">112</td>

   <td width="104">HW</td>

   <td width="104">3</td>

   <td width="104">22.95</td>

  </tr>

  <tr>

   <td width="104">CZ81</td>

   <td width="104">Treadmill</td>

   <td width="104">68</td>

   <td width="104">SG</td>

   <td width="104">2</td>

   <td width="104">349.95</td>

  </tr>

 </tbody>

</table>

<strong> </strong>




What type of data does each line in the report represent? _________________________________________________________________________




_________________________________________________________________________

What attributes can you identify from the user view?




________________________________                                                            ________________________________




________________________________                                                            ________________________________




________________________________                                                            ________________________________

What would be a suitable name for the UNF relation? ___________________________

Which attribute would be suitable as a primary key?   ___________________________

Describe the UNF relation using DBDL:

_____________________________________________________________________________




<strong>Step 2:</strong><strong>  Recognize </strong><strong>Multi-valued Dependencies.                         </strong>

<strong> </strong>

For example, looking at the following User View, we see that for each Customer number, it is possible to have <strong>multiple values</strong> for the order number and order date attributes.  Therefore the order number and date are a multi-valued dependency.




<strong>Premiere Corporation Customer Orders</strong>

<strong> </strong>

<table>

 <tbody>

  <tr>

   <td width="156"><strong>Customer Number</strong></td>

   <td width="156"><strong>Name</strong></td>

   <td width="156"><strong>Order Number</strong></td>

   <td width="156"><strong>Order Date</strong></td>

  </tr>

  <tr>

   <td rowspan="2" width="156">124</td>

   <td rowspan="2" width="156">Sally Adam</td>

   <td width="156">12489</td>

   <td width="156">2016-09-02</td>

  </tr>

  <tr>

   <td width="156">12500</td>

   <td width="156">2016-09-05</td>

  </tr>

  <tr>

   <td width="156">256</td>

   <td width="156">Ann Samuels</td>

   <td width="156">12495</td>

   <td width="156">2016-09-04</td>

  </tr>

  <tr>

   <td width="156">311</td>

   <td width="156">Don Charles</td>

   <td width="156">12491</td>

   <td width="156">2016-09-02</td>

  </tr>

  <tr>

   <td width="156">315</td>

   <td width="156">Tom Daniels</td>

   <td width="156">12494</td>

   <td width="156">2016-09-04</td>

  </tr>

  <tr>

   <td rowspan="2" width="156">522</td>

   <td rowspan="2" width="156">Mary Nelson</td>

   <td width="156">12498</td>

   <td width="156">2016-09-05</td>

  </tr>

  <tr>

   <td width="156">12504</td>

   <td width="156">2016-09-05</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

Identify multi-valued dependencies in DBDL by placing brackets around them. For example the DBDL for this User View would look like this:




<strong>CUSTOMER [ <u>CustNo</u>, CustName, (OrderNum, OrderDate) ]</strong>

<strong> </strong>

Notice the brackets around the OrderNum and Orderdate attributes. This quickly and easily identifies a multi-valued dependency to someone who is reading the DBDL.




<strong>Common Mistake:  </strong>A common mistake is to incorrectly identify repeating data as a multi-valued dependency.  For example, the previous report could also have been printed in the following way:




<strong>Premiere Corporation Customer Orders</strong>

<strong> </strong>

<table>

 <tbody>

  <tr>

   <td width="156"><strong>Customer Number</strong></td>

   <td width="156"><strong>Name</strong></td>

   <td width="156"><strong>Order Number</strong></td>

   <td width="156"><strong>Order Date</strong></td>

  </tr>

  <tr>

   <td width="156"><strong>124</strong></td>

   <td width="156"><strong>Sally Adam</strong></td>

   <td width="156">12489</td>

   <td width="156">2016-09-02</td>

  </tr>

  <tr>

   <td width="156"><strong>124</strong></td>

   <td width="156"><strong>Sally Adam</strong></td>

   <td width="156">12500</td>

   <td width="156">2016-09-05</td>

  </tr>

  <tr>

   <td width="156">256</td>

   <td width="156">Ann Samuels</td>

   <td width="156">12495</td>

   <td width="156">2016-09-04</td>

  </tr>

  <tr>

   <td width="156">311</td>

   <td width="156">Don Charles</td>

   <td width="156">12491</td>

   <td width="156">2016-09-02</td>

  </tr>

  <tr>

   <td width="156">315</td>

   <td width="156">Tom Daniels</td>

   <td width="156">12494</td>

   <td width="156">2016-09-04</td>

  </tr>

  <tr>

   <td width="156"><strong>522</strong></td>

   <td width="156"><strong>Mary Nelson</strong></td>

   <td width="156">12498</td>

   <td width="156">2016-09-05</td>

  </tr>

  <tr>

   <td width="156"><strong>522</strong></td>

   <td width="156"><strong>Mary Nelson</strong></td>

   <td width="156">12504</td>

   <td width="156">2016-09-05</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

The fact that the Customer Number and Name for Sally Adams and Mary Nelson have been repeated on multiple lines does <strong>not</strong> make Customer Number and Name a multi-valued dependency!   You should still identify that for one customer number, there are multiple values for the order number and date.  Note that this does not mean that EVERY customer number will have multiple order numbers, just that this user view shows that it is <u>possible</u> for some customer numbers to have multiple values for Order Number and Date. The Multi-valued Dependency must be identified in the DBDL. Note also that it is possible to have more than 1 multi-valued dependency.

<strong> </strong>

<strong>Step 3: Create 1NF relations from UNF. </strong>

<strong> </strong>

Therefore, the process of taking a relation from UNF to 1NF, involves resolving the multi-valued dependencies.




<strong>Method:    </strong>

<ul>

 <li><strong>Choose a primary key for the multi-valued dependency. </strong></li>

 <li><strong>Identify the primary key of the multi-valued dependency by underlining it or writing (PK) .</strong></li>

 <li><strong>Rewrite the DBDL by removing the parenthesis and concatenating the original primary key with the primary key of the multi-valued dependency.</strong></li>

 <li><strong>Rewrite the DBDL with the two-part Primary Key and include all the non-key attributes.</strong></li>

</ul>

<strong> </strong>

For example, using our previous report from part B, we had the following:




UNF:    Customer [ <u>CustNo</u>, CustName, ( OrderNum, OrderDate ) ]

<strong> </strong>

<ol>

 <li><strong>Choose a primary key for the repeating group:</strong> <strong>OrderNum</strong> would make a suitable primary key for the repeating group as it uniquely identifies the data in the repeating group.</li>

 <li><strong>Rewrite the DBDL by removing the parenthesis and concatenating the original entity name with the entity name of the multi-valued dependency. </strong></li>

</ol>

CustOrder [ <u>CustNo, OrderNum</u>, CustName, OrderDate  ]

<strong> </strong>




NOTE:  If we start with a relation that does not contain any multi-valued dependencies, it is already in 1NF.




<strong>Last Section:</strong>

<strong>Lab 09 Submission:</strong>

<strong>For the following User View, determine the UNF and the 1NF and hand in this page only to your instructor. </strong>

<strong>Premiere Corporation Order Detail Report</strong>

<strong> </strong>

<table width="660">

 <tbody>

  <tr>

   <td width="66"><strong>Order Number</strong></td>

   <td width="99"><strong>Order Date</strong></td>

   <td width="83"><strong>Cust number</strong></td>

   <td width="83"><strong>Part Number</strong></td>

   <td width="82"><strong>Part Desc</strong></td>

   <td width="83"><strong>Number Ordered</strong></td>

   <td width="83"><strong>Quoted Price</strong></td>

   <td width="82"><strong>Total</strong></td>

  </tr>

  <tr>

   <td width="66">12489</td>

   <td width="99">2016-09-02</td>

   <td width="83">124</td>

   <td width="83">AX12</td>

   <td width="82">Iron</td>

   <td width="83">11</td>

   <td width="83">14.95</td>

   <td width="82">164.45</td>

  </tr>

  <tr>

   <td width="66">12491</td>

   <td width="99">2016-09-02</td>

   <td width="83">311</td>

   <td width="83">BT04</td>

   <td width="82">GasGrill</td>

   <td width="83">1</td>

   <td width="83">149.99</td>

   <td width="82">149.99</td>

  </tr>

  <tr>

   <td width="66"> </td>

   <td width="99"> </td>

   <td width="83"> </td>

   <td width="83">BZ66</td>

   <td width="82">Washer</td>

   <td width="83">2</td>

   <td width="83">399.99</td>

   <td width="82">799.98</td>

  </tr>

  <tr>

   <td width="66">12494</td>

   <td width="99">2016-09-04</td>

   <td width="83">315</td>

   <td width="83">CB03</td>

   <td width="82">Bike</td>

   <td width="83">4</td>

   <td width="83">279.99</td>

   <td width="82">1,119.96</td>

  </tr>

  <tr>

   <td width="66">12495</td>

   <td width="99">2016-09-04</td>

   <td width="83">256</td>

   <td width="83">CX11</td>

   <td width="82">Blender</td>

   <td width="83">2</td>

   <td width="83">22.95</td>

   <td width="82">45.90</td>

  </tr>

  <tr>

   <td width="66">12498</td>

   <td width="99">2016-09-05</td>

   <td width="83">522</td>

   <td width="83">AZ52</td>

   <td width="82">Dartboard</td>

   <td width="83">2</td>

   <td width="83">12.95</td>

   <td width="82">25.90</td>

  </tr>

  <tr>

   <td width="66"> </td>

   <td width="99"> </td>

   <td width="83"> </td>

   <td width="83">BA74</td>

   <td width="82">Basketball</td>

   <td width="83">4</td>

   <td width="83">24.95</td>

   <td width="82">99.80</td>

  </tr>

  <tr>

   <td width="66">12500</td>

   <td width="99">2016-09-05</td>

   <td width="83">124</td>

   <td width="83">BT04</td>

   <td width="82">GasGrill</td>

   <td width="83">3</td>

   <td width="83">149.99</td>

   <td width="82">449.97</td>

  </tr>

  <tr>

   <td width="66">12504</td>

   <td width="99">2016-09-05</td>

   <td width="83">522</td>

   <td width="83">CZ81</td>

   <td width="82">Treadmill</td>

   <td width="83">2</td>

   <td width="83">325.99</td>

   <td width="82">651.98</td>

  </tr>

 </tbody>

</table>




<strong> </strong>