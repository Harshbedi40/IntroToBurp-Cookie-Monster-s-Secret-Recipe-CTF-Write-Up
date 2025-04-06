# **IntroToBurp-CTF-WriteUp**

# Step 1: Open the Website and Burp Suite
* First, open the website by clicking on the provided link in the challenge description.
* Simultaneously, launch Burp Suite in your browser. Burp Suite will intercept and analyze your web traffic.

# Step 2: Copy the URL and Paste in Burp Suite Browser
* Copy the URL of the website from your browser's address bar.
* Paste this URL into Burp Suite's browser tab to ensure Burp Suite intercepts the web traffic.

# Step 3: Fill in the Registration Details
* Once the website loads, fill in the registration details in the appropriate form fields (e.g., username, password, email).
* After entering the information, click the "Register" button to submit the form.

# Step 4: Two-Factor Authentication (2FA) and Interception
* After registration, you'll be prompted to enter a One-Time Password (OTP) for two-factor authentication (2FA).
* Before entering the OTP, go to Burp Suite and click on the "Intercept" tab.
* In Burp Suite, set the intercept to "on" so that Burp can capture the request when you attempt to submit the OTP.

# Step 5: View the OTP in Burp Suite
* After entering any random 4-digit number for the OTP, the intercept will capture the request.
* In Burp Suite, click on the intercepted OTP request to view the number that was captured.

# Step 6: Modify the OTP Request
* In the intercepted request, remove the OTP number that was originally entered.
* After that, click the "Forward" button at the top of Burp Suite to forward the request with the modified OTP.

# Step 7: Find the Flag
* Once the request is forwarded, you will be presented with the flag.
* Copy the flag, which will be displayed in the response or somewhere on the page.

# Step 8: Submit the Flag
* Paste the flag into the picoCTF platform to complete the challenge.


Here's an enhanced version of your write-up that makes the steps clearer, more structured, and engaging for your GitHub post:

---

# **Cookie Monster's Secret Recipe-CTF-WriteUp**

# **Step-by-Step Guide**

# **Step 1: Open the Website**
- First, navigate to the challenge website by clicking on the link provided. Additionally, open **CyberChef** in your browser—this will be helpful for decoding the hidden data.

### **Step 2: Enter Credentials**
- Enter **"Admin"** as both the **username** and **password** in the login form.
- However, **DO NOT** click on the **Register** button yet. This is important for the next steps!

### **Step 3: Inspect the Application**
- Right-click anywhere on the webpage and select **Inspect** (or press `Ctrl + Shift + I`).
- In the **Developer Tools** window, go to the **Application** tab. This is where you'll investigate the cookies and local storage.

### **Step 4: Click the Register Button**
- Now, click the **Register** button on the page. At this point, the application will trigger certain actions that modify the cookies.

### **Step 5: Refresh the Application Page**
- Refresh the application page after clicking **Register**. You’ll notice that new data will appear, though it may seem unreadable at first.
- Look closely in the **Application** tab, and you’ll spot a string of **garbled** or **encoded** text in the cookies or local storage.

### **Step 6: Copy the Encoded Data**
- Copy the unreadable string you find in the **Application** tab. This is the encoded data that contains the flag.

### **Step 7: Decode the Data with CyberChef**
- Go back to **CyberChef** and paste the copied string into the input field.
- Now, apply the following operations:
  - **URL Decode**: This will decode any URL-encoded characters.
  - **Base64 Decode**: This will decode the string from Base64 encoding.

### **Step 8: Get the Flag**
- After applying both decoders, click on the **Bake** button in CyberChef.
- The output will reveal the **flag** in a human-readable format.

### **Step 9: Submit the Flag**
- Copy the flag from CyberChef and head back to **picoCTF**.
- Paste the flag into the appropriate submission field and click **Submit**.
