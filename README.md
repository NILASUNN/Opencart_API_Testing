**OpenCart API Automation – Postman | Newman | Jenkins**

**Project Overview**

This project focuses on automating OpenCart REST APIs for cart functionality using Postman. The Postman collections are executed using Newman CLI and integrated with Jenkins for Continuous Integration (CI). The project demonstrates API testing, automation, token-based authentication, and CI/CD integration.

**🛠 Tools & Technologies Used**
1. Postman
2. Newman (CLI)
3. Jenkins
4. Git & GitHub
5. OpenCart
6. REST API
7. JavaScript (Postman Test Scripts)
8. JSON

**Automated API Workflow**

The following OpenCart APIs were automated:
1. API Login (Generate Token)
2. Add Product to Cart
3. Get Cart Products
4. Edit Product Quantity in Cart
5. Remove Product from Cart

This simulates an end-to-end cart workflow.

**Authentication**
1. Token-based authentication is used.
2. API token is generated using the login API.
3. The token is stored in collection/environment variables and used in subsequent requests.

**📂 Project Structure**
Opencart_API_Testing
│
├── collection.json
├── env.json
├── README.md


**▶️ How to Run the Project**
1. Install Newman
npm install -g newman
2. Start OpenCart
Start Apache and MySQL from XAMPP and make sure OpenCart is running:
http://127.0.0.1/opencart-3.0.3.8/upload/
3. Run Collection Using Newman
newman run collection.json -e env.json


**🤖 Jenkins Integration**
1. Jenkins is configured to run Newman collections.
2. The build executes Newman using a Windows batch command.
3. This enables automated API testing in a CI/CD pipeline.
   
**Example Jenkins Command:**
newman run collection.json -e env.json

**Jenkins CI Integration**
The Postman collection is executed using Newman through Jenkins as part of Continuous Integration.

### Jenkins Build Success
![Jenkins Build](screenshots/jenkins_build_success.png)

**✅ Validations Performed**
1. Status code validation
2. Response body validation
3. Token extraction and reuse
4. Cart product validation
5. Success message validation

**📊 Key Features**
1. Token-based authentication handling
2. Dynamic environment variables
3. End-to-end cart workflow automation
4. Newman CLI execution
5. Jenkins CI integration
6. GitHub version control

**👩‍💻 Author**
Abinaya
