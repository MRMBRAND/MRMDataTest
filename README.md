# MRMDataTest

MRM collects data on products displayed on food and drink menus. Although the product details come from a controlled database, this information can be changed directly by the user when creating a menu.

In this test we would like you to create the code that takes a CSV file containing product details entered by users on menus and finds matches to known product brand names.

Data sources:

- `input.csv`: A dump of product names and descriptions entered by users on menus
- `terms.csv`: A list of brand names which may be mentioned in product names and descriptions

Your code should demonstrate this functionality:

- Some business logic that takes the `input.csv` file as an input stream and uses stream processing to analyse each row
- Some business logic that uses a pattern matching approach of your choice to identify if a row contains term matches from the `terms.csv` (consider terms in the `input.csv` not being spelled correctly)
- A data layer that writes matches found in form of `MenuId`, `TermId` to a Postgres database using a write stream

Constraints:

- Use Python
- Use Postgres to store matches
- To make your code scaleable, everything has to be streamed
- Use any frameworks and libraries of your choice
- Write unit tests
- Timebox your work to not more than 4 hours

Bonus task:

- Add a simple REST API that can be used to call your code by posting the `input.csv` file to it