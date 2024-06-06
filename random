import string
import random

def generate_password(length, use_letters, use_numbers, use_symbols):
    char_pool = ''

    if use_letters:
        char_pool += string.ascii_letters  # a-z, A-Z
    if use_numbers:
        char_pool += string.digits  # 0-9
    if use_symbols:
        char_pool += string.punctuation  # !@#$%^&*()_+-=[]{}|;:,.<>?/~`

    if not char_pool:
        raise ValueError("At least one character type must be selected")

    # Generate password
    password = ''.join(random.choice(char_pool) for _ in range(length))
    return password

def main():
    try:
        length = int(input("Enter the desired password length: "))
        if length <= 0:
            raise ValueError("Length must be a positive integer")
    except ValueError as e:
        print(f"Invalid input: {e}")
        return

    use_letters = input("Include letters? (y/n): ").strip().lower() == 'y'
    use_numbers = input("Include numbers? (y/n): ").strip().lower() == 'y'
    use_symbols = input("Include symbols? (y/n): ").strip().lower() == 'y'

    try:
        password = generate_password(length, use_letters, use_numbers, use_symbols)
        print(f"Generated password: {password}")
    except ValueError as e:
        print(f"Error: {e}")

if _name_ == "_main_":
    main()
