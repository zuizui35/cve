SQL injection exists in the hr-system

website: https://github.com/BradWenqiang/hr

version: 2.0

Function point: Background Management---->User query function

Route: r=bishe/register?userName=

The injection parameter: userName exists

The database name was successfully exploded using sqlmap
![image-20240304005500928](https://github.com/zuizui35/cve/assets/162043156/01e697d1-9409-4fbe-a5bd-ff90a92f34c3)

Invoke the selectAll() method through the userName parameter

![image-20240304005641617](https://github.com/zuizui35/cve/assets/162043156/a32a9827-4c36-4cd6-8ff6-468795ddeb9b)


The selectAll() method calls the selectAll() method of the service layer
![image-20240304005743154](https://github.com/zuizui35/cve/assets/162043156/49ecd378-df86-4241-95f1-bcfca34d0d5b)


The selectAll() method calls the selectAllListPage() method of the mapper layer

![image-20240304005816927](https://github.com/zuizui35/cve/assets/162043156/e6c20aa7-6671-4dcc-9115-66c30aa8dcbb)


Finally, the SQL statement is executed in the selectAllListPage() method

![image-20240304005925739](https://github.com/zuizui35/cve/assets/162043156/de689195-8f7c-46af-8de0-d1b61af782da)
