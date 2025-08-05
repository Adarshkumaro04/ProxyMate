🚀 Proxymate
Proxymate is a lightweight and handy CLI tool designed to simplify managing proxy settings for npm, Git, and Windows environment variables using PowerShell. It's especially useful for students and professionals working behind institutional or enterprise proxies.

✨ Features
✅ Set Proxy – Easily configure HTTP & HTTPS proxy for npm, Git, and system environment.

❌ Unset Proxy – Cleanly remove all proxy settings in one command.

📊 Status Check – View the current proxy settings for your system and developer tools.

🏫 IIIT Allahabad Mode – Auto-configures proxy settings for IIIT-A campus with one command.

📦 Installation
Install Proxymate globally using npm:

bash
Copy
Edit
npm install -g @adarshnpm/proxymate
⚙️ Usage
➕ Set Proxy
To configure custom proxy settings:

bash
Copy
Edit
proxymate set --http http://<your-proxy>:<port>
This will:

Set proxy for npm and Git

Generate .proxyenv.ps1 script for setting system proxy

Provide instructions to run the script

🏫 IIIT Allahabad Users
If you're on the IIIT-A campus network, simply run:

bash
Copy
Edit
proxymate set
This will auto-set:

cpp
Copy
Edit
http://172.31.2.4:8080
Note: You may still need to log in via browser to activate the proxy.

➖ Unset Proxy
To remove all proxy settings:

bash
Copy
Edit
proxymate unset
This command will:

Remove proxy from npm and Git

Delete the .proxyenv.ps1 file

🔍 Check Proxy Status
To view current settings:

bash
Copy
Edit
proxymate status
It will show:

npm proxy config

Git proxy config

Environment variable status

⚠️ Prerequisites
To apply system proxy via PowerShell, you must allow script execution:

Check Current Execution Policy:
powershell
Copy
Edit
Get-ExecutionPolicy
If Restricted, Update It:
Run in Admin PowerShell:

powershell
Copy
Edit
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
Then apply the proxy script:

powershell
Copy
Edit
. $env:USERPROFILE\proxyenv.ps1
🛠️ Troubleshooting
❓ npm proxy not set?
If npm config get proxy returns null, manually set it:

bash
Copy
Edit
npm config set proxy http://<your-proxy>:<port>
npm config set https-proxy http://<your-proxy>:<port>
Then verify with:

bash
Copy
Edit
cat ~/.npmrc
🤝 Contributing
Want to make Proxymate better?

Fork the repo

Create your feature branch:

bash
Copy
Edit
git checkout -b feature-name
Commit your changes:

bash
Copy
Edit
git commit -am "Add new feature"
Push to the branch:

bash
Copy
Edit
git push origin feature-name
Open a Pull Request


📄 License
This project is licensed under the ISC License.
