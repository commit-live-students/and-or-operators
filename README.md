![GitHub Logo](https://s3.ap-south-1.amazonaws.com/greyatom-social/GreyAtom-logo.png)

# AND and OR Conjunctive Operators

The SQL AND & OR operators are used to combine multiple conditions to narrow data in an SQL statement. These two operators are called as the conjunctive operators.

These operators provide a means to make multiple comparisons with different operators in the same SQL statement.

## The AND Operator

The AND operator allows the existence of multiple conditions in an SQL statement's WHERE clause.

### Syntax
The basic syntax of the AND operator with a WHERE clause is as follows −

        SELECT column1, column2, columnN
        FROM table_name
        WHERE [condition1] AND [condition2]...AND [conditionN];

You can combine N number of conditions using the AND operator. For an action to be taken by the SQL statement, whether it be a transaction or a query, all conditions separated by the AND must be TRUE.

Following is an example, which would fetch the all fields from the Customers table, where the City is London and PostalCode is WA1 1DP.

        Select * from greyatom.Customers WHERE City='London' AND PostalCode = 'WA1 1DP';

This would produce the following result −

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| ---------- | ------------ | ----------- | ------- | ---- | ---------- | ------- |
| 4 |	Around the Horn |	Thomas Hardy |	120 Hanover Sq.	 | London |	WA1 1DP	 | UK |


## The OR Operator

The OR operator is used to combine multiple conditions in an SQL statement's WHERE clause.

### Syntax
The basic syntax of the OR operator with a WHERE clause is as follows −

        SELECT column1, column2, columnN
        FROM table_name
        WHERE [condition1] OR [condition2]...OR [conditionN]
You can combine N number of conditions using the OR operator. For an action to be taken by the SQL statement, whether it be a transaction or query, the only any ONE of the conditions separated by the OR must be TRUE.

### Example
The following code block has a query, which would fetch all fields from Customers table where PostalCode is WA1 1DP OR EC2 5NT.

        Select * from greyatom.Customers WHERE PostalCode = 'WA1 1DP' OR PostalCode = 'EC2 5NT';

This would produce the following result −

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| ---------- | ------------ | ----------- | ------- | ---- | ---------- | ------- |
| 4 |	Around the Horn |	Thomas Hardy |	120 Hanover Sq.	 | London |	WA1 1DP	 | UK |
| 11 |	B's Beverages |	Victoria Ashworth |	Fauntleroy Circus | London |	EC2 5NT |	UK |
