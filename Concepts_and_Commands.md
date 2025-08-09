## <h1>Git Configuration</h1>
- Need to configure git, to identify who you are:
  --Every commit you make is associated with a username and email.
  --Helps in tracking authorship & collaborating in teams.
- Key Config Variables:
  1. user.name[Mandatory]: Your full name (e.g., "John Doe")
  2. user.email[Mandatory]: Your email (e.g., "john@example.com")
  3. core.editor: Which code editor git uses for commit messages.
  4. init.defaultBranch: Default branch name for a new repo
  5. Global vs Local Config:
     --global: Applies to your entire machine (all repos)
     --Local config (without --global): Applies only to the current repository
  6. Git Config **Commands**:
     <h2>**git config --global user.name "Alice Johnson"**</h2>
     <h2>**git config --global user.email "alice@example.com"**</h2>

## <h1>Authentication - Connect your local GIT to your GITHUB account</h1>
- Authentication links your local Git actions with your GitHub account permissions.
- Authentication — When you push or pull to/from GitHub, Git needs to verify you are allowed to do so. Ways to connect:
  1. Using HTTPS, GitHub asks for your username and password/personal access token (PAT).
  2. Using SSH, GitHub authenticates you via your SSH keys. (Secure key based connection)
- Why connect Git to Github:
  --Code is stored remotely (on cloud).
  --Team members can clone and contribute.

## <h1>What Are SSH Keys ?</h1>
-SSH keys are like a digital lock and key.
🔑 Private key – stays safely on your computer.
🗝️ Public key – you upload it to GitHub.
-Instead of using a username and password every time (or a token), you can use SSH keys — a safer and easier method.
- Steps to create a connection using SSH key:
  1. You create a key pair (private + public) 
     **ssh-keygen -t rsa -b 4096 -C "your_email@example.com"**
     []
     This creates two files:
        id_rsa (your private key — don't share it!)
        id_rsa.pub (your public key)
  3. You add the public key to your GitHub account.
     Copy Public Key -Show your public key:
     **cat ~/.ssh/id_rsa.pub**
     Add Key to GitHub
       Go to GitHub → Settings → SSH and GPG keys
       Click "New SSH key"
       Paste the key → Give it a name → Save
     Test Connection
     **ssh -T git@github.com**
     You should see output: Hi your-username! You've successfully authenticated...
  4. You clone or push using the SSH link (e.g., git@github.com:...).
     **git clone git@github.com:yourusername/your-repo.git**
  5. GitHub sees your key and allows you to work without asking for password/token.
 
## Commands Explanation:
1. **ssh-keygen -t rsa -b 4096 -C "your_email@example.com"**
ssh-keygen	Command to generate a new SSH key pair (public/private).
-t rsa	Specifies the type of key: RSA (a common, secure encryption method).
-b 4096	Sets the key size to 4096 bits (more secure than the default 2048).
-C "your_email@example.com"	Adds a label/comment to the key (helps identify it later). Usually your email.
2. **cat ~/.ssh/id_rsa.pub**
-cat is a command that displays the contents of a file in the terminal.
-~/.ssh/id_rsa.pub is the default file where your SSH public key is stored (after you generate it with ssh-keygen).
3. **git --version**
   Shows the installed Git version.
4. **pwd**
   Displays the current directory path.
5. **cd**
   Changes the current directory.
6. **git clone \[URL]**
   Downloads a copy of someone else's public Git repo via HTTP.
7. **history**
   Lists the recently used commands in the terminal.
8. **ls -a**
   Lists all files in a directory, including hidden ones starting with a dot.



