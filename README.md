# IntroToBurp-CTF-Write-Up

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

In Burp Suite, set the intercept to "on" so that Burp can capture the request when you attempt to submit the OTP.

Step 5: View the OTP in Burp Suite
After entering any random 4-digit number for the OTP, the intercept will capture the request.

In Burp Suite, click on the intercepted OTP request to view the number that was captured.

Step 6: Modify the OTP Request
In the intercepted request, remove the OTP number that was originally entered.

After that, click the "Forward" button at the top of Burp Suite to forward the request with the modified OTP.

Step 7: Find the Flag
Once the request is forwarded, you will be presented with the flag.

Copy the flag, which will be displayed in the response or somewhere on the page.

Step 8: Submit the Flag
Paste the flag into the picoCTF platform to complete the challenge.

