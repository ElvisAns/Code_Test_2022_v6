# The review report for the code

The overall structure is good and i am pleased you are using the Repository Design pattern which may make things easy if 
we want to switch our source of datas from Eloquent to an other provider (Even an external API of course).

- An other good observation is that almost all the string are enclosed in single  quote and this save time since the PHP engine will try to find variable within  the string and i will print it as is.
- I saw the environement variables are playing alot in the RBAC and i would discourage this. The Role Based Access could be managed by storing role ids in the database  to allow them being easily managed programmatically.
- Another good news is that nowadays laravel is shipped with well structured RBAC and even more with fortify...We can delegate it to manage **authorization** and **authentication** as a middleware for specifics route and verbs; with that we won't need to reverify auth in each controller method.
- An suggestion would be to use the Event subscription class in the whole application instead of hardcoding logging and actions on each event.


## A short note about the test

To be honest i didn't expect such a structure for testing.

I would have, personnaly, wrote unit tests for each route and even more
with feature test on our controllers methods.



## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://elvisansima.netlify.app/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/cibalinda-elvis)