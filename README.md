Proxymate


Proxymate is a lightweight command-line tool designed to simplify the management of proxy settings for npm, Git, and system environment variables on Windows using PowerShell. It helps developers easily configure and remove proxy settings with simple commands, especially useful for students and professionals working behind a proxy.


✨ Features:-

✅ Set Proxy: Configure HTTP & HTTPS proxy for npm, Git, and environment variables.

❌ Unset Proxy: Cleanly remove all proxy configurations in one command.

📊 Status Check: View the current proxy settings of your system and developer tools.

🏫 IIIT Allahabad Mode: Built-in default proxy config for IIIT-A campus network.



📦 Installation:-

Install proxymate globally via npm:

bash
Copy
Edit
npm install -g @adarshnpm/proxymate
⚙️ Usage
➕ Set Proxy
To configure proxy settings:

bash
Copy
Edit
proxymate set --http http://<your-proxy>:<port>
This command will:

Set the proxy for npm and Git

Generate a .proxyenv.ps1 script to configure system environment proxy

Provide instructions to run the script

🏫 IIIT Allahabad Users
If you're a student of IIIT Allahabad, just run:

bash
Copy
Edit
proxymate set
It will auto-configure http://172.31.2.4:8080 as your proxy for all tools.

You’ll still need to log in through the proxy using your browser once.

➖ Unset Proxy
To remove all proxy configurations:

bash
Copy
Edit
proxymate unset
Removes proxy from npm and Git

Deletes the .proxyenv.ps1 script

🔍 Check Proxy Status
To see current settings:

bash
Copy
Edit
proxymate status
This shows:

npm proxy config

Git proxy config

Environment variables

⚠️ Prerequisites
PowerShell must allow script execution to run .proxyenv.ps1.

Update Execution Policy:
Check current policy:

powershell
Copy
Edit
Get-ExecutionPolicy
Change policy if restricted:
Run in Admin PowerShell:

powershell
Copy
Edit
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
Apply script:

powershell
Copy
Edit
. $env:USERPROFILE\proxyenv.ps1
🛠️ Troubleshooting
npm proxy config is missing?
If npm config get proxy returns null:

bash
Copy
Edit
npm config set proxy http://<your-proxy>:<port>
npm config set https-proxy http://<your-proxy>:<port>
Check your ~/.npmrc file to verify.

🤝 Contributing
Want to improve proxymate?

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
git commit -am 'Add new feature'
Push and open a Pull Request

👤 Author
Built with ❤️ by Adarsh Kumar
GitHub: @adarshgithub

📄 License
This project is licensed under the ISC License
