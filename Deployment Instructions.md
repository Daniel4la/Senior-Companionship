# **Deployment Instructions**

## **Importing the Solution into Microsoft Power Platform**

### **Step 1: Download and Set Up** 

1. **Download the solution** “MK-508 Senior Companionship" from the provided source.  
2. **Sign up for Microsoft Power Platform** and log in to your account.  
3. Navigate to **Power Pages**, then select the **environment** where you want to import the solution.

### **Step 2: Import the Solution** 

4. In the **left-hand panel**, go to **Solutions**, then click **Import**.  
5. Select the solution file you previously downloaded.  
6. If a **connection needs to be re-established** (e.g., with Office 365 Outlook):

   * Click the **three-dot menu** (⋮) next to the connector.

   * Choose **Add new connection**.

7. Sign in using a **valid Outlook account** to finalize the connection.  
8. Click **Import** to complete the process.

### **Step 3: Activate Your Power Pages Site** 

9. Once imported, navigate to **Power Pages Home**, then to the **Inactive Sites** tab.  
10. Locate your newly imported site and click **Reactivate**.  
11. Choose a new **site name or web address** and click **Done**.  
12. Your site is now active and accessible.

### **Step 4: Adjust Site Privacy Settings (Optional)** 

13. If you want to modify who can access the site:

* Click **Edit Site**.

* Go to **Security \> Site Visibility**.

* Choose between **Private** (default) or **Public** access, depending on your needs.

## **Chatbot Agent Setup (Copilot Studio)** 

### **Step 1: Access Copilot Studio** 

1. Open **Microsoft Copilot Studio** using the **same Microsoft account** and **environment** as before.  
2. In the **Agents** tab, locate and select **"Senior Companion"**.

### **Step 2: Configure Authentication** 

3. Navigate to: **Settings \> Security \> Authentication**.  
4. To allow users to access the chatbot, you must **configure manual authentication**.  
5. Follow the official Microsoft guide for copilot authentication setup:

* [Copilot Studios \- Configure end-user authentication](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configuration-end-user-authentication)   
* [Copilot Studio \- Configure Entra ID Authentication](https://learn.microsoft.com/en-us/microsoft-copilot-studio/configuration-authentication-azure-ad?tabs=fic-auth)

## **Power Pages Google Authentication Setup** 

### **Step 1: Begin Google Auth Configuration** 

1. In **Power Pages**, edit your newly activated site.  
2. Navigate to **Security \> Identity Providers**, then choose **Google**.  
3. Click the provided **link to the Google Console** and **copy the Redirect URL** listed on the page.

### 

### **Step 2: Configure Google Cloud** 

4. In the Google Cloud Console:

* Click **“Get Started”** under Google Auth Platform. Or [https://console.cloud.google.com/auth/branding](https://console.cloud.google.com/auth/branding) 

5. Set up basic app information:

* Provide a **name** for your app.

* Enter a **support email address**.

* Choose **“External”** for public access (or **“Internal”** if restricted to your organization).

6. On the next screen, enter your **contact email** and click **Create**.

### **Step 3: Add OAuth Credentials** 

7. Open the **left-side navigation menu** → go to **API & Services \> Credentials**.  
8. Click **Create Credentials** → select **OAuth Client ID**.  
9. Choose **“Web Application”**, enter a name, and **paste the Redirect URL** (from Step 3\) under **Authorized Redirect URLs**.  
10. Click **Create** to finalize the setup.

***Note:** Google authentication may take several minutes to a few hours to activate.*

11. Follow the official Microsoft guide for Google OAuth setup:  
* [Google OAuth Configuration for Power Pages](https://learn.microsoft.com/en-us/power-pages/security/authentication/oauth2-google)
