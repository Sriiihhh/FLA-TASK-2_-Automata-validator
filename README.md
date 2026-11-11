# Automata Validator
### Finite Automata-Based Input Validation System

## Project Overview
Automata Validator is a Python-based web application that demonstrates the use of Finite Automata in real-world input validation. The project implements three validation applications: ATM PIN validation with card locking, password policy validation, and email format validation.

The system processes user inputs character by character using predefined state transitions and determines whether the given input satisfies the specified rules.

## Applications

### 1. ATM PIN Validation and Card Lock
- Validates ATM PINs containing exactly four digits.
- Rejects non-digit characters and incorrect PIN lengths.
- Simulates an ATM card-lock mechanism after three consecutive incorrect PIN attempts.
- Resets the failed-attempt count after a correct PIN.

### 2. Password Policy Validation
- Minimum length: 8 characters.
- Maximum length: 16 characters.
- Requires at least one uppercase letter.
- Requires at least one lowercase letter.
- Requires at least one digit.
- Requires at least one special character.
- Uses character classification and bitmask-based state tracking.

### 3. Email Format Validation
- Checks for a valid username.
- Requires exactly one `@` symbol.
- Requires the domain to begin with a letter.
- Allows letters and digits in the remaining domain.
- Requires a dot followed by an extension containing at least two letters.
- Rejects inputs that do not follow the defined format.

## Technologies Used
- Python
- Streamlit
- Graphviz
- Pytest

## Project Structure


Automata_Validator/
│
├── app.py
├── requirements.txt
├── README.md
│
├── automata/
│   ├── __init__.py
│   ├── atm_pin.py
│   ├── password.py
│   └── email_validator.py
│
├── diagrams/
│   ├── generate_diagrams.py
│   ├── atm_pin_dfa.png
│   ├── password_dfa.png
│   └── email_dfa.png
│
├── tests/
│   └── test_validators.py
│
├── screenshots/
└── report/




## Testing

The project uses Pytest to verify the correctness of the validation functions.

Run the test suite using:

```bash
python -m pytest tests/test_validators.py -v
```

**Test Result:** 14 test cases passed successfully.

## State Diagrams

The project includes state diagrams generated using Graphviz to illustrate the transitions and accepting states of the three validation automata.

## Limitations
- The ATM PIN validation checks the PIN format, while the card-lock mechanism is a simulation and does not connect to an actual banking system.
- Password validation checks the defined character and length requirements but does not check against leaked-password databases.
- Email validation checks a simplified email format and does not verify whether the email account actually exists.

## Conclusion
This project demonstrates how Finite Automata can be applied to practical input validation problems. By implementing ATM PIN, password and email validation, it illustrates state transitions, accepting states, dead states and the role of automata in designing rule-based validation systems.


