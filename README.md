# nodejs-demo-app

# 🚀 Node.js CI/CD Pipeline with Docker & GitHub Actions

This project demonstrates a complete CI/CD pipeline for a Node.js application using **Docker** and **GitHub Actions**. Every push to the `main` branch automatically builds a Docker image and pushes it to **DockerHub**.

---

## 📦 Tech Stack Used

- **Node.js** (with Express)
- **Docker(CLI)**
- **GitHub Actions**
- **DockerHub**

---

## 📁 Project Structure

.github/
├── workflows/
    └── main.yml
nodejs-demo-app/
├── app.js
├── package.json
├── Dockerfile

---

## 🔧 Setup Instructions

### 1. create code files
```bash
touch app.js package.json Dockerfile
```
This command create the empty files now open these files using your favourite editor and add or write your code in these files

### 2. Add data in code files
```bash
nano app.js
nano package.json
nano Dockerfile
```
### 3. Create a repo on dockerhub manually to push the created image of node.js app

Open your browser and go to:
```link
https://hub.docker.com
```
Log in with your DockerHub account credentials Create a new account if you don't have any.

After logging in, click on your profile icon in the top-right corner.

From the dropdown, click “Repositories”.

On the “Repositories” page, click the “Create Repository” button (usually top-right).

Fill Out Repository Details:

| **Field**            | **Value**                                      |
|----------------------|------------------------------------------------|
| Repository Name      | `nodejs-cicd-app` (or any name you prefer)     |
| Visibility           | Choose `Public` or `Private`                   |
| Description (Optional)| Something like `"Node.js CI/CD app"`          |


### 4. Add DOCKER_USERNAME & DOCKER_PASSWORD in repo secrets

1) Go to your GitHub repository.

2) Click on the “Settings” tab near the top right of the page.

3) In the left-hand sidebar, scroll down and click on “Secrets and variables” under the “Security” section.

4) Click on “Actions” (under “Secrets and variables”).

5) Click the “New repository secret” button.

In the name section paste this as it is
Name: DOCKERHUB_USERNAME

In the value section paste your dockerhub username
Value: Enter your DockerHub username

Click “Add secret”


Now Click on the “New repository secret” button again and this time.

In the name section paste this as it is
Name: DOCKERHUB_PASSWORD


In the value section paste your dockerhub password
Value: Enter your DockerHub password
(You can also use a DockerHub access token instead for better security)

Click “Add secret”



### 5. Configure CI/CD using github action for that create a main.yml
### Go to your code repo

![image](https://github.com/user-attachments/assets/e9d28587-5b72-458f-ac9b-3b610b204675)

### Click on Actions

### Now click on  set up a workflow yourself to configure the CI/CD or Configure as you want i.e. using jenkins or any other tool.

![image](https://github.com/user-attachments/assets/19477d2f-6f51-4e63-8840-5670a74e81db)

### Paste your workflow code or main.yml content in this file as shown below & click on commit change

![image](https://github.com/user-attachments/assets/28380de2-a394-4c54-920c-3d929cfd128c)


### 6. Go to actions after Commiting the main.yml

### you will see this interface there
![image](https://github.com/user-attachments/assets/d2f6eb48-0ee8-4f4c-9986-183395879f38)
### This means your CI/CD is created and now the instructions written in main.yml is in execution

### You can check the logs by clicking on build-and-deploy the output should be look like this:
![image](https://github.com/user-attachments/assets/3de31e2c-6e00-4603-8680-dd6c3c5009ac)

### If the main.yml is executed succesfully you will see this:
![image](https://github.com/user-attachments/assets/ef117e5c-bf5a-4513-992b-601923efa9c1)
### if any error is exist check the logs and solve it.


### TO confirm your depolyment is successfull or not login to your dockerhub account and see the images is prsent in your the repo which you create
![image](https://github.com/user-attachments/assets/f0cf06b3-38b0-4816-84da-e8a32cb54895)

### If you see this image in your Dockerhub repo means your deployment is successful.
