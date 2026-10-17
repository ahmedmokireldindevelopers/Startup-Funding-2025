# Secure files and password protection

## Important limitation

A public GitHub repository cannot securely password-protect an individual PDF, spreadsheet, or DOCX file. If the file is committed to a public repository, anyone can download it, inspect Git history, or copy an old version.

A password prompt inside a React/Vite page is also not real protection: the password and the encrypted file key would be delivered to the browser and can be inspected.

## Recommended options

### Option 1 — Private GitHub repository

Use a private repository for internal documents and control access through GitHub collaborators or an organization team. This protects the repository, not a public link to a single file.

### Option 2 — Encrypt an archive locally

With 7-Zip, create an AES-256 encrypted archive before sharing it:

```bash
7z a -t7z -mhe=on -p 'investor-data-room.7z' 'Investor Data Room/'
```

- `-p` asks for the password interactively.
- `-mhe=on` encrypts file names as well as file contents.
- Do not place the password in Git, a README, a script, or the same email as the archive.

To extract it:

```bash
7z x 'investor-data-room.7z'
```

### Option 3 — Password-protected PDF

Use a trusted desktop PDF editor that supports an **open password** and, separately, a **permissions password**. Choose AES-256 when available, disable copying/editing only when it is appropriate for the recipient, and keep the original source file in a private location.

Before sending, test the protected file in a separate viewer or account. A permissions-only password is weaker than an open password because the document can still be viewed without authentication.

### Option 4 — Private data room

For investor diligence, use a private data-room or cloud-storage folder with named-user access, expiration dates, download controls, and access logs. Share the link only after a basic qualification step. Revoke access when the process ends.

## Suggested data-room structure

```text
00_Index_and_Read_Me.pdf
01_Company_Overview/
02_Product_and_Traction/
03_Financial_Model/
04_Legal_and_Compliance/
05_Team/
06_Fundraising_Ask/
```

Keep sensitive identity documents, credentials, API keys, customer-level exports, and unreleased security findings outside the repository and outside a broad investor link. Use a separate, time-limited channel for anything that truly needs to be shared.

## Safe rule for this project

- Public learning PDFs: keep them in GitHub if their license permits redistribution.
- Proprietary templates or paid resources: store them in a private repository or controlled data room.
- Investor diligence files: use named access and expiration, not a front-end password.
- Passwords and encryption keys: never commit them to this repository.
