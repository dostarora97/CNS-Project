# 1. About 
Submitted as: Project for Cryptography & Netwrok Security(2019), RVCE 2020  
Submitted by: [Dost Arora](https://github.com/dostarora97) & [Anmol Gaba](https://github.com/anmolgaba)  
Project Document : https://docs.google.com/document/d/1fR1WpjXpgekh7VzAPWhu2FC7JwcrrqDSpjxf2FHGmd8/edit?usp=sharing  
**Forked From : [ahui2016/PyMima](https://github.com/ahui2016/PyMima)**

# 2. Installation
Python ^3.6.2
```
git clone https://github.com/dostarora97/RVCE-CNS-Project
python3 -m pip install -r requirements.txt
python3 create_default_account.py
python3 mainwindow.py
```
## 2.1 Note
- The initial master password is `keep all secrets` & is stored in `create_default_account.py`. You can modify it there, before creating an account.
- `pymima.db` stores all the data. If the master-password is forgotten the data cannot be recovered.
- To reset the master password, delete the `pymima.db` file and run `python3 create_default_account.py`.
- `python3 create_default_account.py` creates a default account with the default master password as stated in the file and also produces `pymima.db`
- Use `python3 change_master_password.py` to update the master password. Modify the old-password & the new-password in the file according to the needs.

# 3. Docs - from [source](https://github.com/ahui2016/PyMima/blob/master/README.md)

## 3.1 PyMima
- GUI Password Manager by PyQt
- This is a simple but basic full-featured desktop stand-alone password management software.
- With SQLite, all data is stored in a single file (pymima.db) for easy backup

## 3.2 Maximum Feature keep revision History
- When deleting a project, move it to the recycle bin first and you can restore it at any time.
- Deleting items from the recycle bin is completely removed, so make sure you don't accidentally delete them.
- Many password management softwares have a recycle bin function, but there are not many revision history.
- Use the software to modify the project each time, retaining the revision history
- Due to the retention of the revision history, the passwords used in the past are all retained!

## 3.3 Written In Pyqt5: Open-source, Easy To Modify , Cross Platform
- Python is a simple and easy to read language, Qt documentation is very detailed
- Programs written in PyQt5 make it easy to run on all three desktop platforms
- PyQt5 is a good choice for writing some small software with GUI interface for your own use.
- Although the software is simple, some common desktop GUI usages are used, which can be used as a reference example.
- Of course, the level is limited, it can only be regarded as a jade, the code quality is not high.

## 3.4 Basic Skills
- Although it is just a small software, the interface is not modern, but it is very convenient to use.
- such as:
	- For common projects, you can double click on the star top
	- User name, password, etc. can be double-clicked to copy
	- Simple search function
	- Have a simple random password generation function
	- When the password is displayed, the numbers are displayed in different colors for easy identification.
	- Timing lock function is also available (in case of temporary leaving forgotten to close and leaking)
- Especially for the recycle bin and modification history, these two functions are not easy to save by using the excel or text file to save the password.

## 3.5 About Security
- The encryption method uses NaCl's secretbox, which is mainly considered to be friendly to programming in this way, easy to handle correctly, not easy to make mistakes, and security is also sufficient. The specific encryption strength can be searched and researched by itself.
- As mentioned above, since the encryption method has high security, please remember the master password. Once you forget it, there is no way to help you crack it.
- NaCl is a widely supported encryption library, such as Ruby, Go, JavaScript, etc., you can easily use NaCl, so as long as you have a password, you can easily write a decryption program to handle pymima.db in other languages, so this software It doesn't limit you, you can easily migrate.
- This software provides a double-click function to copy the user name or password, which is convenient to use, but pay attention to:
	There is no automatic clearing of the clipboard function, so after copying the password, pay attention to clearing the clipboard yourself.
	The reason why the clipboard is not automatically cleared, because the copy itself is a security risk, other programs can monitor the clipboard, it is impossible to prevent. There are still a lot of people who will use the clipboard assisting software, which will automatically keep the history of the clipboard so that it can be copied at any time.
	But generally speaking, in your own computer, the problem is not too big, don't be too nervous, and my own convenience is also directly double-clicked and copied.
- All data is encrypted and saved in pymima.db. This file can be saved to the mobile hard disk or network disk for backup. As long as the strong password is used, most people can't crack it. A strong password is a 12-digit password that contains uppercase and lowercase letters and numbers (no personal information such as a phone number or birthday). It is theoretically difficult to brute force.
- There is no absolute security. I even open the source code. In case there is any leak or loss, I am not responsible. (This is the same for any other password management software, no absolute security)
