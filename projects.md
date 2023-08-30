Example 1: Create a New Project

bash

curl -X POST -H "Content-Type: application/json" -d '{
  "nickname": "MyProject",
  "projectTitle": "Project ABC",
  "projectDescription": "This is a sample project",
  "projectCategory": "Technology",
  "amountToRaise": 10000,
  "minimumBuyIn": 100,
  "roi": 5,
  "stakeAmount": 200,
  "photo": "project.jpg"
}' https://malaika-backend-server.onrender.com/api/projects

Example 2: Get All Projects

bash

curl https://malaika-backend-server.onrender.com/api/projects

Example 3: Update Project Details

bash

curl -X PUT -H "Content-Type: application/json" -d '{
  "projectTitle": "Project ABC",
  "projectDescription": "Updated description"
}' https://malaika-backend-server.onrender.com/api/projects/user/user123

Example 4: Update Project's User Field

bash

curl -X PUT https://malaika-backend-server.onrender.com/api/projects/update-user/user456/Project%20XYZ

Example 5: Get Projects Without User Address

bash

curl https://malaika-backend-server.onrender.com/api/projects/projects-without-user

Example 6: Delete a Project

bash

curl -X DELETE https://malaika-backend-server.onrender.com/api/projects/user/user123/Project%20ABC

Example 7: Get Deleted Project's Contributors

bash

curl https://malaika-backend-server.onrender.com/api/projects/fetch-contributors/user123/Project%20ABC

Example 8: Return Contributions After Delete

bash

curl -X POST -H "Content-Type: application/json" -d '[
  {
    "contributorsAddress": "contributor1",
    "projectTitle": "Project ABC",
    "contributionAmount": 100,
    "user": "user123"
  }
]' https://malaika-backend-server.onrender.com/api/projects/return-contributions

Example 9: Get Projects by User Address

bash

curl https://malaika-backend-server.onrender.com/api/projects/user/user123
