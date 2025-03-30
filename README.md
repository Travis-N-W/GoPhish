# GoPhish

## Disclaimer
This project is intended for educational and ethical testing purposes only. Unauthorized use of phishing techniques for malicious activities is illegal and punishable by law. Always obtain proper authorization before conducting any security assessments.

## 📸 Project Screenshots
Click [here](https://github.com/Travis-N-W/GoPhish/tree/main/screenshots) to view all screenshots.

## Brief Objective

The objective of this project was to demonstrate a simulated phishing attack using the GoPhish platform. The goal was to create a realistic phishing campaign, leveraging tools such as GoPhish, ngrok, and custom email and landing page templates to conduct a controlled, ethical demonstration. 

By configuring the sending profile, creating a landing page resembling Instagram, and directing the victim to a fake login page, the project aimed to showcase the process of credential harvesting in a phishing attack. The results of the campaign, including the victim's stolen credentials, were tracked and displayed on the GoPhish dashboard, providing insights into the success and impact of the phishing attack.

## Skills Learned
- Credential Harvesting
- Phishing Campaign Setup
- Campaign Monitoring and Analysis
- Ngrok Tunneling

## Tools Used
- Ngrok
- GoPhish
- Ubuntu Virtual Machine

## Steps

### 1. Downloading and Setting Up GoPhish
- Access the official GoPhish GitHub repository: [GoPhish Releases](https://github.com/gophish/gophish/releases)
- Download the pre-built binary for 64-bit Linux (Ubuntu in this case).
- Modify the file permissions to make it executable.
- Run the GoPhish binary.
- Open a browser and enter the GoPhish HTTPS IP address.
- Log in using the default credentials: 
  - Username: `admin`
  - Password: (found in the terminal output)

### 2. Setting Up Ngrok for Public Access
- Visit [Ngrok](https://ngrok.com/) and sign up for a free account.
- Download the Ngrok binary and set up authentication.
- Run the following command to create a secure tunnel:
  ```sh
  ./ngrok http 80
  ```
- Copy the generated publicly accessible Ngrok URL.

### 3. Configuring Email Sending Profile
- Set up an SMTP server in GoPhish:
  - SMTP Server: `smtp.gmail.com:465`
  - Username: Victim’s email address
  - Password: Use an App Password (Generated via Google Security settings)
- Save the profile.

### 4. Creating the Phishing Landing Page
- Download an Instagram-themed HTML template from [Gophish Templates](https://github.com/rat-c/gophish-templates).
- Set up the phishing landing page with a redirection to [Instagram](https://www.instagram.com/).

### 5. Creating a Target Group
- Navigate to **Users & Groups** in GoPhish.
- Create a new group and add target email addresses.

### 6. Launching the Phishing Campaign
- Go to the **Campaigns** section in GoPhish.
- Fill out the required details:
  - Target group
  - Sending profile
  - Landing page
  - Ngrok URL
- Start the campaign to send phishing emails.

### 7. Executing the Attack Simulation
- Open the victim’s email account and click the phishing link.
- Enter login credentials on the fake landing page.
- Victim gets redirected to the real Instagram page.

### 8. Analyzing Results in GoPhish
- Access the GoPhish dashboard.
- View metrics such as email opens, click-through rates, and captured credentials.

## Conclusion
This project successfully demonstrated a phishing attack simulation using GoPhish. By following these steps, security professionals can educate users about phishing threats and improve cybersecurity awareness within organizations.
