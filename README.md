# Overview
CheckMyPass is a Python script designed to help you determine if your password has been compromised in a data breach. 
It uses the Have I Been Pwned API to securely check your password against a database of leaked passwords without exposing your actual password.
! VERY, VERY SAFE AND USEFUL ! 

# Features
Uses SHA-1 hashing to keep your password secure
Implements the k-anonymity model to protect your password during API requests
Simple command-line interface

# Installation
Ensure you have Python 3 installed on your system.
Install the requests module using pip:
pip install requests

# How It Works
SHA-1 Hashing: Your password is hashed using the SHA-1 algorithm.
K-anonymity: The first 5 characters of the hash are sent to the Have I Been Pwned API.
API Response: The API returns a list of hash suffixes and their occurrence counts.
Password Check: The script checks if the suffix of your password hash is in the returned list and how many times it has appeared in data breaches.

# Usage
To run the script, use the following command in your terminal:

python3 checkmypass.py [password1] [password2] ...
Replace [password1] [password2] ... with the passwords you want to check.

# Example
python3 checkmypass.py hello bye jdvksadjksjsfks

# Note
For increased security, instead of passing passwords directly via the command line (which can be risky as it can be hacked), consider reading passwords from a secure text file.

# Additional Information
The script uses the SHA-1 hash algorithm for password hashing.
The k-anonymity model ensures that the API never sees your full password hash, enhancing security.
Major companies like Google, Netflix, and Amazon use similar approaches to protect user data.
For more details on SHA-1 hashing, refer to the Python hashlib documentation.

# Disclaimer
This script is intended for educational purposes and to help you check your password security. Always follow best practices for password management and security.
