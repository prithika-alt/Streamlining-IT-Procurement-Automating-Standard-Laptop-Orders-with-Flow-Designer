# Streamlining IT Procurement: Automating Standard Laptop Orders with Flow Designer

## 📌 Project Overview
This project automates the procurement and configuration workflow for standard laptop orders using **ServiceNow Flow Designer**. The traditional procurement process involves manual handoffs that often cause fulfillment delays, configuration oversights, and inefficient resource allocation. This solution establishes an automated workflow that generates and assigns a catalog task directly to the Hardware team upon request approval.

## 🎯 Problem Statement
Manual handling in enterprise IT procurement leads to operational bottlenecks, particularly during post-approval hardware staging. Without automation, handoffs between approvers and technicians risk delayed fulfillment, missed configuration steps, and unnecessary administrative workload.

## 💡 Project Objectives
* Provide a standardized self-service interface for users requesting standard laptops.
* Automatically trigger hardware configuration tasks upon order approval.
* Route fulfillment tasks directly to the Hardware assignment group.
* Eliminate manual task assignment errors and streamline handoffs.
* Improve IT department resource utilization and fulfillment efficiency.

## 🛠️ Technology Used
* **ServiceNow**
* **Flow Designer**
* **Service Catalog**
* **Catalog Tasks (`sc_task`)**

## ⚙️ Workflow
1. The user submits a request for a **Standard Laptop** via the Service Catalog.
2. The submitted request routes to the designated approver.
3. Upon approval, the **Standard Laptop Task** flow triggers automatically.
4. Flow Designer creates a fulfillment **Catalog Task**.
5. The task is populated with the short description **"Laptop need to Configured"**.
6. The task is assigned directly to the **Hardware** group.
7. The Hardware team completes staging and configuration.
8. Task status and completion updates reflect automatically on the Requested Item (`RITM`) record.

## 🔄 Flow Configuration

* **Flow Name:** `Standard Laptop Task`
* **Trigger:** Service Catalog
* **Action:** Create Catalog Task

### Task Parameters
* **Requested Item:** `Requested Item Record`
* **Short Description:** `Laptop need to Configured`
* **Description:** `Laptop need to Configured`
* **Assignment Group:** `Hardware`
* **Approval:** `Approved`

## 🧩 Service Catalog Configuration
The flow is linked directly to the catalog item record:

**Service Catalog → Maintain Items → Standard Laptop → Process Engine → Flow**

Any existing legacy workflow associations are cleared, and the **Standard Laptop Task** flow is mapped and activated.

## 🧪 Testing the Workflow
1. Open the **ServiceNow** instance.
2. Navigate to **Service Catalog** > **Hardware**.
3. Select **Standard Laptop** and click **Order Now**.
4. Open the generated **Request (`REQ`)** record.
5. Locate the **Approvers** tab and approve the request.
6. Navigate to the associated **Requested Item (`RITM`)**.
7. Inspect the **Catalog Tasks** related list.
8. Open the generated task and verify the assignment group is set to **Hardware** and the short description displays **"Laptop need to Configured"**.

## ✅ Expected Result
Once the requisition is approved, ServiceNow automatically generates a configuration task assigned to the **Hardware** group without requiring manual ticket creation or dispatch.

## 📈 Benefits
* Faster laptop turnaround and reduced employee wait times.
* Reduced manual overhead for IT service desk agents.
* Consistent hardware preparation and configuration compliance.
* Clear accountability through automatic group assignment.

## 📌 Conclusion
By automating standard laptop procurement using ServiceNow Flow Designer, this project removes manual routing bottlenecks and ensures immediate task generation upon approval. The resulting workflow delivers higher operational efficiency, improved tracking, and an optimized user fulfillment experience.

## 🎥 Demo
* **Demo Link:** `Add your demo link here`

## 👨‍💻 Project Details
* Developed as part of the **Naan Mudhalvan** project curriculum.
