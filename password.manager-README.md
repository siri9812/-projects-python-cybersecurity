🔐 Password Manager
====================
A simple terminal-based password manager built with Python.
Securely stores hashed credentials in memory using SHA-256
encryption. No external dependencies required.


✨ Features
-----------
  🔒  Password hashing with SHA-256 (hashlib)
  👤  Create accounts with username & password
  🔑  Secure login verification
  🔇  Hidden password input (getpass)
  🪶  Lightweight and dependency-free


⚙️ How It Works
----------------
  - User passwords are hashed with SHA-256 before storage
  - Hashed passwords are stored in an in-memory dictionary
  - Login compares the hash of the entered password against
    the stored hash — the plain password is never saved
  - getpass.getpass() hides password input from the terminal


🛠 Installation
---------------
  No external packages needed. Requires Python 3.x

  # Clone the repository
  git clone https://github.com/siri9812/password-manager.git

  # Navigate into the project folder
  cd password-manager

  # Run the script
  python password_manager.py


▶️ Usage
---------
  Run the script and follow the on-screen menu:

  Enter 1 to create an account, 2 to login, or 0 to exit: 1
  Enter your username: alice
  Enter your desired password:
  Account created successfully!

  Enter 1 to create an account, 2 to login, or 0 to exit: 2
  Enter the username: alice
  Enter your password:
  Login successful!


🖥 Example Output
------------------
  Enter 1 to create an account, 2 to login, or 0 to exit: 1
  Enter your username: alice
  Enter your desired password:
  Account created successfully!

  Enter 1 to create an account, 2 to login, or 0 to exit: 2
  Enter the username: alice
  Enter your password:
  Login successful!

  Enter 1 to create an account, 2 to login, or 0 to exit: 0


📦 Functions
-------------
  create_account()
      Prompts for a username and password, hashes the password
      using SHA-256, and stores it in the password manager dict.

  login()
      Prompts for credentials, hashes the entered password, and
      compares it against the stored hash for verification.

  main()
      Runs the interactive menu loop until the user exits.


⚠️ Limitations
---------------
  - Data is stored in-memory only — all accounts are lost
    when the script exits (no file or database persistence)
  - SHA-256 is not ideal for password hashing — consider
    using hashlib.pbkdf2_hmac() or bcrypt for production use
  - No account update or delete functional
