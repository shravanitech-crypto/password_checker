
# Password Strength Checker 🔐

## 📌 Project Description
The Password Strength Checker is a simple Python program that checks whether a password satisfies basic security requirements. It validates the password based on its length, digits, uppercase letters, lowercase letters, and special characters.

## 🎯 Features
- Checks whether the password contains at least 8 characters.
- Ensures at least one digit (0–9) is present.
- Checks for at least one uppercase letter (A–Z).
- Checks for at least one lowercase letter (a–z).
- Ensures at least one special character is present.
- Displays an appropriate message if a requirement is not satisfied.

## 🛠️ Technologies Used
- Python
- Built-in Python functions: `len()`, `any()`, `isdigit()`, `isupper()`, and `islower()`.

## 💻 Source Code
```python
def pass_check(password):
    if len(password) < 8:
        return "Password must be at least 8 characters long."

    if not any(char.isdigit() for char in password):
        return "Password must contain at least one digit."

    if not any(char.isupper() for char in password):
        return "Password must contain at least one uppercase letter."

    if not any(char.islower() for char in password):
        return "Password must contain at least one lowercase letter."

    if not any(char in "!@#$%^&*()-_=+[]{}|;:'\",.<>?/`~" for char in password):
        return "Password must contain at least one special character."

    return "Password created Successfully."


print(pass_check("password123!"))
```

## ▶️ How to Run the Program

1. Install Python on your computer.
2. Copy the code into a file named `password_checker.py`.
3. Open a terminal in the folder containing the file.
4. Run the following command:

```bash
python password_checker.py
```

## 📤 Sample Output

```text
Password must contain at least one uppercase letter.
```

**Explanation:** The password `password123!` contains lowercase letters, digits, and a special character, but it does not contain an uppercase letter.

## 📚 Concepts Learned
- Conditional statements (`if`)
- Functions and return statements
- String handling
- Generator expressions
- The `any()` function
- Password validation logic

## 🚀 Future Improvements
- Allow users to enter a password using keyboard input.
- Add a password strength indicator.
- Provide multiple validation messages at once.
- Add checks for commonly used or weak passwords.

## 👩‍💻 Author
Shravani Sirsat
