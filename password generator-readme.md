🔐 Password Generator
======================
A lightweight, cryptographically secure password generator built
with Python's built-in secrets module. No dependencies required.


✨ Features
-----------
  🔒  Cryptographically secure  (uses secrets module)
  🔢  Customizable length
  🔤  Letters, digits & special characters
  🪶  Lightweight and dependency-free


⚙️ How It Works
----------------
  - Builds an alphabet from ascii_letters, digits, and punctuation
  - Uses secrets.choice() for secure random selection
  - Joins characters into a password of the desired length
  - Default length is 10 if none is specified


🛠 Installation
---------------
  No external packages needed. Requires Python 3.6+

  # Clone the repository
  git clone https://github.com/siri9812/password-generator.git

  # Navigate into the project folder
  cd password-generator

  # Run the script
  python password_generator.py


▶️ Usage
---------
  # Run directly:
  python password_generator.py

  # Or import into your project:
  from password_generator import generate_password

  password = generate_password(length=16)
  print(f"Generated password: {password}")


🖥 Example Output
------------------
  Generated password: c(cO:JRCgC


📦 Parameters
--------------
  generate_password(length: int = 10)



⚠️ Limitations
---------------
  - Does not guarantee inclusion of every character type
    (e.g. may occasionally produce no symbol by chance)
  - Password length must be a positive integer


📄 License
-----------
  MIT License - free to use and modify for personal or
  commercial projects.
