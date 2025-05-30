# **IntroToBurp-CTF-WriteUp**

# Step 1: Open the Website and Burp Suite
* First, open the website by clicking on the provided link in the challenge description.
* Simultaneously, launch Burp Suite in your browser. Burp Suite will intercept and analyze your web traffic.

  ![image](https://github.com/user-attachments/assets/3bd166ee-a6e8-4317-8d83-3c6702417a14)


# Step 2: Copy the URL and Paste in Burp Suite Browser
* Copy the URL of the website from your browser's address bar.
  ![image](https://github.com/user-attachments/assets/e2d49c3d-7b91-447e-bf18-3f90f6ed1bee)

* Paste this URL into Burp Suite's browser tab to ensure Burp Suite intercepts the web traffic.
  ![image](https://github.com/user-attachments/assets/3acc61b6-342d-402e-9276-07d713082e22)


# Step 3: Fill in the Registration Details
* Once the website loads, fill in the registration details in the appropriate form fields (e.g., username, password, email).
* After entering the information, click the "Register" button to submit the form.
  ![image](https://github.com/user-attachments/assets/e1c6d552-82e5-4788-808c-12e29a638474)


# Step 4: Two-Factor Authentication (2FA) and Interception
* After registration, you'll be prompted to enter a One-Time Password (OTP) for two-factor authentication (2FA).
* Before entering the OTP, go to Burp Suite and click on the "Intercept" tab.
* In Burp Suite, set the intercept to "on" so that Burp can capture the request when you attempt to submit the OTP.
  ![image](https://github.com/user-attachments/assets/fe807165-fd62-4567-ac46-8887428cdac5)


# Step 5: View the OTP in Burp Suite
* After entering any random 4-digit number for the OTP, the intercept will capture the request.
  ![image](https://github.com/user-attachments/assets/c4035464-6a32-424f-96a4-3ff350c2b6f3)

* In Burp Suite, click on the intercepted OTP request to view the number that was captured.

# Step 6: Modify the OTP Request
* In the intercepted request, remove the OTP option that was originally entered.
* After that, click the "Forward" button at the top of Burp Suite to forward the request with the modified OTP.
  ![image](https://github.com/user-attachments/assets/60a4a35d-c01c-4e6f-bf09-993dcf0b49bc)


# Step 7: Find the Flag
* Once the request is forwarded, you will be presented with the flag.
* Copy the flag, which will be displayed in the response or somewhere on the page.
  ![image](https://github.com/user-attachments/assets/7e668c59-f3d6-47b3-bdf4-97bc1ecbd668)


# Step 8: Submit the Flag
* Paste the flag into the picoCTF platform to complete the challenge.
  ![image](https://github.com/user-attachments/assets/1dd4ac09-c8a7-40e5-8f52-47c1082bf30a)

  

# **Cookie Monster's Secret Recipe-CTF-WriteUp**

# **Step-by-Step Guide**

# **Step 1: Open the Website**
- First, navigate to the challenge website by clicking on the link provided. Additionally, open **CyberChef** in your browser—this will be helpful for decoding the hidden data.
  ![image](https://github.com/user-attachments/assets/9640e4df-3016-437d-a51b-b8f5d95bf538)
  ![image](https://github.com/user-attachments/assets/37702bcb-a256-4f98-aa29-80b8d74a9ed7)

### **Step 2: Enter Credentials**
- Enter **"Admin"** as both the **username** and **password** in the login form.
  ![image](https://github.com/user-attachments/assets/facdda34-29f9-4dce-838e-f314d95eaa72)
  
- However, **DO NOT** click on the **Register** button yet. This is important for the next steps!

### **Step 3: Inspect the Application**
- Right-click anywhere on the webpage and select **Inspect** (or press `Ctrl + Shift + I`).
  ![image](https://github.com/user-attachments/assets/257cc21a-6a38-4190-800e-5f52a8d777fe)

- In the **Developer Tools** window, go to the **Application** tab. This is where you'll investigate the cookies and local storage.
  ![image](https://github.com/user-attachments/assets/fb88c622-f4a1-4ddb-aba8-5c2bf12376a7)


### **Step 4: Click the Register Button**
- Now, click the **Register** button on the page. At this point, the application will trigger certain actions that modify the cookies.

### **Step 5: Refresh the Application Page**
- Refresh the application page after clicking **Register**. You’ll notice that new data will appear, though it may seem unreadable at first.
- Look closely in the **Application** tab, and you’ll spot a string of **garbled** or **encoded** text in the cookies or local storage.
  ![image](https://github.com/user-attachments/assets/597a09eb-138e-4003-ba9a-d1a8ce985b6d)


### **Step 6: Copy the Encoded Data**
- Copy the unreadable string you find in the **Application** tab. This is the encoded data that contains the flag.
  ![image](https://github.com/user-attachments/assets/17be2152-a18e-4762-8813-79f4ff3a1268)


### **Step 7: Decode the Data with CyberChef**
- Go back to **CyberChef** and paste the copied string into the input field.
  ![image](https://github.com/user-attachments/assets/8baeca1c-90f0-4fa8-9241-7405f51e937a)

- Now, apply the following operations:
  - **URL Decode**: This will decode any URL-encoded characters.
  - **Base64 Decode**: This will decode the string from Base64 encoding.
- now you cleraly able to see the flag if not just click on bake option
  ![image](https://github.com/user-attachments/assets/9bd6c649-dcfb-4f9c-a2ff-d884e710605a)


### **Step 9: Submit the Flag**
- Copy the flag from CyberChef and head back to **picoCTF**.
  ![image](https://github.com/user-attachments/assets/4d25aa63-8341-4a0e-ac69-67fa5d91876c)

- Paste the flag into the appropriate submission field and click **Submit**.
  ![image](https://github.com/user-attachments/assets/9ffe67db-d662-4e7c-a60b-d7cf4d21abb7)



# **Bookmarklet Web Vulnerability-CTF-WriteUp**

### **Step 1: Open the Website**
- Click [**here**](#) to access the vulnerable website. Once you open it, you will be able to see the JavaScript code displayed on the page.
  ![image](https://github.com/user-attachments/assets/f5f2c4f7-2e51-4c7a-a02d-58b0e4235946)


### **Step 2: Copy the JavaScript Code**
- Highlight the displayed JavaScript code and copy it to your clipboard. This will be used to create the bookmarklet.
  ![image](https://github.com/user-attachments/assets/21b940c0-58f3-4b79-b566-960ea354d326)


### **Step 3: Create a Bookmark**
- Create a new bookmark in your browser. To do this, click on the “Done” button. At this point, clicking on the bookmark will not trigger any action, but this is part of the process.
  ![image](https://github.com/user-attachments/assets/a4a99304-cbe7-4ff8-943f-b5ea55838ad0)


### **Step 4: Edit the Bookmark**
- Right-click on the bookmark you just saved and select the **Edit** option from the context menu.
  ![image](https://github.com/user-attachments/assets/da2e5499-e1aa-4831-8ee3-0e8c72f879df)


### **Step 5: Modify the Bookmark's URL**
- In the edit menu, leave the bookmark's name unchanged. However, clear the existing URL and replace it with the JavaScript code you copied earlier. After pasting the code, click “Done” to save the changes.
  ![image](https://github.com/user-attachments/assets/7563acbc-9030-4bef-82dd-086d0f4cdb38)


### **Step 6: Trigger the Bookmarklet**
- Now, when you click on the bookmark, a pop-up will appear at the top of the page. This pop-up contains the flag you need.
  ![image](https://github.com/user-attachments/assets/eea4d85e-505e-4028-9a16-d184ec13f06f)


### **Step 7: Submit the Flag**
- Copy the flag from the pop-up and head over to the [picoCTF submission page](#). Paste the flag in the submission form by clicking on the "Submit Flag" button.
  ![image](https://github.com/user-attachments/assets/4a71be56-1590-449a-b7f6-64d54f263e5f)



# **Local Authority Web Vulnerability-CTF-WriteUp**

### **Step 1: Open the Website**
- Start by opening the vulnerable website by clicking on the [**website**](#) link. Once the page loads, you should see the **username** and **password** displayed on the screen.
  ![image](https://github.com/user-attachments/assets/da8e3e1c-ac56-4706-923d-4ff83ec26a65)


### **Step 2: Enter the Default Credentials**
- In the login form, enter **"admin"** as both the **username** and **password**. However, **do not** click the **Login** button yet.
  ![image](https://github.com/user-attachments/assets/c39de966-4fef-44ce-b793-8c143964a38d)


### **Step 3: Inspect the Page**
- Right-click anywhere on the page and select **Inspect** from the context menu. This will open the developer tools.
  ![image](https://github.com/user-attachments/assets/c6c43354-5bac-4b19-9aec-2bb99c6f5921)

 
- Go to the **Sources** tab in the developer tools. You won’t find any JavaScript files listed at this point.
![image](https://github.com/user-attachments/assets/53107ed5-153a-494b-9385-22ad0741feee)


### **Step 4: Click the Login Button**
- Now, click on the **Login** button. After doing this, you should be able to see a **JavaScript file** listed under the Sources tab that wasn’t there before.

### **Step 5: Examine the JavaScript File**
- Click on the newly visible JavaScript file. Within this file, you’ll find the **username** and **password** that are necessary for the next step.
  ![image](https://github.com/user-attachments/assets/28d7db01-2655-4694-9b4b-e9df9ac06c55)


### **Step 6: Enter the Retrieved Credentials**
- Return to the login form and replace **"admin"** with the **username** and **password** you found in the JavaScript file. Once entered, click the **Login** button.

### **Step 7: Retrieve and Submit the Flag**
- Upon successful login, you will be shown the **flag**. Copy the flag and head over to the [picoCTF submission page](#). Paste the flag into the submission form and click **Submit Flag**.
  ![image](https://github.com/user-attachments/assets/a9bb54d2-a56c-43a6-b555-8432a83670f4)



Sure! Here's a cleaned-up and more attractive version of your **PicoCTF challenge writeup for "n0s4n1ty 1"**, ideal for putting on GitHub. I’ve corrected the grammar, improved clarity, and added some formatting for better readability.

---

## 🕵️ PicoCTF: *n0s4n1ty 1* — Web Exploitation-CTF-Writeup

#### 🔹 **Step 1:**  
Click on the link labeled **"here"** to open the target website. You’ll land on a web page where you’re prompted to upload a file/profile.
![image](https://github.com/user-attachments/assets/ee24bb15-8140-4172-9a82-eebbd3b53739)


#### 🔹 **Step 2:**  
Create a simple `.txt` file and insert a **malicious payload** into it. You can use **ChatGPT** to generate this payload — just ask it for a PHP web shell or a suitable payload for solving this PicoCTF challenge.

#### 🔹 **Step 3:**  
Once you receive the payload, paste it into your `.txt` file and **save it as** `shell.php`.

#### 🔹 **Step 4:**  
Now go back to the website. Click on **"Choose File"**, select the `shell.php` file you just created, and then click on **"Upload File"**.
![image](https://github.com/user-attachments/assets/66cddd7a-905e-4a6d-bc39-6a23a0e392ac)


#### 🔹 **Step 5:**  
After uploading, you’ll be given a **file path**. Copy this path and paste it into the URL bar of your browser, like so:

```
uploads/shell.php?cmd=whoami
```

Make sure to append this after the base URL (don't forget to include any numeric ID or directory structure if present
![image](https://github.com/user-attachments/assets/6eae826b-809b-440d-b801-9a9b736081e5)


---

#### 🔹 **Step 6:**  
If everything worked, you’ll see the result of the `whoami` command, which confirms the shell is active. You can now execute additional commands by modifying the `cmd` parameter.

To directly retrieve the flag, run:

```
uploads/shell.php?cmd=sudo%20cat%20/root/flag.txt
```

Note: Use `%20` in place of spaces in the URL.
![image](https://github.com/user-attachments/assets/9c8cddfc-87f5-4777-9a04-0b85304d214b)


---

#### 🔹 **Step 7:**  
🎉 **Congratulations!** You’ll see the flag displayed on the screen. Copy it, paste it into the PicoCTF flag submission box, and click **"Submit Flag"** to complete the challenge.


Here's a polished and GitHub-ready version of your **PicoCTF challenge writeup for "WebDecode"**, with corrected grammar, better formatting, and improved readability:
![image](https://github.com/user-attachments/assets/9a159294-ff7e-4fd1-a0d8-974d4b0d2be2)


---

## 🌐 PicoCTF: *WebDecode* — Web Exploitation Writeup

### Challenge Type: Web Exploitation  
### Difficulty: Easy  
### Author: *Your Name or GitHub Handle*

---

### 🔍 Step-by-Step Walkthrough

#### 🔹 **Step 1:**  
Click on the provided **"here"** link to open the challenge website. Once there, navigate to the **"About"** section.  
Also, open [CyberChef](https://gchq.github.io/CyberChef/) in a new tab — we'll need it later for decoding.
![image](https://github.com/user-attachments/assets/66189b57-e4a4-4239-8a33-6d0af7490b61)
![image](https://github.com/user-attachments/assets/71b26e90-9fe4-430a-bfc1-a04534819cae)


---

#### 🔹 **Step 2:**  
Right-click anywhere on the webpage and select **"View Page Source"** or **"Inspect"** to examine the underlying HTML code.
![image](https://github.com/user-attachments/assets/edb1d531-c16e-47de-8455-4a5e8bcaeaa3)



---

#### 🔹 **Step 3:**  
Look through the page source to search for the **flag**. If you spot it directly, great! If not, don’t worry — move to the next step.

---

#### 🔹 **Step 4:**  
If the flag isn’t immediately visible, search for the keyword **`notify: true`** or similar. Near that, you’ll likely find an **encoded or encrypted flag
![image](https://github.com/user-attachments/assets/429bc48d-e118-4d0d-a668-212043c39b08)


---

#### 🔹 **Step 5:**  
Copy the encoded string and paste it into **CyberChef**. Use the **"Magic"** or **"Auto Decode"** or simply click on the **"Cook"** button to decode the data. You should now see the flag revealed.
![image](https://github.com/user-attachments/assets/283c5248-d4a5-4f9f-98f3-989d0b1a8558)


---

#### 🔹 **Step 6:**  
🎉 **Congratulations!** The decoded flag should be visible on your screen. Copy it, paste it into the PicoCTF platform, and click **"Submit Flag"** to complete the challenge.
![image](https://github.com/user-attachments/assets/a41b5caa-f00a-4d22-ab3a-8c0ffbf4229e)

---

### 🧠 Final Thoughts

This challenge highlights the importance of inspecting hidden or encoded content within a webpage and using tools like **CyberChef** to decode it. It's a great example of how developers might unintentionally leave sensitive data accessible through client-side code.

---
Here's a cleaned-up and attractive version of your **PicoCTF challenge writeup for "Unminify"**, with corrected grammar, improved formatting, and better structure for a GitHub `README.md`.

---

## 🔍 PicoCTF: *Unminify* — Web Exploitation Writeup

### Challenge Type: Web Exploitation  
### Difficulty: Very Easy  
### Author: *Your Name or GitHub Handle*

---

### 🧭 Step-by-Step Walkthrough

#### 🔹 **Step 1:**  
Click on the provided **"here"** link to open the challenge website. You’ll land on a simple web page.
![image](https://github.com/user-attachments/assets/0d17df4d-c712-4399-a1f1-e1baa45524e1)

---

#### 🔹 **Step 2:**  
Right-click anywhere on the page and select **"View Page Source"** or **"Inspect"** to open the developer tools and view the underlying code.
![image](https://github.com/user-attachments/assets/04fef0da-9f69-4a14-afa5-8d44eeb80ae8)

---

#### 🔹 **Step 3:**  
Once you're in the source code, carefully look through the content to **locate the flag**.

---

#### 🔹 **Step 4:**  
The flag should be **clearly visible** in the code — no decoding or decryption is needed.
![image](https://github.com/user-attachments/assets/0d40a47d-b3fa-4627-a824-943b377f97f7)


---

#### 🔹 **Step 5:**  
🎉 **Congratulations!** You’ve found the flag.  
Simply copy it, paste it into the PicoCTF submission box, and click **"Submit Flag"** to complete the challenge.
![image](https://github.com/user-attachments/assets/3f3263bc-044d-405a-968a-28c46aa39688)


---

### 🧠 Final Thoughts

This challenge demonstrates how even **minified or embedded code** can sometimes expose sensitive information. Always check the source code — it's often the first and simplest step in web exploitation challenges.

---

## 🔎 PicoCTF: *Inspect HTML* — Web Exploitation Writeup

### Challenge Type: Web Exploitation  
### Difficulty: Very Easy  
### Author: *Your Name or GitHub Handle*

---

### 🧭 Step-by-Step Walkthrough

#### 🔹 **Step 1:**  
Click on the provided **"here"** link to open the challenge website. This will take you to a basic web page.
![image](https://github.com/user-attachments/assets/2e49c7a5-0814-4545-97a1-02914d79931f)


---

#### 🔹 **Step 2:**  
Right-click anywhere on the page and choose **"View Page Source"** or **"Inspect"** to open the developer tools and view the page's HTML source code.
![image](https://github.com/user-attachments/assets/06d34b5e-f504-4008-ac61-9906285b336c)


---

#### 🔹 **Step 3:**  
In the source code, **search for the flag** — it's hidden in the HTML and doesn’t require any decoding.

---

#### 🔹 **Step 4:**  
Scroll toward the **end of the code** — you’ll spot the flag clearly embedded there.
![image](https://github.com/user-attachments/assets/f7185e6d-d3c3-477b-b862-84817555db01)

---

#### 🔹 **Step 5:**  
🎉 **Congratulations!** You've successfully found the flag.  
Copy it, paste it into the PicoCTF platform, and click **"Submit Flag"** to complete the challenge.
![image](https://github.com/user-attachments/assets/50262001-ddce-413a-b083-94cf92db1b13)


---

### 🧠 Final Thoughts

This challenge is a great reminder to always **inspect the page source** — sometimes the flag is hidden in plain sight! It's a classic example of client-side exposure in web applications.

---

Here's a clean, grammatically correct, and GitHub-optimized version of your **PicoCTF challenge writeup for "Includes"**, structured in a professional and clear format for a `README.md`:

---

## 🔍 PicoCTF: *Includes* — Web Exploitation Writeup

### Challenge Type: Web Exploitation  
### Difficulty: Easy  
### Author: *Your Name or GitHub Handle*

---

### 🧭 Step-by-Step Walkthrough

#### 🔹 **Step 1:**  
Click on the **"here"** link provided in the challenge to open the target website. You'll see a simple web page.
![image](https://github.com/user-attachments/assets/6d90b68e-6dd1-4608-8265-13f77e421a44)

---

#### 🔹 **Step 2:**  
Right-click anywhere on the page and choose **"View Page Source"** or **"Inspect"** to open the browser’s developer tools.
![image](https://github.com/user-attachments/assets/8aac4dd2-6a27-4670-bcd2-c08d76c25135)

---

#### 🔹 **Step 3:**  
In the page source, you’ll notice two linked files:
- `style.css`
- `script.js`

Start by clicking on **`style.css`**.
![image](https://github.com/user-attachments/assets/effb8c04-c8b5-47c7-aa0b-b63066fd51a9)

---

#### 🔹 **Step 4:**  
Inside `style.css`, you’ll find the **first part of the flag**, often hidden in a comment.  
Copy this part of the flag — but **do not submit it yet**.
![image](https://github.com/user-attachments/assets/e7d6bbac-363b-4f3c-8220-d13e2eccb798)

---

#### 🔹 **Step 5:**  
Next, open the second file: **`script.js`**.  
There, you’ll find the **second part of the flag**. Copy this portion as well.
![image](https://github.com/user-attachments/assets/c2c2cb6a-4408-4e98-959b-8354fe1ae94d)

---

#### 🔹 **Step 6:**  
🎉 **Congratulations!** You’ve now obtained **both parts of the flag**.  
Combine them carefully (make sure there are **no extra spaces between them**), paste the complete flag into PicoCTF, and click **"Submit Flag"**.
![image](https://github.com/user-attachments/assets/4756164a-9499-4b7d-8833-d4d6682cfc90)

---

### 🧠 Final Thoughts

This challenge teaches a valuable lesson about **included external files**. Developers sometimes leave sensitive information in files like `.css` or `.js`, assuming they won't be checked — but for a hacker or CTF participant, these are goldmines.

Always inspect external resources when assessing a web application's structure and behavior!

---

